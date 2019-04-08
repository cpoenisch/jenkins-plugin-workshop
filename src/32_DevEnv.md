# Set up the development environment

## Task
Follow the instructions below to prepare your [local development environment](#local-toolchain), alternatively run with [Docker](#docker) or choose the browser-based online IDE powered by [GitPod](#gitpod).

### Local Toolchain
For building and developing the Jenkins plugin [Java SE Development Kit](#jdk) and [Maven](#maven) are required.

#### IDE
The preferred IDE for this workshop is [IntelliJ IDEA Community Edition](https://www.jetbrains.com/idea) because it is free and Maven is shipped with the installation. Alternatively take the IDE of your choice (Eclipse, NetBeans, etc.) you are most familiar with.

#### JDK
Jenkins core is based on Java and therefore most of the Jenkins plugins also relies on Java or JVM compatible languages like Groovy. For this workshop we will use JDK 8 you can download for free from the [Oracle website](http://www.oracle.com/technetwork/java/javase/downloads/) and install it afterwards. Ensure this JDK is properly configured in your IDE.

#### Maven
Most of the Jenkins plugins utilize Maven as the preferred build management system. The plugin to be changed is already configured as a Maven project providing a _pom.xml_.

Download Maven from related [Apache project](https://maven.apache.org/download.cgi) and extract it to an arbitrary path. Afterwards ensure the _bin/_ subdirectory is added to your _PATH_ in order to invoke _mvn_ from command line.

_IDEA_: Use the bundled Maven version or change it via _Settings > Build Tools > Maven_

In order to make Jenkins repositories available during Maven builds edit your _~/.m2/settings.xml_ (Windows: _%USERPROFILE%\\.m2\\settings.xml_) as follows:

```xml
<settings>
  <pluginGroups>
    <pluginGroup>org.jenkins-ci.tools</pluginGroup>
  </pluginGroups>

  <profiles>
    <!-- Give access to Jenkins plugins -->
    <profile>
      <id>jenkins</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <repositories>
        <repository>
          <id>repo.jenkins-ci.org</id>
          <url>https://repo.jenkins-ci.org/public/</url>
        </repository>
      </repositories>
      <pluginRepositories>
        <pluginRepository>
          <id>repo.jenkins-ci.org</id>
          <url>https://repo.jenkins-ci.org/public/</url>
        </pluginRepository>
      </pluginRepositories>
    </profile>
  </profiles>
  <mirrors>
    <mirror>
      <id>repo.jenkins-ci.org</id>
      <url>https://repo.jenkins-ci.org/public/</url>
      <mirrorOf>m.g.o-public</mirrorOf>
    </mirror>
  </mirrors>
</settings>
```

### Docker

For building and debugging the plugin inside a Docker container you can use following commands:

**Build Plugin**
```bash
docker run -it --rm -v "$PWD":/usr/src/app -v "$HOME"/.m2:/root/.m2 \
-w /usr/src/app maven:3-jdk-8-alpine mvn install
```

**Run Debugging Instance**
```bash
docker run -it -d --rm -p 8080:8080 -v "$PWD":/usr/src/app -v "$HOME"/.m2:/root/.m2 \
-w /usr/src/app maven:3-jdk-8-slim mvn hpi:run
```
<!-- docker run -it --rm -v `pwd`:/usr/src/app -v /c/Users/ChristianPoe/.m2:/root/.m2 -w /usr/src/app maven:3-jdk-8-alpine mvn install -->
<!-- docker run -it -d --rm -p 8080:8080 -v `pwd`:/usr/src/app -v /c/Users/ChristianPoe/.m2:/root/.m2 -w /usr/src/app -e "MAVEN_OPTS=-Djava.awt.headless=true" maven:3-jdk-8-alpine mvn hpi:run -->

### GitPod

As an handy alternative without the need to install any tools locally you can use an one-click online IDE.
[GitPod](https://gitpod.io/) provides a ready-to-code development environment in your browser.

**Usage**
- Prefix any GitHub URL with [https://gitpod.io#](https://gitpod.io#), e.g.: \
[https://gitpod.io/#https://github.com/cpoenisch/yabv-workshop-plugin](https://gitpod.io/#https://github.com/cpoenisch/yabv-workshop-plugin)
- Or use the [browser extension](https://docs.gitpod.io/20_Browser_Extension.html) for Firefox or Chrome
