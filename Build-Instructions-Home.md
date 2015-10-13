#Build Instructions

Use the following guide to help you install and set up your instance of OWF.

* [Build Instructions](https://github.com/ozoneplatform/owf/wiki/OWF-7-Build-Instructions)   
* [Build Base](OWF-7-Build-Base)
* [Clustering an OWF Environment](OWF-7-Clustering-an-OWF-Environment)
* [Deploying OWF to an Existing Tomcat Instance](OWF-7-Deploy-OWF-in-Existing-Tomcat-Instance)
* [Allowing Remote Access to OWF](OWF-7-Allowing-Remote-Access-to-OWF)
* [Prior to OWF 6](OWF-7-Prior-to-OWF-6)
* [Known Issues](build-known-issues)


##Objectives
This document will describe how to build the following projects:

* **OWF Server**--A local copy of the bundled (`owf-server.war` + `cas-server.war` + `owf-samples` + Tomcat) ZIP file as well as the release version.
* **OZONE Security JAR**--A new version of the `ozone-security` JAR file. 

##Requirements
This document is targeted to widget developers and assumes a basic familiarity with the target development environment, be it Microsoft Windows or Linux. Before any of the build tasks can run, the developer must install Ant 1.7.1, Ant Contrib 1.0b3 and Grails 1.3.7. The following sections list the tools, the version requirements for recent OWF releases and nominal configuration elements. Instructions provided below assume a Microsoft Windows development environment for illustrative purposes only.   

##Download and Install Applications
OWF Development requires the use of the Java Development Kit (JDK), Apache Ant, Apache Ant Contrib, Ruby, RubyGems, Sass and Compass, as well as Groovy. The following table lists the versions of each tool required by the last few releases of OWF and the Store.

*The term Store and Marketplace can be used interchangeably.*

| Application  	| JDK	|ANT	| Ant Contrib	| Grails| Ruby	|Compass	|SASS*	| Groovy										|	
| -------------	| ------|-------|---------------| ------| ----- |---------	|-------|-----------									|	
| OWF 7.17.0	|1.8	|1.8.4	| 		-	 	|2.4.0	|1.9.2	|0.11.7		|3.1.3	|2.3.0 (included with Grails) (1.8.8 for OWF)	|


