### to build project via Maven
mvn -pl +admin,+web clean install

### to run test via Maven
mvn -pl +admin,+web clean test


#### Maven

The Maven WAR plugin is responsible for collecting and compiling all the dependencies, 
classes, and resources of the web application into a web application archive.
war: This is the default goal that is invoked during the packaging phase of the project. 
It builds a WAR file if the packaging type is war.

#### Inclusion and exclusion

Using --projects you can specify which modules to build.
You can do this by specifying a comma-delimited list of project selectors. 
A project selector is a string that is composed of the groupId:artifactId, only :artifactId or the relative path to a module.

A module can be selected (default), or excluded from the build. 
You exclude a module by prefixing the selector with a ! or -.
To explicitly select a module, prefix it with a +.

mvn -pl +admin,+web clean install
