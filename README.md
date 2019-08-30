# Spring Boot
This repository brings Spring Boot projects.

# Setting up VScode
Install the following VScode extensions:

- Spring Boot Tools (Pivotal)
- Spring Initializr Java Support (Microsoft)
- Spring Dashboard (Microsoft)

# Creating Projects
Find the MAVEN PROJECTS view in the project explorer.
The plus (+) submenu of the view allows you to create Maven projects.
The 'marven-archetype-quickstart' creates a vanilla Maven project.
Edit pom.xml as follows:

~~~
<project ...>
   <parent>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-parent</artifactId>
      <version>2.1.7.RELEASE</version>
   </parent>
   <dependencies>
      <dependency>
         <groupId>org.springframework.boot</groupId>
         <artifactId>spring-boot-starter-web</artifactId>
      </dependency>
   </dependencies>
   <build>
      <plugins>
         <plugin>
	         <groupId>org.springframework.boot</groupId>
	         <artifactId>spring-boot-maven-plugin</artifactId>
         </plugin>
      </plugins>
      <pluginManagement>
         some plugins specified by Marven
      </pluginManagement>
   </build>
</project>
~~~

The plugin 'spring-boot-maven-plugin' is required to create an executable jar.

See: https://docs.spring.io/spring-boot/docs/2.1.7.RELEASE/reference/html/getting-started-first-application.html

# Compile, Package and Run

You can compile your Spring Boot application by Maven:

~~~
$ mvn package
~~~

Thanks to pring-boot-maven-plugin specified in pom.xml, the package phrase creates a completely self-contained executable jar file that we could run.

Run you application in either way:

~~~
$ java -jar path-to-executable.jar
OR
$ mvn spring-boot:run
~~~