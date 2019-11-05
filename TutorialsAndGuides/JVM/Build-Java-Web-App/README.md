## [Building Java Web Applications](https://guides.gradle.org/building-java-web-applications/)

### (Manually) Create a project

```
$: gradle wrapper  # create Gradle wrapper
$: touch settings.gradle
$: touch build.gradle
```

Add plugins, repositories and dependencies to `build.gradle`.  

### Add files to the project

Add:
* a servlet and metadata
* index HTML page
* JSP page

### Run the app

```
$: ./gradlew appRun  # run app
# Note: visit http://localhost:8080/webdemo
```

### Add unit tests and mocks with Mockito

```
$: ./gradlew build  # compiles, runs tests, generates a report

# Note: see the HTML report in `build/reports/tests/test/index.html`
# Note: see the XML report in `build/reports/test-results/test/TEST-**.xml`
```

### Add Selenium functional tests

```
$: ./gradlew test  # -> automated browser
```
