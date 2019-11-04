## [Dependency Management Terminology](https://docs.gradle.org/current/userguide/dependency_management_terminology.html)

```
Configuration: set of dependencies grouped
Dependency: pointer to another software
Dependency constraint: requirements that narrow dependencies

Module: software that evolves over time; has a name, version and can be hosted in a repository
Module metadata: module releases can have info
Module version: changes in the same module type
Platform: a set of modules
  * module set: set of modules published together
  * runtime environments: set of libraries known to work well together
  * deployment environments: Java runtime, application server, ...
Repository: hosts modules

Resolution rule: how a dependency is resolved

Transitive dependency: modules can have their own dependencies
```
