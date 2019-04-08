# Build the plugin

## Task

First import the cloned plugin repository into your IDE as a Maven project.

Run a full build by invoking Maven from command line or IDE integrated terminal:

```bash
mvn install
```

Watch the build log for any build failures and ensure a .hpi file is created in the target directory.

Optionally, install the built plugin to an existing Jenkins master instance.

## Hints
<details>
  <summary>Show / Hide</summary>

**Maven Repositories**

Add Jenkins plugin repositories to pom.xml or your .m2/settings.xml
```xml
<pluginRepositories>
  <pluginRepository>
    <id>repo.jenkins-ci.org</id>
      <url>https://repo.jenkins-ci.org/public/</url>
  </pluginRepository>
</pluginRepositories>
```

**IntelliJ IDEA**

- Add Maven framework support
- Configure JDK 8 as project SDK and set Java language level to 8

Ensure that following directories are marked as:
- **Source Root**: _src/main/java_
- **Resources Root**: _src/main/resources_
- **Test Source Root**: _src/test/java_
- **Test Resources Root**: _src/test/resources_
- **Excluded**: _target_
</details>
