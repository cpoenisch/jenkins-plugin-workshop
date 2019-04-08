# Implement the changes

## Task

Change the Groovy view rendering the Build Flow from displaying the build display name instead of the build number. Rebuild the project to check for any syntax or compiling errors.

## Hints
<details>
  <summary>Show / Hide</summary>

- Take a look at the JavaDocs for available [AbstractBuild](https://javadoc.jenkins.io/hudson/model/AbstractBuild.html) methods
- Source file for the Groovy view is located in [resources](https://github.com/cpoenisch/yabv-workshop-plugin/blob/master/src/main/resources/com/axis/system/jenkins/plugins/downstream/yabv/BuildFlowAction/buildFlow.groovy)
- Change the current implementation at line 46 from
```Java
span("${build.parent.name} #${build.number}")
```
to
```Java
span("${build.parent.name} ${build.displayName}")
```
</details>
