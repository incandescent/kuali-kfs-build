Kuali KFS Maven bootstrap build wrapper
=======================================

This is a small project that helps bootstrap KFS into Maven.  The provided Ant `build.xml` checks out KFS source, downloads the binary Tomcat dependency, and builds KFS war and jar artifacts.  These artifacts can then be *installed* or *deployed* via Maven so that the KFS war and code are available to other Maven projects (not the least of which would be a KFS war wrapper, see https://github.com/incandescent/incandescent-kfs).

To build the KFS war and jar:

    ant

To build & install the KFS war and jar into your local Maven repo (`~/.m2/repo`):

    ant mvn-install

