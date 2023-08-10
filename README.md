# secure-api-gateway-parent  

This project contains a maven project object model file (POM file) for use by all ForgeRock Java Secure API Gateway projects.

## Dependency Management

The parent pom manages the following dependency version in the dependencyManagement section:

- Spring Boot artifacts via the import of the spring-boot bom file
- Other 3rd party dependencies
- Test dependencies

## Defines the Java version for the project

The parent pom uses the `pluginManagement` section of the pom to specify the configuration for the `maven-compiler-plugin`. Via this mechanism child projects will inherit those settings. For this reason it is important to have your development machine set up to be using a JDK version that matches what is defined in this plugin configuration. Currently this is Java 14.

The ForgeRock development team use OpenJDK 14. 

## Distribution Management 

The parent pom specifies the repositories into which artifacts should be built. Child Open Banking projects should not need to override these settings 



