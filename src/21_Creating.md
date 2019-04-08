# Creating a new plugin

## Plugin Archetype

A new plugin can be created from scratch by running following Maven command:

```bash
mvn -U archetype:generate -Dfilter=io.jenkins.archetypes:
```

This invokes the generation of a new plugin from several project archetypes and requests for all mandatory information like _groupId_, _artifactId_, initial _version_ and _package_ structure.

## Plugin Structure

The plugin workspace is structured as follows:

- **Project root**: Maven build configuration pom.xml and all the project subdirectories
- **src/main/java**: Deliverable Java source code files
- **src/main/resources**: Deliverable resources, such as Jelly and property files for UI
- **src/main/webapp**: Static resources, such as images and HTML files
- **src/test/java**: Unit testing classes
- **src/test/resources**: Necessary resources for unit tests only

## Maven POM

Maven is generally used to build Jenkins plugins and stores the configuration in the pom.xml located at the root directory. New plugin are based on the Plugin Parent POM:
```xml
<parent>
    <groupId>org.jenkins-ci.plugins</groupId>
    <artifactId>plugin</artifactId>
    <version>3.42</version>
    <relativePath />
</parent>
```

The Jenkins baseline version and Java level are mandatory and can be set via Maven property:
```xml
<properties>
    <jenkins.version>2.164.1</jenkins.version>
    <java.level>8</java.level>
</properties>
```

## Further Reading

- [Start a new plugin](https://wiki.jenkins.io/display/JENKINS/Before+starting+a+new+plugin)
- [Jenkins Parent POM](https://github.com/jenkinsci/plugin-pom)
