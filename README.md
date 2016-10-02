### A Java Ecosystem Primer
Maybe you’ve read a blog post with some Java code, but it felt more like an academic paper than an understandable explanation. Sometimes Java doesn’t seem approachable for beginners, but maybe you’re still interested because it’s a building block language, or you’re interested in Mobile development or the robust library support for Machine Learning, or you’ve heard about the functional languages supported by the JVM. Java can be a tough ecosystem to break into. It’s very mature and there are often multiple frameworks and tools you can leverage to solve your problem. Here's an introduction to the ecosystem and give you just enough history so you know where to start.

#### How Does Java Work?
You may have heard write once run anywhere, here’s how that works. Write your code in a .java file, you run a tool called a compiler which outputs this file to Java bytecode, a .class file. Your Mac or Windows laptop has some software called the Java Virtual Machine (or JVM) and it can read bytecode and run your program. Lots of devices have a JVM and can run your code, but you only to write it once.

#### Some Acronyms
* JVM: can read Java Bytecode
* JRE: a package containing the JVM + the Java Class Library. It lets you run your application because it has all the basic Java libraries.
* JDK: contains things to develop applications: the JRE, the compiler, a utility for creating JARs, tools for decompiling class files, etc.
* JAR: a Java archive, it’s a library containing many .class files you can rely on like a gem or a package.

#### Integrated Development Environments (IDEs)
Here are the main 3 integrated development environments: Intellij IDEA, Eclipse, and NetBeans. They are rich with built in features like an integrated compiler, debugger, and code analysis tools.

#### Libraries
I want to write some code, but I don’t want to reinvent the wheel. When I said the Java ecosystem is mature, there are lots of libraries, tools and frameworks.

The Apache Software Foundation is a non-profit software foundation that creates open source software resources. You may recognize some of the projects under their Umbrella:
* Commons libraries
* Cassandra: a distributed database
* Hadoop: data processor
* HTTP Server: web Server
* Kafka: message broker
* Tomcat: web container

Google also publishes a lot of open source libraries. The Guava libraries specifically are like a second generation Apache collections.
* Guava (2nd generation Commons Libraries)
* Guice
* GSON
* Protobuf

#### Build & Dependency Management
You’ve written some code and now you’re ready to compile and package it. Your dependencies are the libraries your application depends on. Your build tool is going to compile your code, run your tests, package your class together in a JAR.

* Ant: Ant was released in 2000 as an xml based build tool similar to make for Java. Ivy usually handles the dependency management aspect.
* Maven: In 2002 before the release of Ivy, Maven came along to rival Ant. It is an XML based build and dependency management tool that relies heavily on convention. A few nice things introduced over the years in Maven are Archetypes which are essentially templates that automatically generate the scaffold for your application.
* Gradle: There’s always room for improvement, in 2012 Gradle 1.0 was launched. It follows Maven’s build by convention approach, and is based on it’s own DSL (domain specific language) written in Groovy which is another JVM language (which we’ll get to later). It’s compatible with Ant and Maven making migration easier. The features I appreciate the most are the ability to parallelize test execution and a daemon mode that reduces the startup overhead and in turn minimizing build execution time.

#### Dependency Repositories
Nexus and Artifactory are dependency repositories, if your .jars are books, it’s like the library. Or if you’re a Rubyist it’s like GemFury. Maven Central and Maven repository are both implementation of Nexus repositories hosted on the Web. Most companies will have an internal repository so when they build they can be sure they are getting the exact libraries their build tool declares.

#### Web frameworks
Java isn’t the first tool I’d necessarily use to create a complete web application, but here’s a list of popular web frameworks provided by a 2016 survey from the website zeroturnaround. They come out with a pretty good survey of trends in the Java community. Spring MVC tops the list, followed by JSF, Vaadin, and GWT.

#### Web Services
If you’re writing a set of microservices or Rest APIs, popular options are
* Spring Boot
* Dropwizard 

#### Other Languages on the JVM
Another cool thing about the JVM is that any language that can create bytecode can be run on the JVM.
* Kotlin (JetBrains)
* Scala
* Clojure (Lisp like)
* Groovy

JetBrains the maker of the IDE we talked about in the first slide created the Kotlin language. Groovy backs the Gradle build tool. Scala and Clojure are both functional languages with very different implementations.
