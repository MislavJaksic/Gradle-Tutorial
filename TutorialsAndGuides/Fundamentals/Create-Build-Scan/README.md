## [Build scans](https://guides.gradle.org/creating-build-scans/)

Build scan is a record of a build: what happened and why.  
Build scans can be published to [online](https://scans.gradle.com/).  

```
$: ./gradlew build --scan  # create build scan
  # Do you accept these terms? yes
  # Publishing build scan...
# Note: before viewing the scan you have to give your email
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
