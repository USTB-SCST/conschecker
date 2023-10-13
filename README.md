# How to use:

##### 1. Import  *conschecker-client-1.0.0.jar* and  *conschecker-common-1.0.0.jar* to your maven repository.

````bash
mvn install:install-file -Dfile=conschecker-common-1.0.0.jar -DgroupId=com.nanxing -DartifactId=conschecker-common -Dversion=1.0.0 -Dpackaging=jar
mvn install:install-file -Dfile=conschecker-client-1.0.0.jar -DgroupId=com.nanxing -DartifactId=conschecker-client -Dversion=1.0.0 -Dpackaging=jar
````

##### 2. Import  the *conschecker-client* dependency in your Spring Boot projects

````xml
<dependency>
    <groupId>com.nanxing</groupId>
    <artifactId>conschecker-client</artifactId>
    <version>1.0.0</version>
</dependency>
````

##### 3. Configure the following  items in the Spring Boot configuration file

````yaml
conschecker:
  scanPackage: com.example # Target package name for static scanning
  MBSName: example-MBS # The name of the MBS that this microservice belongs to
````

Then every time the microservice is started, the *conschecker-client* generates an MSDM model for the microservice.
