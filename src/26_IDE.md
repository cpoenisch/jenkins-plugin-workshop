# IDE Support

Because most Jenkins plugins are based on Java and are built with Maven any IDE software can be chosen that provides JVM language and Maven framework support. The [Maven HPI Plugin](https://github.com/jenkinsci/maven-hpi-plugin) provides an easy way to integrate the plugin lifecycles into the Maven build process.

With help of the [Gradle JPI Plugin](https://github.com/jenkinsci/gradle-jpi-plugin) Groovy and Gradle can be used as an alternative way to build and release such configured plugins.

### Jelly Views

XML based tag libraries for [writing Jelly views](https://wiki.jenkins.io/display/JENKINS/Writing+Jelly+views+with+IDE+assistance) are supported by Stapler plugins available for most modern IDEs (see links to below).

### Internationalization

Support for different languages can be achieved by [internationalization](https://wiki.jenkins.io/display/JENKINS/Internationalization) features in Stapler plugins.

### IntelliJ IDEA

- [Website](https://www.jetbrains.com/idea)
- [Stapler Plugin](https://wiki.jenkins.io/display/JENKINS/IntelliJ+IDEA+plugin+for+Stapler)

### NetBeans

- [Website](https://netbeans.apache.org/)
- [Stapler Plugin](https://github.com/stapler/netbeans-stapler-plugin)

### Eclipse

- [Website](https://www.eclipse.org/eclipseide/)
- [Eclipse Development Guide](https://wiki.jenkins.io/display/JENKINS/Jenkins+plugin+development+with+Eclipse)
- [Alternative Eclipse Setup](https://wiki.jenkins.io/display/JENKINS/Eclipse+alternative+build+setup)
