# jpa01-cs111111


Deployed at: https://cs11111111.dokku-16.cs.ucsb.edu


# About this repo

This is a minimal "Hello World" type webapp built with Spring Boot.

# What can you do with this code?

| Command | What it does   |
|----------|---------------------------------------|
| `mvn compile` | Should result in a clean compile |
| `mvn test` | Runs JUnit tests on the code base |
| `mvn test jacoco:report` | Runs JUnit tests, and if all tests pass, computes code coverage.  The code coverage report (Jacoco) can be found in `target/site/jacoco/index.html` |
| `mvn test pitest:mutationCoverage` | Runs JUnit tests, and if all tests pass, runs pit (pitest.org) mutation testing to measure effectivness of test suite |
| `mvn package` | Builds the jar file `target/gs-spring-boot-0.1.0.jar` |
| `mvn spring-boot:run` | Runs the code to startup a web server.  Access it via `http://localhost:8080` on the *same machine* where the server is running.  Use CTRL/C to stop it. |
| `java -cp target/hello-1.0.0.jar edu.ucsb.cs156.spring.hello.Application` | If done after `mvn package`, runs the code to startup a web server.  |
| `java -jar target/hello-1.0.0.jar | If done after `mvn package`, this is another way to start up the web server.|


# Sources

The code in this repo is in support of
jpa01 for Fall 2024 for CMPSC 156.

The code in this repo is based in part on the tutorial here:
<https://spring.io/guides/gs/spring-boot/>, and the code here in the
`complete` directory of this repo
<https://github.com/spring-guides/gs-spring-boot.git>.  

That code has been
modified for use in UCSB CMPSC 156 as described
below.

# Modifications from the original

* Java 21 support
  * Converting `pom.xml` to use Java 21
* JUnit 5
  * Converting test code to use JUnit 5 instead of JUnit 4  
* Dokku Support
  * Ensuring that the `PORT` environment variable is
    used to define the port on which Spring Boot starts the web server 
* Testing and CI
  * Adding JUnit tests
  * Adding jacoco as a plugin to measure test 
    case coverage
  * Adding pitest for mutation test coverage.
 


