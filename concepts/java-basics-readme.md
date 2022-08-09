# Java basics
### WAR, JAR & EAR file formats
These files are simply zipped files using the java jar tool. These files are created for different purposes.
* **<ins>JAR - Java ARchive</ins>**: The .jar files contain libraries, resources and accessories files like property files.
* **<ins>WAR - Web application ARchive**</ins>: The war file contains the web application that can be deployed on any servlet/jsp container. The .war file contains <ins>jsp, html, javascript and other files necessary</ins> for the development of web applications.
* **<ins>EAR - Enterprise application ARchive**</ins>: It is used for packaging one or more modules into a single archive so that the deployment of the various modules onto an application server happens simultaneously and coherently.

![alt txt](/images/ear-war-jar-consolidated.jpg)

![alt txt](/images/Difference-Between-JAR-WAR-and-EAR-Comparison-Summary.jpg)

### Java Beans
JavaBean is regular Java class which follows certain conventions:
1. All properties are private (use getters/setters)
2. A public no-argument constructor  (so it can be created at will and configured by setting its properties)
3. Implements [Serializable](https://docs.oracle.com/javase/8/docs/api/java/io/Serializable.html). serializable objects can be written to streams.

## EJB - Jakarta Enterprise Beans (formerly Enterprise JavaBeans)
### History
By 1996, Java had already become popular among developer for its friendly APIs and automated Garbage Collection and was starting to be widely used in back-end systems. One problem, however, was that most of these systems needed the same set of standard capabilities – such as persistence, transaction integrity, and concurrency control – which the JDK lacked at that time. That, naturally, led to many home-grown, closed implementations.

IBM stepped forward and released the Enterprise Java Bean (EJB) specification in 1997, with the promise that developers could write code in a standard way, with many of the common concerns automatically handled.

That’s how the first Java framework for the enterprise was born; the specification was later adopted by Sun in 1999 as EJB 1.0.

### Overview & Architecture
[EJB](https://en.wikipedia.org/wiki/Jakarta_Enterprise_Beans) is a server-side software component that encapsulates business logic of an application. An EJB web container provides a runtime environment for web related software components, including computer security, Java servlet lifecycle management, transaction processing, and other web services. The EJB specification is a subset of the Java EE specification.

![alt txt](/images/JavaEE-serverAndContainers.gif)

Refer [What are EJBs Enterprise Java Beans? - Youtube](https://www.youtube.com/watch?v=utANrHfAh28) & [Enterprise Java Beans - Introduction](https://www.youtube.com/watch?v=3YwSY8joz20)

1. Application Server - In the EJB architecture, the Application server is the outermost layer that holds or contains the Container to be deployed. The application layer provides the necessary environment to execute the application developed using the beans. Popular application servers are Web-logic, Tomcat, JBoss, Web-sphere, Wildfly, and Glass-finish. The main tasks of the application server are:
    * Manage Interfaces
    * Execution of the processes
    * Connecting to the database
    * Manage other resources.

2. Container - In EJB architecture, the Container is the second outermost layer. For the enterprise bean, the Container provides support for the following:
    * transactional services such as registering the objects, assign remote interfaces, purge the instances.
    * monitoring the object's activities and coordinating distributed components.
    * security services.
    * the pooling of resources.
    * managing the Life-cycle of beans and their concurrency.
    * business logic of the application

3. Beans - Java beans of the enterprise are installed in the Container in the same way as a Plain old java object (POJO) is installed and registered to the Container. For developing secured, large scale and robust business applications, beans provide business logic.
    * Packaging the Enterprise beans (EB) within the web application's [WAR](https://en.wikipedia.org/wiki/WAR_(file_format)) module simplifies deployment and application organization. 
    * EB may be packaged within a WAR module as Java programming language class files or within a [JAR](https://en.wikipedia.org/wiki/JAR_(file_format)) file that is bundled within the WAR module. 
    * A [servlet](https://en.wikipedia.org/wiki/Jakarta_Servlet) or JSP page handles the web front-end, and the application is packaged into a WAR module as a Java programming class file.
    * The EJB in the WAR file can have its own deployment descriptor, ejb-jar.xml, if required.

### Types of EJB
1. Session beans - It could be Stateless, Stateful or Singleton. Support asynchronous execution.
2. Message-driven beans (MDB) - asynchronous in nature, implements the JMS specification

## JMS 
Java Message Service is a Java API that allows applications to create, send, receive, and read messages. Refer [JMS API](https://docs.oracle.com/javaee/5/tutorial/doc/bncdr.html)

![alt txt](/images/jms-architecture.jpg)

## N-Layer architecture - Java

![alt txt](/images/java-n-layer-architecture.jpg)

## Server comparison

| Feature | Apache HTTP Server (AHS) | Tomcat | Weblogic | JBOSS | Websphere | IIS |
| :- | :- | :- | :- | :- | :- | :- |
| Owner | Apache | Apache | Oracle | RedHat | IBM | Microsoft |
| Server type | Web Server | App Server | App Server | App Server | App Server | App Server |
| Definition | AHS serves static files such as text, HTML, images, audio and video files to web-based clients| Tomcat is a web container that runs the web applications based on servlet and JavaServer pages.| Java Application server which provides a range of services like- Http service, session handling, etc |Now known as Wildfly. JBoss is free and open-source J2EE application server. Red Hat charges to provide a support subscription. | Web application server, specifically, it is a software framework and middleware that hosts Java-based web applications | IIS is used to host ASP.NET web applications and static websites on Windows. It can also be used as an FTP server |

## Java .Net Analogy

| .Net | Java |
| :- | :- |
| ASP (Active Server Pages) | JSP (Java Server Pages) |
| ASP.Net | Servelet |
| Spring MVC | ASP.Net MVC |
| Spring Boot | .Net (previously .Net Core) |


![alt txt](/images/java-.net-analogy.jpg)