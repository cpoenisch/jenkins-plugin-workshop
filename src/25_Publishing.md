# Publishing a plugin

## Packaging
To create a local distribution image of your plugin run the following Maven command:

```bash
mvn package
```

After successful packaging an plugin artifact should be created at _target/*.hpi_. This .hpi file can then be manually uploaded to the [Jenkins Update Center](/12_Installation.html#jenkins-update-center) or directly placed in the Jenkins plugin directory (located at _$JENKINS_HOME/plugins_). The Jenkins master needs to be restarted afterwards.

## Hosting
In order to officially host a new plugin in the Jenkins Update Center, meaning it will be available to all Jenkins users worldwide, you first have to meet some prerequisites regarding the plugin structure and open source licensing. Fulfilling those you can request hosting your plugin repository under the [Jenkins GitHub organization](https://github.com/jenkinsci). It is recommended to add your maintainer information and to create a well-documented and up-to-date wiki page for your plugin.

## Further Reading

- [Hosting Plugins](https://wiki.jenkins.io/display/JENKINS/Hosting+Plugins)
