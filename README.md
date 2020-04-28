# Flowable  with Spring Boot 

## Java Lectures
[Article Medium:](https://medium.com/@anuragsidana22/implement-flowable-engine-using-java-e437061b6773)
[Video Tutorials:](https://www.youtube.com/playlist?list=PLgkvQA5zy_iG_3PS0kSohWkmXE3Yxsqmi)
https://flowable.com/open-source/docs/userguide-5/index.html#configuration

## TOMCAT /Flowable 
* Flowable Admin*: an administrative application that allows users with admin privilege to query the BPMN, DMN, form and content engines and provides several options to change process instances, tasks, jobs and so on. The admin application connects to the engines through the REST API that is deployed together with the Flowable Task app and the Flowable REST app.


```
apps – By default looks for all files ending with .zip or .bar and deploys them
cases – By default looks for all files ending with .cmmn, .cmmn11, .cmmn.xml or .cmmn11.xml and deploys them
dmn – By default looks for all files ending with .dmn, .dmn11, .dmn.xml or .dmn12.xml and deploys them
forms – By default looks for all files ending with .form and deployes them
processes – By default looks for all files ending with .bpmn20.xml or .bpmn
```

```
The REST Servlets are also available under:

process-api for the Process Engine
cmmn-api for the CMMN Engine
dmn-api for the DMN Engine
idm-api for the IDM Engine
form-api for the Form Engine
content-api for the Content Engine
```
Flowable OpenAPI (Swagger) docs

## Doc  Urls
- https://www.youtube.com/watch?v=SeKdgWtEpCE   //Simple Manual Flow in Flowable BPMN
- Intro to  Archimate  :  https://youtu.be/ULl9lf0OZco
- https://www.soscisurvey.de/tools/view-chars.php
-https://www.goodelearning.com/downloads/
- https://www.goodelearning.com/downloads/enterprise-architecture/togaf-poster-5-building-blocks
- https://paulhh.wordpress.com/flowable-blogs/
- https://youtu.be/U0kWRbaw92I
- https://github.com/flowable/flowable-examples/tree/master/spring-boot-example
- https://flowable.com/open-source/docs/bpmn/ch14-Applications/#flowable-applications
- https://paulhh.wordpress.com/2017/01/31/flowable-6-instant-gratification/
- https://flowable.com/open-source/downloads/
- https://flowable.com/open-source/docs/bpmn/ch05a-Spring-Boot/
- https://robferguson.org/blog/2018/12/24/flowable-rest-api-part-1/
- https://www.baeldung.com/flowable
- https://blog.flowable.org/2018/12/19/building-your-own-flowable-spring-boot-application/
- https://blog.ippon.fr/2018/01/04/gestion-des-processus-metiers-embarquer-un-moteur-bpm-dans-votre-application-jhipster/

##  Run

```
mvn  spring-boot:run
```

##  Tomcat
*add  application.properties  in  TOMACAT-HOME/lib

```
spring.datasource.driver-class-name=com.mysql.jdbc.Driver
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/flowable?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false&characterEncoding=UTF-8
spring.datasource.username=flowable
spring.datasource.password=flowable
```


##  User Management

* http://<host-ip>:8080/flowable-idm 
* http://localhost:8080/flowable-idm 
# Create Workflow

 *  http://localhost:8080/flowable-admin   (compte :  admin /test)
 
 * Navigate to http://localhost:8080/flowable-modeler  and sign in using the default user id: admin and password: test
 

 * http://localhost:8080/flowable-task
 
##  REST API:

* Process API Endpoint configuration :http://localhost:8080/flowable-task/process-api
* Content API Endpoint configuration:  http://localhost:8080/flowable-task/content-api
* CMMN API Endpoint configuration :  http://localhost:8080/flowable-task/cmmn-api

* DMN API Endpoint configuration : http://localhost:8080/flowable-task/dmn-api
* Form API Endpoint configuration :           http://localhost:8080/flowable-task/form-api
* App API Endpoint configuration :              http://localhost:8080/flowable-task/app-api
