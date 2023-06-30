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


