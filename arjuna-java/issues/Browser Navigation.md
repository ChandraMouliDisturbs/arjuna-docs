## goBack() is not working as expected.

Throwing a setu Error.

### TRACE
```java
log4j:WARN No appenders could be found for logger (org.apache.http.client.protocol.RequestAddCookies).
log4j:WARN Please initialize the log4j system properly.
log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: go_back() missing 1 required positional argument: 'url'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 279, in go_back
    browser.go_back()
TypeError: go_back() missing 1 required positional argument: 'url'

(BaseSetuObject.java:136)	-----------------------------------------------------
FAILED: test
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:92)
	at arjuna.lib.setu.guiauto.requester.component.GuiAutoComponentFactory$DefaultBrowser.goBack(GuiAutoComponentFactory.java:298)
	at com.testmile.arjuna_ex.BrowserNavigateURL.test(BrowserNavigateURL.java:17)
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

### Setu Log
```SystemVerilog
[DEBUG]	2019-05-01|14:39:15	(BasicRestClient.java:63)	----------------------------------------
[DEBUG]	2019-05-01|14:39:15	(BasicRestClient.java:58)	Executing POST request POST http://localhost:9000/setu HTTP/1.1
[DEBUG]	2019-05-01|14:39:15	(BasicRestClient.java:59)	{
  "action": "GUIAUTO_BROWSER_GO_BACK",
  "args": {
    "testSessionSetuId": "dce0c345-8982-4c4e-946a-5cd332ad7376",
    "automatorSetuId": "f1e380c7-e3af-4441-a23d-240ad26d32bd"
  }
}
[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:131)	Got Http Error: 500
[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:133)	Error: go_back() missing 1 required positional argument: 'url'
[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 279, in go_back
    browser.go_back()
TypeError: go_back() missing 1 required positional argument: 'url'

[ERROR]	2019-05-01|14:39:15	(BaseSetuObject.java:136)	-----------------------------------------------------

```

## goForward() is not working as expected.

Throwing a setu Error.

### TRACE
```java
log4j:WARN No appenders could be found for logger (org.apache.http.client.protocol.RequestAddCookies).
log4j:WARN Please initialize the log4j system properly.
log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: go_forward() missing 1 required positional argument: 'url'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 283, in go_forward
    browser.go_forward()
TypeError: go_forward() missing 1 required positional argument: 'url'

```

### Setu Log
```SystemVerilog
[DEBUG]	2019-05-01|14:49:42	(BasicRestClient.java:63)	----------------------------------------
[DEBUG]	2019-05-01|14:49:42	(BasicRestClient.java:58)	Executing POST request POST http://localhost:9000/setu HTTP/1.1
[DEBUG]	2019-05-01|14:49:42	(BasicRestClient.java:59)	{
  "action": "GUIAUTO_BROWSER_GO_FORWARD",
  "args": {
    "testSessionSetuId": "04709f8d-9611-4e41-a997-6519bf531871",
    "automatorSetuId": "61c723fe-3b62-4fc7-b93f-578d6931e765"
  }
}
[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:131)	Got Http Error: 500
[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:133)	Error: go_forward() missing 1 required positional argument: 'url'
[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 283, in go_forward
    browser.go_forward()
TypeError: go_forward() missing 1 required positional argument: 'url'

[ERROR]	2019-05-01|14:49:42	(BaseSetuObject.java:136)	-----------------------------------------------------

```

## refresh() is not working as expected.

Throwing a setu Error.

### TRACE
```java
log4j:WARN No appenders could be found for logger (org.apache.http.client.protocol.RequestAddCookies).
log4j:WARN Please initialize the log4j system properly.
log4j:WARN See http://logging.apache.org/log4j/1.2/faq.html#noconfig for more info.
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: type object 'BrowserHandler' has no attribute 'refresh'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
AttributeError: type object 'BrowserHandler' has no attribute 'refresh'

(BaseSetuObject.java:136)	-----------------------------------------------------
FAILED: test
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:92)
	at arjuna.lib.setu.guiauto.requester.component.GuiAutoComponentFactory$DefaultBrowser.refresh(GuiAutoComponentFactory.java:308)
	at com.testmile.arjuna_ex.BrowserNavigateURL.test(BrowserNavigateURL.java:20)
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

### Setu Log
```SystemVerilog
[DEBUG]	2019-05-01|14:51:33	(BasicRestClient.java:63)	----------------------------------------
[DEBUG]	2019-05-01|14:51:33	(BasicRestClient.java:58)	Executing POST request POST http://localhost:9000/setu HTTP/1.1
[DEBUG]	2019-05-01|14:51:33	(BasicRestClient.java:59)	{
  "action": "GUIAUTO_BROWSER_REFRESH",
  "args": {
    "testSessionSetuId": "2265036f-7d78-4f24-a3d8-cd6eab755550",
    "automatorSetuId": "07d73e7a-abe7-48b2-9a8f-3a10eb5e7941"
  }
}
[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:131)	Got Http Error: 500
[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:133)	Error: type object 'BrowserHandler' has no attribute 'refresh'
[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 135, in take_browser_action
    return handler.take_browser_action(action, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\guiauto\adapter\automator.py", line 89, in take_browser_action
    return getattr(BrowserHandler, action)(self.automator.browser, **json_dict)
AttributeError: type object 'BrowserHandler' has no attribute 'refresh'

[ERROR]	2019-05-01|14:51:33	(BaseSetuObject.java:136)	-----------------------------------------------------

```