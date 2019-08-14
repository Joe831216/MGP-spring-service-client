# VMAMV
The VMAMV is a tool for monitoring microservice systems, generating visualized version-based service dependency graphs, and 
providing graph search services. The proposed scheme is called Version-based Microservice Analysis, Monitoring, and 
Visualization (VMAMV). This system automatically detects potential design problems and service anomalies and immediately 
notifies users of problems before or shortly after they occur.
# vmamv-springboot-service-client
The VMAMV system consists of [VMAMVS (vmamv-service)](https://github.com/Joe831216/vmamv-service) and client-side libraries.
The vmamv-springboot-service-client is the monitored [springboot](https://spring.io/projects/spring-boot)-service-side library 
of VMAMV.
# How to use?
## Dependencies
There are some dependencise need to be installed in the monitored service, 
please refer to the example [pom.xml](https://github.com/Joe831216/cinema-catalog/blob/master/pom.xml) file.
## Steps
1. Using the the `@EnableVmamvClient` Annotation on your "application class".
2. Configure the following properties:  
`spring.application.name`  
`info.version`  
`server.port`  
`mgp.system.name`  
`logging.level.org.zalando.logbook=TRACE`
3. Mark the additional information by using Annotaions. 
(To learn how to do, please read the [Mark the Information](https://github.com/Joe831216/vmamv-springboot-service-client/) section)
4. Using `ServiceDependencyAnalyzer` to automatically generate the OAS file extension for SpringFox.
## Mark the Information
