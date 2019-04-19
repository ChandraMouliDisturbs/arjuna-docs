# arjuna-java documentation
Docs for Arjuna java Client
### Getting Started with Arjuna Java Client
#### Prerequisities
Setup the Arjuna Framework service as per the instructions as per the given link.
[Getting Started with Arjuna Frame work service](arjuna-python#getting-started-with-arjuna-frame-work-service)

Install the following artifacts
* Java 1.8
* Github Desktop or Git Bash 
* Eclipse Oxygen IDE.
Clone the arjuna-java Source repo to a desired directory.

As a suggestion, don't clone inside a directory whose name is already arjuna.

`<arjuna_java_repo_root>` refers to the directory contains the arjuna-java repo. 

###### Command to clone arjuna repo
`git clone https://github.com/test-mile/arjuna-java.git`

##### For Eclipse IDE

###### Create a workspace

Switch to Workspace by choosing `arjuna_java_repo_root` directory.

###### Import projecst to IDE
Goto File Menu Select Import Projects.
Select Maven and Exisiting Maven Projects fromt he Import wizard.
Click on Browse Select the `<arjuna_java_repo_root>` directory and click on OK.
Select the two maven projects It not checked by default and click on Finish.

###### Install Java Client jar

Right click on the `arjuna-java` project, select Run As Maven install.
If the following error message is prompted

`No compiler is provided in this environment. Perhaps you are running on a JRE rather than a JDK?`

In the project Build Path, Update the Jdk Library to the installed jdk.

The following console log will be prompted
```
[INFO] --- maven-install-plugin:2.4:install (default-install) @ arjuna-java ---
[INFO] Installing G:\__work__\tm\3pview\jarjuna-ws\arjuna-java\arjuna-java\target\arjuna-java-0.1.0-alpha-SNAPSHOT.jar to C:\Users\Test\.m2\repository\com\testmile\arjuna-java\0.1.0-alpha-SNAPSHOT\arjuna-java-0.1.0-alpha-SNAPSHOT.jar
[INFO] Installing G:\__work__\tm\3pview\jarjuna-ws\arjuna-java\arjuna-java\pom.xml to C:\Users\Test\.m2\repository\com\testmile\arjuna-java\0.1.0-alpha-SNAPSHOT\arjuna-java-0.1.0-alpha-SNAPSHOT.pom
[INFO] Installing G:\__work__\tm\3pview\jarjuna-ws\arjuna-java\arjuna-java\target\arjuna-java-0.1.0-alpha-SNAPSHOT-sources.jar to C:\Users\Test\.m2\repository\com\testmile\arjuna-java\0.1.0-alpha-SNAPSHOT\arjuna-java-0.1.0-alpha-SNAPSHOT-sources.jar
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
```
 ###### Setup arjuna-java-examples project.

Right click on the `arjuna-java-examples` project, Select Maven and Update the Project.
Place your driver executables under `<arjuna_java_repo_root>`\arjuna-java\arjuna-java-examples\guiauto\drivers\<host_os> directory

Make sure you triggered launch-setu command in a seperate terminal before running java client code.
Run the following class as a Java Application from eclipse.

arjex.s01config.Basic1WithCentralTestContext.


