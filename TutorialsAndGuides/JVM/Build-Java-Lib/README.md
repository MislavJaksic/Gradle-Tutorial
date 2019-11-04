## [Building Java Libraries](https://guides.gradle.org/building-java-libraries/)

### Run the init task

```
$: gradle init  # ->
  # Select type of project to generate:
  #   3: library
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

### Customize the library JAR

You can set a version and add data to MANIFEST:MF.  

```
$: ./gradlew jar
$: jar xf build/libs/demo-0.1.0.jar MANIFEST.MF  # extract MANIFEST.MF
```

### Adding API documentation

```
$: ./gradlew javadoc
# Note: see `build/docs/javadoc/index.html`
```