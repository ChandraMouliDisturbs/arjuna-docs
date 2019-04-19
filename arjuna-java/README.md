# arjuna-java documentation
Docs for Arjuna java Client
### Getting Started with Arjuna Java Client
#### Prerequisities
Setup the Arjuna Framework service as per the instructions as per the given link.
[Getting Started with Arjuna Frame work service](../arjuna-python#getting-started-with-arjuna-frame-work-service)

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

###### Install Java Client jar from Gihub Repo

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

###### Install Java Client from maven central

Include the following dependecy in your projects pom.xml

```
<dependency>
    <groupId>com.testmile</groupId>
    <artifactId>arjuna-java</artifactId>
    <version>0.1.0</version>
</dependency>

```

Creating a Test Project using Arjuna-java and testNG

* Create a Maven Project.
Add the following dependenciies to the pom.xml
```xml
<dependencies>
	<dependency>
		<groupId>com.testmile</groupId>
		<artifactId>arjuna-java</artifactId>
		<version><arjuna_latest_version></version>
	</dependency>
	<dependency>
		<groupId>org.testng</groupId>
		<artifactId>testng</artifactId>
		<version>6.14.3</version>
	</dependency>
	<dependency>
		<groupId>log4j</groupId>
		<artifactId>log4j</artifactId>
		<version>1.2.17</version>
	</dependency>
</dependencies>
```
* Create `config` directory under project root.
* Under config directory create a project.conf file.
Create two sections in it.
```
arjunaOptions {

}
userOptions {

}
```
* Place your selenium driver executable under `<project_dir>\guiauto\drivers\(linux|mac|windows)\driver_executable` Create the directory structure alike config.

For e.g., 
`<project-path>\guiauto\drivers\windows\chromedriver.exe`
`<project-path>\guiauto\drivers\windows\geckodriver.exe`

Writing a simple selenium test case using arjuna-java and testNG

```java
import org.testng.annotations.Test;
import org.testng.asserts.Assertion;

import arjuna.tpi.Arjuna;
import arjuna.tpi.guiauto.GuiAutomator;
import arjuna.tpi.testng.TestNGBaseTest;

@Test
public class SimpleTest extends TestNGBaseTest{
	
	public void test() throws Exception {
		GuiAutomator automator = Arjuna.createGuiAutomator();
		automator.Browser().goToUrl("https://www.google.com");
		String winTitle = automator.MainWindow().getTitle();
		Assertion assertion = new Assertion();
		assertion.assertEquals(winTitle, "Google", "Window Title Should match");
		automator.quit();
	}
}
```
Please find other styles of test writing in the belo Link

[Test Writing in arjuna-java ](test-writing)

In the above example chrome browser is launched. How do we launch other browsers?

There are mutiple to do this through configuration.

[Test configuration](test-configuration)


