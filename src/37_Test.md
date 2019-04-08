# Write unit tests

## Task (optional)

Write a new unit test for the implemented change that is divided into following parts:

**ARRANGE**: Create an upstream job and a downstream job with arbitrary build names \
**ACT**: Schedule a new upstream build \
**ASSERT**: Assert that the job and build pages contain a Build Flow graph with the set build names

Trigger the new test directly from your IDE or run all tests by executing following Maven command:

```bash
mvn test
```

## Hints
<details>
  <summary>Show / Hide</summary>

- Configure the [Build Name Setter](http://wiki.jenkins.io/display/JENKINS/Build+Name+Setter+Plugin) plugin as a test dependency inside pom.xml
- As an alternative use a pipeline test setup setting _currentBuild.displayName_ directly
- Use the [Jenkins Test Harness](https://wiki.jenkins.io/display/JENKINS/Unit+Test) providing a [@JenkinsRule](https://javadoc.jenkins.io/component/jenkins-test-harness/org/jvnet/hudson/test/JenkinsRule.html) to setup the jobs
- Utilize [XPath](https://wiki.jenkins.io/display/JENKINS/Unit+Test#UnitTest-HTMLscraping) and [WebAssert](https://wiki.jenkins.io/display/JENKINS/Unit+Test#UnitTest-Webpageassertions) features to test the generated HTML
</details>
