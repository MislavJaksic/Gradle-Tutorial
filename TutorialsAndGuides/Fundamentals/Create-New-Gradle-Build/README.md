## [Creating New Gradle Builds](https://guides.gradle.org/creating-new-gradle-builds/)

### Initialize

```
$: gradle init  # ->
  # Choose: basic
  # Choose: groovy
  # Choose: default
```

```
build.gradle  # project config
settings.gradle  # build config
```

### Create a task

Task is an atomic piece of work configured in `build.gradle`.  

```
$: ./gradlew copy
$: ./gradlew zip
# Note: see ./build/distributions
```

### Apply a plugin

Plugins are applied in `build.gradle`.  

### Explore and debug your build

```
$: ./gradlew tasks  # list tasks
$: ./gradlew properties  # list properties
```
