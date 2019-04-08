# Building a plugin

To build a plugin run following Maven command:

```bash
mvn install
```

When rebuilding a plugin it is sometimes helpful to clean the target directory previously:

```bash
mvn clean install
```

This will create a plugin artifact at _target/&lt;plugin&gt;.hpi_ that can be deployed manually to Jenkins.

## CI Integration

Hosted Jenkins plugins are automatically built with each commit by placing _Jenkinsfile_ at project root.

```bash
#!groovy
buildPlugin()
```

## Further Reading

- [Apache Maven Project](https://maven.apache.org/index.html)
- [Maven Build Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)
- [Pipeline Global Library](https://github.com/jenkins-infra/pipeline-library)
