# Extensions

Extensibility in Jenkins, for core internals as well as for plugins, is accomplished by definitions of extension points. In general an extension point is an interface or abstract class that defines a contract of what needs to be implemented by contributing classes.

There a mainly two concepts of [Descriptors and Describables](https://jenkins.io/doc/developer/extensibility/#descriptors-and-describables) and [Actionable and Actions](https://jenkins.io/doc/developer/extensibility/#actionable-and-actions) in order to create new or extend other extension points.

The bulk work in developing plugin consists in implementing those extension points. Whenever a plugin implements such extension points by annotating the class with an _@Extension_ mark, Jenkins automatically detects, creates instances and attaches them to the according extension point instance.

## Example Extension

The implementation of the _BuildStepDescriptor_ below registers a new build step called _SampleBuilder_ by marking the _Descriptor_ class with the _@Extension_ annotation.

```java
@Extension
public static class Descriptor extends BuildStepDescriptor<Builder> {

    @Override
    public String getDisplayName() {
        return "SampleBuilder";
    }
}
```

## Further Reading

The full list of all available extensions can be found in the [Extensions Index](https://jenkins.io/doc/developer/extensions/).

For further information regarding extending Jenkins in general see [Extensibility](https://jenkins.io/doc/developer/extensibility/).
