## [Consuming JVM Libraries](https://guides.gradle.org/consuming-jvm-libraries/)

### (Manually) Create a project

```
$: gradle wrapper  # create Gradle wrapper
$: touch settings.gradle
$: touch build.gradle
```

Add plugins, repositories and dependencies to `build.gradle`.  

### Create the application

Add `*.java` files to `src/main/java`.  

```
$: ./gradlew jar  # package app
$: ./gradlew build
$: ./gradlew installDist
```

```
# Note: see distributions
  # build/distributions/greeterApp.tar
  # build/distributions/greeterApp.zip
# Note: see installed app
  # build/install/greeterApp

$: build/install/greeterApp/bin/greeterApp Gradle  # run installed app
```
