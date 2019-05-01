
### In the absence of Arjuna.init(), If somebody tries to createAutomator(), A `NullPointerException` is thrown.

Instead of throwing `NullPointerException`. A Useful Information to resolve the missing Arjuan.init() is missing should be provided

### TRACE:
```java
java.lang.NullPointerException
	at arjuna.lib.setu.guiauto.requester.automator.AbstractAppAutomator.<init>(AbstractAppAutomator.java:60)
	at arjuna.lib.setu.guiauto.requester.automator.DefaultGuiAutomator.<init>(DefaultGuiAutomator.java:34)
	at arjuna.lib.state.ArjunaSingleton.createGuiAutomator(ArjunaSingleton.java:120)
	at arjuna.tpi.Arjuna.createGuiAutomator(Arjuna.java:65)
	at com.testmile.arjuna_ex.LaunchBrowser1.test(LaunchBrowser1.java:12)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at org.testng.internal.MethodInvocationHelper.invokeMethod(MethodInvocationHelper.java:124)
	at org.testng.internal.Invoker.invokeMethod(Invoker.java:583)
	at org.testng.internal.Invoker.invokeTestMethod(Invoker.java:719)
	at org.testng.internal.Invoker.invokeTestMethods(Invoker.java:989)
	at org.testng.internal.TestMethodWorker.invokeTestMethods(TestMethodWorker.java:125)
	at org.testng.internal.TestMethodWorker.run(TestMethodWorker.java:109)
	at org.testng.TestRunner.privateRun(TestRunner.java:648)
	at org.testng.TestRunner.run(TestRunner.java:505)
	at org.testng.SuiteRunner.runTest(SuiteRunner.java:455)
	at org.testng.SuiteRunner.runSequentially(SuiteRunner.java:450)
	at org.testng.SuiteRunner.privateRun(SuiteRunner.java:415)
	at org.testng.SuiteRunner.run(SuiteRunner.java:364)
	at org.testng.SuiteRunnerWorker.runSuite(SuiteRunnerWorker.java:52)
	at org.testng.SuiteRunnerWorker.run(SuiteRunnerWorker.java:84)
	at org.testng.TestNG.runSuitesSequentially(TestNG.java:1208)
	at org.testng.TestNG.runSuitesLocally(TestNG.java:1137)
	at org.testng.TestNG.runSuites(TestNG.java:1049)
	at org.testng.TestNG.run(TestNG.java:1017)
	at org.testng.remote.AbstractRemoteTestNG.run(AbstractRemoteTestNG.java:114)
	at org.testng.remote.RemoteTestNG.initAndRun(RemoteTestNG.java:251)
	at org.testng.remote.RemoteTestNG.main(RemoteTestNG.java:77)
```


### SetuId for Browser Object is null
automator.Browser().getSetuId() is returning null

automator.getAutomationContext() is returning null