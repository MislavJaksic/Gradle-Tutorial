## [Build scans](https://guides.gradle.org/creating-build-scans/)

Build scan is a record of a build: what happened and why.  
Build scans can be published to [online](https://scans.gradle.com/).  

```
S: pwd  # -> /path/to/gradle-build-scan-quickstart
$: ./gradlew build --scan  # create build scan
  # Do you accept these terms? yes
  # Publishing build scan...
# Note: beore viewing the scan you have to give your email
```

---

Configure builds scans per project.  

```
# Note: add to build.gradle
plugins {
    id 'com.gradle.build-scan' version '2.1'
}
buildScan {
    termsOfServiceUrl = 'https://gradle.com/terms-of-service'
    termsOfServiceAgree = 'yes'
}
```

---

Configure builds scans per Gradle installation.  

```
Note: add to buildScan.gradle in /path/to/gradle/home/.gradle/init.d
initscript {
    repositories {
        gradlePluginPortal()
    }
    dependencies {
        classpath 'com.gradle:build-scan-plugin:@scanPluginVersion@'
    }
}
rootProject {
    apply plugin: com.gradle.scan.plugin.BuildScanPlugin
    buildScan {
        termsOfServiceUrl = 'https://gradle.com/terms-of-service'
        termsOfServiceAgree = 'yes'
    }
}
```

---







TODO

## [Gradle and Java](https://guides.gradle.org/building-java-libraries/)

Create a folder.  
Initialize a Java library project with:  
```
gradle init
```
Select the desired options.  

Build the project with:  
```
./gradlew build
```
The build command generates a test report under "build/reports/...".  
The build command also generates a _project_name.jar file.  

To modify the behaviour of jar command modify the "build.gradle" script.  
To generate javadocs use the javadoc command.  

### [Gradle Java dependency management](https://docs.gradle.org/current/userguide/dependency_management_for_java_projects.html)

TODO

### [Publishing](https://docs.gradle.org/5.0/userguide/publishing_overview.html#publishing_overview)

TODO
