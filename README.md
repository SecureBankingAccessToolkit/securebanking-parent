# securebanking-parent  

This project contains a maven project object model file (POM file) for use by all ForgeRock Java Secure Banking projects.

## Dependency Management

The parent pom manages the following dependency version in the dependencyManagement section:

- Secure Banking artifiacts via the import of the securebanking-bom's pom file
- Spring Boot artifacts via the import of the spring-boot bom file
- Other 3rd party dependencies
- Test depenencies

## Defines the Java version for the project

The parent pom specifics the version of java used by the maven-complier-plugin, and also the compiler source version and target versions. 


### maven-compiler-plugin configuration ** Important **
In order to ensure that the project compiles nicely on all developer workstations the maven-compiler-plugin specifies the location of the javac compiler to use. This is simpler than configuring all workspaces etc to use the correct compiler version. To configure the project to use a specific javac compiler on your system you need to define a property in your maven settings.xml file. It should look something like this;

```
<settings>
  [...]
  <profiles>
    [...]
    <profile>
      <id>compiler</id>
        <properties>
          <JAVA_1_14_HOME>C:\Program Files\Java\j2sdk1.4.2_09</JAVA_1_14_HOME>
        </properties>
    </profile>
  </profiles>
  [...]
  <activeProfiles>
    <activeProfile>compiler</activeProfile>
  </activeProfiles>
</settings>

```

For further information see [here]([https://maven.apache.org/plugins/maven-compiler-plugin/examples/compile-using-different-jdk.html)

## Distribution Management 

The parent pom specifies the repositories into which artifacts should be built. Child Open Banking projects should
not need to override these settings 



