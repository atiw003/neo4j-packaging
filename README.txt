Neo4j component packaging example.

Use this template to package Neo4j components together by
adding dependencies to the components you want to include.
(And remove the ones you don't want to be included.)
Then execute
   mvn package
in the root of the project.
This will produce .tar.gz and .zip packages in the
target/ directory, containing:
bin/   example start scripts for programs
docs/  aggregated javadocs for all included (Neo4j) components
lib/   all dependency jars (and a dummy packaging-example jar)
src/   example dummy program

If you need to include a component that depends on Java 6,
modify the maven-compiler-plugin configuration in the
pom.xml file accordingly.

If you want Javadocs to be generated for non-Neo4j components
as well, add their groupId to the comma separated list in the
includeGroupIds element in the maven-dependency-plugin configuration.
(See an example of this in the pom.xml file.)
