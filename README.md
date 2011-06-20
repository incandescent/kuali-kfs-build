Kuali KFS Maven bootstrap build wrapper
=======================================

This is a small project that helps bootstrap KFS into Maven.  The provided Ant `build.xml` checks out KFS source, downloads the binary Tomcat dependency, and builds KFS war and jar artifacts.  These artifacts can then be *installed* or *deployed* via Maven so that the KFS war and code are available to other Maven projects (not the least of which would be a KFS war wrapper, see https://github.com/incandescent/incandescent-kfs).

To build the KFS war and jar:

    ant

To build & install the KFS war and jar into your local Maven repo (`~/.m2/repo`):

    ant mvn-install

**NOTE:** You should *not* have to edit `generic-kfs-build.properties`.  The idea here is that there is one *generic* KFS binary war which can subsequently be customized via the Maven [war overlay](http://maven.apache.org/plugins/maven-war-plugin/overlays.html) process.  See https://github.com/incandescent/incandescent-kfs for an example.
