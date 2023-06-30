# Camunda Platform Process Application

==================Main classes descitpion ============

We Have here 3 classes existed in the package :

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/0ba8f43b-d772-4a6f-b55e-d67552674af0)

CamundaBpmProcessApplication : process the application exposing this applciation's resources to process engine.

LoggerDelegate : will help when creating a service task, will show the different information , it implement JavaDelegate Interface

ProcessConstants : contains PROCESS_DEFINITION_KEY (by default the name of the project if not changed)

now lets modify the process.bpmn file by adding two user tasks:

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/95cdaac2-06b3-4e90-8eb1-15c5307ced92)


the process_definition_key in processconstants class must be the same in the bpmn id process


===========Unit test==========

For now we can ignore unit tests : 

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/425ead5e-ac52-42a0-a54b-ee5a45918a32)


=========Camunda config files============

as we can see here we have :

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/95c2b9a4-2808-4ca8-b598-07e6230547df)

The camunda.cfg.xml contains the configuration , we can see the list of plugin, we can developp our proper plugin and add it to the list.


==========Forms==============

we can create a custom form also 

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/c4849bcf-3860-488b-b368-4a3dae615162)

==========Clean Install ==============

mvn clean 

mvn install 

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/a2338f35-8095-42ef-9129-31f773b37b30)

a war will be generated.

=============Deployement==========
now lets deploy the generated war in wildfly server:

we can found the camunda provided app and dependancies like webapp,api-rest....

the path is : camunda-bpm-wildfly-7.18.0\server\wildfly-26.0.1.Final\standalone\deployments

lets copy our generated war in the deployement folder:

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/bc0d0014-82b7-475a-9c10-fe7e6b3409ac)

=============Open wildfly server===========

go to cockpit , deployement:

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/1d306dea-09e8-4a14-bdfe-96375358c5ea)

our deployement is here :

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/73faa721-0ac1-4cd9-adda-7d9dcba7ea6e)

lets execute it via tasklist module:

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/078d4378-7ca7-496b-8554-9d7fd1f49a53)

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/62f8272c-688d-40c6-80ee-d003bee862b9)

the user task is appeared here we can claim it and complete it:

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/0be08bec-3b81-4ab8-91dd-9c228abbf547)

In the cockpit we can see the new instance of the process: 

![image](https://github.com/ghailen/camunda-spring-project-example/assets/36199753/a06093bb-8222-4184-8bc2-442c1336a278)





