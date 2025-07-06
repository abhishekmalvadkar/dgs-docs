## TDD 1 : Setup new API container for DGS

Github Issue: [GH-4](https://github.com/abhishekmalvadkar/dgs-docs/issues/4)

### Problem Context

We need to create new spring boot application which will act as API container i.e  
it will have our all functionalities of DGS system.

### Steps to create spring boot application for DGS API container

* Go to [Spring Initializr](https://start.spring.io/)
* Select Maven
* Select latest stable spring boot version (3.5.3)
* Fill project metadata like below
  * **Group**: com.amalvadkar
  * **Artifact**: dgs-service-api
  * **Name**: dgs-service-api
  * **Description**: DGS API Container
  * **Package name**: com.amalvadkar.dgs
  * **Packaging**: Jar
  * **Java**: Select latest LTS version (21)
* Select below dependencies 
  * Spring Web
  * Spring Data JPA
  * MySQL Driver
  * Liquibase Migration
  * Lombok
  * Validation
  * Spring Boot DevTools
  * Spring Configuration Processor
  * Spring Boot Actuator
  * Testcontainers
* Generate and unzip
* Open in IntelliJ
* Create git repositories
* Share project on GitHub in public mode
* Mark GitHub ticket [GH-5](https://github.com/abhishekmalvadkar/dgs-docs/issues/5) as DONE

### Happy Coding :)