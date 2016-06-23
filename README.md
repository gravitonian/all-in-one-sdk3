# Alfresco All-In-One Project - SDK 3

This is a sample AIO project for the [Alfresco SDK 3.x PoC](https://github.com/Alfresco/alfresco-sdk/tree/sdk-3.0). To run this project, please clone the Alfresco SDK and install the `sdk-3.0` branch. Install with `mvn clean install -DskipTests=true`

Then clone this project and run with `mvn clean install -DskipTests=true alfresco:run` or `./run.sh` and verify that it 

 * Runs the embedded Tomcat+H2 DB (and Solr4)
 * Runs Alfresco Share
 * Packages both as JAR and AMP assembly for modules
 
# Few things to notice

 * No parent pom
 * No runner project - it's all in the Alfresco Maven Plugin
 * Standard JAR packaging and layout
 * Works seamlessly with Eclipse and IntelliJ IDEA
 * AMP as an assembly
 * [Configurable Run mojo](https://github.com/Alfresco/alfresco-sdk/blob/sdk-3.0/plugins/alfresco-maven-plugin/src/main/java/org/alfresco/maven/plugin/RunMojo.java) in the `alfresco-maven-plugin`
 * No unit testing/functional tests just yet
 * Resources loaded from META-INF
 * Web Fragment (this includes a sample servlet configured via web fragment)
 
# TODO
 
  * Abstract assembly into a dependency so we don't have to ship the assembly in the archetype
  * Create new, slim and simply parent pom to set sensible defaults and profiles
    * Purge, functional/remote unit tests
    * Ensure that all functionality still works even without parent pom
   
  
 