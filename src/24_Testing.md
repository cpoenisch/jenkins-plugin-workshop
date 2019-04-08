# Testing a plugin

Next to well-known unit testing frameworks like JUnit, TestNG, Spock etc. which can be easily integrated in Java projects, Jenkins provides an own test harness framework built around JUnit to make testing plugins much easier. There are several test techniques included like stubbing, HTML scraping or round-trip testing and provides multiple test harness annotations.

Unit tests can be executed with following Maven command:

```bash
mvn test
```

While building the plugin unit tests can be skipped by appending the Maven command as follows:

```bash
mvn install -DskipTests
```

## Further Reading

- [Jenkins Unit Tests](https://wiki.jenkins.io/display/JENKINS/Unit+Test)
