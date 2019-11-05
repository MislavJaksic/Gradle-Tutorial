## [Building Java Applications](https://guides.gradle.org/building-java-applications/)

### Run the init task

```
$: gradle init  # ->
  # Select type of project to generate:
  #   2: application
  # Select implementation language:
  #   3: Java
  # Select build script DSL:
  #   1: Groovy
  # Select test framework:
  #   4: JUnit Jupiter
  # Project name (default: demo): demo
  # Source package (default: demo): demo
```

### Review the generated project files

```
build.gradle  # project config
settings.gradle  # build config
```

### Execute the build

```
$: ./gradlew build  # compiles, runs tests, generates a report
```

```
# Note: see the packaged *.jar
$: jar tf build/libs/demo.jar
```

```
# Note: see the HTML report in `build/reports/tests/test/index.html`
# Note: see the XML report in `build/reports/test-results/test/TEST-**.xml`
```
