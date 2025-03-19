This is a plugin for the Rascal tutor compiler. 
We inject this dependency later to allow for the rascal project
to ignore the depedendency on selenium that this screenshot feature
has. Also the (dynamic) dependencies on Chrome and ChromeDriver are
encapsulated by the current module.

The rascal-maven-plugin project makes sure that the current plugin
is loaded when the tutor compiler is executed by it. Other tools
that wish to enable the screenshot feature of the tutor should
simply add the current project to their classpath.

The current project shades all dependencies such that the above
activation of the screenshot feature remains easy and simple.
