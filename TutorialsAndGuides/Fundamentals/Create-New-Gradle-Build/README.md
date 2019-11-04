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

Task is an atomic piece of work.  

```
# Note: add to build.gradle
task copy(type: Copy, group: "Custom", description: "Copies from source to destination") {
    from "src"
    into "dest"
}
```

```
$: ./gradlew copy
```

### Apply a plugin

```
# Note: add to build.gradle
plugins {
    id "base"
}
```

```
# Note: add to build.gradle
task zip(type: Zip, group: "Archive", description: "Archives sources in a zip file") {
    from "src"
    setArchiveName "basic-demo-1.0.zip"
}
# Note: see build/distributions
```

### Explore and debug your build

```
$: ./gradlew tasks  # list tasks
$: ./gradlew properties  # list properties
```
