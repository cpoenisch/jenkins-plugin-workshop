# Debugging a plugin

With help of the [Maven HPI Plugin](https://jenkinsci.github.io/maven-hpi-plugin) Jenkins plugins can be started in a local Jenkins sandbox.

For debugging purposes run following Maven command from plugin project directory:

```bash
mvn hpi:run
```

By default, the debugging instance is then available at [http://localhost:8080/jenkins](http://localhost:8080/jenkins) in your browser.

In order to launch Jenkins on a different port than 8080 use this system property:

```bash
mvn hpi:run -Djetty.port=8090
```

Changing the default context path can be achieved by setting this system property:

```bash
mvn hpi:run -Dhpi.prefix=/debug
```

## Debugging from IDE

Starting a debug session from your IDE requires to set special Maven options:

`MAVEN_OPTS="-Xdebug -Xrunjdwp:transport=dt_socket,server=y,address=8000,suspend=n"`

This allows to hook into the instance and set break points while being in IDE debugging mode.

Changing code while debugging is supported for Jelly/Groovy views, properties and help files with simple page reload in the browser. Utilizing from JVM's hot swap feature does not support changing method signatures. Changes in pom.xml also requires to restart the debugging process.

## Further Reading

- [Plugin Debugging](https://wiki.jenkins.io/display/JENKINS/Plugin+tutorial#Plugintutorial-Changingcodewhiledebugging)
- [Developing with JRebel](https://wiki.jenkins.io/display/JENKINS/Developing+with+JRebel)
- [IDEA Debugging](https://www.jetbrains.com/help/idea/debugging-code.html)
