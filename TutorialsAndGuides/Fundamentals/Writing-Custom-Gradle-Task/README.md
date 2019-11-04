## [Writing Custom Gradle Tasks](https://guides.gradle.org/writing-gradle-tasks/)

Task is an atomic piece of work.  

### Create an ad-hoc task

Tasks are defined in `build.gradle`.  

```
$: gradle tasks --all  # prints all tasks
$: gradle hello  # -> "Hello, World!"
```

### Make the message configurable

```
$: gradle hello  # -> "Hello, World!"
$: gradle gutenTag  # -> "Guten Tag, Welt!"
```
