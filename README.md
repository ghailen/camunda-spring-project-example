# Camunda Platform Process Application

We Have here 3 classes existed in the package :

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/0ba8f43b-d772-4a6f-b55e-d67552674af0)

CamundaBpmProcessApplication : process the application exposing this applciation's resources to process engine.

LoggerDelegate : will help when creating a service task, will show the different information , it implement JavaDelegate Interface

ProcessConstants : contains the name of the project


A Process Application for [Camunda Platform](http://docs.camunda.org).

This project has been generated by the Maven archetype
[camunda-archetype-servlet-war-7.16.0](https://docs.camunda.org/manual/latest/user-guide/process-applications/maven-archetypes/).

## Show me the important parts!
[BPMN Process](src/main/resources/process.bpmn)

## How does it work?

## How to use it?

### Unit Test
You can run the JUnit test [ProcessTest](src/test/java/org/ghailene/ProcessTest.java) in your IDE or using:

```bash
mvn clean test
```

### Deployment to an Application Server
You can also build and deploy the process application to an application server.
For an easy start you can download Apache Tomcat with a pre-installed Camunda
from our [Download Page](https://camunda.com/download/).

#### Manually
1. Build the application using:

```bash
mvn clean package
```
2. Copy the *.war file from the `target` directory to the deployment directory
of your application server e.g. `tomcat/webapps` or `wildfly/standalone/deployments`.
For a faster 1-click (re-)deployment see the alternatives below.

#### Apache Tomcat (using Tomcat Maven Plugin)
1. Create a user in Tomcat with the role `manager-script`.
2. Add the user's credentials to the `tomcat7-maven-plugin` configuration in the [pom.xml](pom.xml) file.
3. Build and deploy the process application using:

```bash
mvn clean tomcat7:deploy
```

#### Wildfly (using Wildfly Maven Plugin)
1. Build and deploy the process application using:

```bash
mvn clean wildfly:deploy
```

#### JBoss AS7 (using JBoss AS Maven Plugin)
1. Build and deploy the process application using:
```bash
mvn clean jboss-as:deploy
```

### Run and Inspect with Tasklist and Cockpit
Once you deployed the application you can run it using
[Camunda Tasklist](http://docs.camunda.org/latest/guides/user-guide/#tasklist)
and inspect it using
[Camunda Cockpit](http://docs.camunda.org/latest/guides/user-guide/#cockpit).

## Environment Restrictions
Built and tested against Camunda Platform version 7.16.0.

## Known Limitations

## License
[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0).

<!-- Tweet
New @Camunda example: Camunda Platform Process Application - A Process Application for [Camunda Platform](http://docs.camunda.org). https://github.com/camunda-consulting/code/tree/master/snippets/camunda-spring-servlet-war-project-example
-->
