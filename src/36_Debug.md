# Debug the plugin

## Task

Instantiate a local Jenkins instance for debugging purposes by executing following Maven command:

```bash
mvn hpi:run
```

Open the local Jenkins instance at [http://localhost:8080/jenkins](http://localhost:8080/jenkins) in your browser.

In order to be able to change the display name of a build install the [Build Name Setter](http://wiki.jenkins.io/display/JENKINS/Build+Name+Setter+Plugin) beforehand. Then create at least two dependent Freestyle jobs and configure them to set the build name to anything other than the build number. Start a new upstream build and check if the change you did is working properly.

## Hints
<details>
  <summary>Show / Hide</summary>

- Create an upstream job that triggers a downstream job
- Set the build name in the Build Environment section
- The default build trigger can be selected from post-build actions
</details>
