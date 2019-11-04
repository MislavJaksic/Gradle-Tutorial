## [Writing Custom Gradle Tasks](https://guides.gradle.org/writing-gradle-tasks/)

Task is an atomic piece of work.  

### Create an ad-hoc task

```
# Note: add to build.gradle
tasks.register("hello") {
    group = 'Welcome'
    description = 'Produces a greeting'

    doLast {
        println 'Hello, World!'
    }
}
```

```
$: gradle tasks --all  # prints all tasks
$: gradle hello  # -> "Hello, World!"
```

### Make the message configurable

```
# Note: add to build.gradle
class Greeting extends DefaultTask {  
    String message
    String recipient

    @TaskAction
    void sayGreeting() {
        println "${message}, ${recipient}!"
    }
}

tasks.register("hello", Greeting) {
    group = 'Welcome'
    description = 'Produces a world greeting'
    message = 'Hello'
    recipient = 'World'
}

tasks.register("gutenTag", Greeting) {
    group = 'Welcome'
    description = 'Produces a German greeting'
    message = 'Guten Tag'
    recipient = 'Welt'
}
```

```
$: gradle hello  # -> "Hello, World!"
$: gradle gutenTag  # -> "Guten Tag, Welt!"
```
