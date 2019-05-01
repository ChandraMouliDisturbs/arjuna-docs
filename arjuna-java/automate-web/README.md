### Prerequisites

Place your driver [Driver executables](../#driver-executables)

Initialsing Arjuna is a prerequisite to start automation with Arjuna. There are two possible ways to do this
1. Handing the Arjuna `init()` to `arjuna.tpi.testng.TestNGBaseTest` by inherting it.
2. Call the `Arjuna.init()` at the your custom place(fixture or the test).

#### Launching browser with explicit Arjuna init

```java

import org.testng.annotations.Test;

import arjuna.tpi.Arjuna;
import arjuna.tpi.guiauto.GuiAutomator;

public class LaunchBrowser1 {

    @Test
	public void test() throws Exception{
        Arjuna.init();
        GuiAutomator automator = Arjuna.createGuiAutomator();
    }
}
    
```


#### Launching browser with implict Arjuna init

`TestNGBaseTest` class initializes Arjuna Before Suite.


```java
import org.testng.annotations.Test;

import arjuna.tpi.Arjuna;
import arjuna.tpi.guiauto.GuiAutomator;
import arjuna.tpi.testng.TestNGBaseTest;

public class LaunchBrowser2  extends TestNGBaseTest{

    @Test
	public void test() throws Exception{
        GuiAutomator automator = Arjuna.createGuiAutomator();
    }
}
    
```

#### Launching browser with implict Arjuna init

`TestNGBaseTest` class initializes Arjuna Before Suite.

```java
import org.testng.annotations.Test;

import arjuna.tpi.Arjuna;
import arjuna.tpi.guiauto.GuiAutomator;
import arjuna.tpi.testng.TestNGBaseTest;

public class LaunchBrowser2  extends TestNGBaseTest{

    @Test
	public void test() throws Exception{
        GuiAutomator automator = Arjuna.createGuiAutomator();
    }
}
    
```

#### Browser Navigation
Providing the data to test can be passed in multiple ways.
The following is one of it. Further we will see more ways to externalize the data.

*project.conf*
```
arjunaOptions {
	browser_name = chrome
	browser.maximize = true
	guiauto.max.wait=10
}

userOptions {
	wp.app.url = "http://104.198.233.154"
	wp.login.url = ${userOptions.wp.app.url}"/wp-admin"
	wp.logout.url = ${userOptions.wp.app.url}"/wp-login.php?action=logout"
}
```

```java
import org.testng.annotations.Test;

import arjuna.tpi.Arjuna;
import arjuna.tpi.guiauto.GuiAutomator;
import arjuna.tpi.testng.TestNGBaseTest;

public class BrowserNavigateURL  extends TestNGBaseTest{

    @Test
	public void test() throws Exception{
        GuiAutomator automator = Arjuna.createGuiAutomator();
        String loginURL = automator.getConfig().getUserOptionValue("wp.login.url").asString();
        automator.Browser().goToUrl("https://www.google.com");
        automator.Browser().goToUrl(loginURL);
        automator.Browser().goBack();
        automator.Browser().goForward();
        automator.Browser().refresh();
    }
}
```
