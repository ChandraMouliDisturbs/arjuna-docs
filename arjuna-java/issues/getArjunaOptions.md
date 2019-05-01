## Key Error while fetching ArjunaOptions from `TestConfig` object
* ROOT_DIR
* TOOLS_DIR
* APPS_DIR
* PROJECT_CONF_DIR
* GUIAUTO_AUTOMATOR_NAME
* BROWSER_HEADLESS_MODE
* BROWSER_PROXY_HOST
* BROWSER_PROXY_PORT
* APP_URL
* BROWSER_HEADLESS_MODE
* BROWSER_HEADLESS_MODE
* BROWSER_PROXY_HOST
* BROWSER_PROXY_PORT
* APP_URL
* GUIAUTO_SCROLL_PIXELS
* GUIAUTO_SWIPE_TOP
* GUIAUTO_SWIPE_BOTTOM
* GUIAUTO_SWIPE_MAX_WAIT
* MOBILE_APP_PACKAGE
* MOBILE_APP_ACTIVITY

Following are the error logs/trace

```java
ROOT_DIR(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'ROOT_DIR'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'ROOT_DIR'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.

TOOLS_DIR	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'TOOLS_DIR'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'TOOLS_DIR'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

APPS_DIR(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'APPS_DIR'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'APPS_DIR'

(BaseSetuObject.java:136)	-----------------------------------------------------

PROJECT_CONF_DIRarjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'PROJECT_CONF_DIR'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'PROJECT_CONF_DIR'

(BaseSetuObject.java:136)	-----------------------------------------------------

GUIAUTO_AUTOMATOR_NAMEarjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'GUIAUTO_AUTOMATOR_NAME'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'GUIAUTO_AUTOMATOR_NAME'

(BaseSetuObject.java:136)	-----------------------------------------------------

BROWSER_HEADLESS_MODEarjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'BROWSER_HEADLESS_MODE'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'BROWSER_HEADLESS_MODE'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

BROWSER_PROXY_HOST(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'BROWSER_PROXY_HOST'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'BROWSER_PROXY_HOST'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

BROWSER_PROXY_PORT(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'BROWSER_PROXY_PORT'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'BROWSER_PROXY_PORT'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

APP_URL	at org.testng.SuiteRunner.privateRun(SuiteRunner.java:415)
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
(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'APP_URL'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'APP_URL'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

GUIAUTO_SCROLL_PIXELS(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'GUIAUTO_SCROLL_PIXELS'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'GUIAUTO_SCROLL_PIXELS'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

GUIAUTO_SWIPE_TOP(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'GUIAUTO_SWIPE_TOP'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'GUIAUTO_SWIPE_TOP'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

GUIAUTO_SWIPE_BOTTOM(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'GUIAUTO_SWIPE_BOTTOM'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'GUIAUTO_SWIPE_BOTTOM'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

GUIAUTO_SWIPE_MAX_WAIT(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'GUIAUTO_SWIPE_MAX_WAIT'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'GUIAUTO_SWIPE_MAX_WAIT'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

MOBILE_APP_PACKAGE(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'MOBILE_APP_PACKAGE'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'MOBILE_APP_PACKAGE'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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

MOBILE_APP_ACTIVITY(BaseSetuObject.java:130)	---------- Setu Error Response ----------------------
(BaseSetuObject.java:131)	Got Http Error: 500
(BaseSetuObject.java:133)	Error: 'MOBILE_APP_ACTIVITY'
(BaseSetuObject.java:134)	---------- Setu Error Trace -------------------------
(BaseSetuObject.java:135)	Traceback (most recent call last):
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 51, in post
    res = self.__call_test_session_handler(testsession_handler, action_type, json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\interface\setu.py", line 188, in __call_test_session_handler
    return method(action_type.name.replace(handler_remove_prefix[method], "").lower(), json_dict["args"])
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 121, in take_conf_action
    return getattr(self.__conf_handler, action)(**json_dict)
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\adapter.py", line 194, in get_arjuna_option_value
    return {"value": self.__configurator.get_arjuna_option_value(configSetuId, option)}
  File "G:\__work__\tm\arjuna\arjuna\lib\setu\testsession\impl.py", line 59, in get_arjuna_option_value
    sname = ArjunaOption[option.upper().strip().replace(".", "_")]
  File "C:\Python36\lib\enum.py", line 327, in __getitem__
    return cls._member_map_[name]
KeyError: 'MOBILE_APP_ACTIVITY'

(BaseSetuObject.java:136)	-----------------------------------------------------
arjuna.lib.httpclient.SetuHttpException: Setu returned an error response.
	at arjuna.lib.httpclient.BasicRestClient.handleResponse(BasicRestClient.java:38)
	at arjuna.lib.httpclient.BasicRestClient.post(BasicRestClient.java:60)
	at arjuna.lib.setu.core.requester.connector.DefaultSetuRequester.post(BaseSetuObject.java:127)
	at arjuna.lib.setu.core.requester.connector.BaseSetuObject.sendRequest(BaseSetuObject.java:97)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.fetchConfOptionValue(DefaultTestConfig.java:33)
	at arjuna.lib.setu.core.requester.config.DefaultTestConfig.getArjunaOptionValue(DefaultTestConfig.java:48)
	at com.testmile.arjuna_ex.utils.Utils.displayAllArjunaOptions(Utils.java:49)
	at com.testmile.arjuna_ex.AutomatorConfigObj.test(AutomatorConfigObj.java:31)
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
Able to get the ArjunaOptions from the `TestConfig` object:
```
LOG_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/log
DATA_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/data/
DATA_SOURCES_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/data//sources
DATA_REFERENCES_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/data//references
GUIAUTO_NAMESPACE_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/guiauto/namespace/
SCREENSHOTS_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/screenshots/
PROJECT_CONF_FILE :: G:\__work__\tm\oss_ws\arjuna-ex/config/project.conf
TESTRUN_ENVIRONMENT :: TEST
BROWSER_NAME :: CHROME
BROWSER_VERSION :: not_set
BROWSER_MAXIMIZE :: true
BROWSER_DIM_WIDTH :: not_set
BROWSER_DIM_HEIGHT :: not_set
BROWSER_BIN_PATH :: not_set
BROWSER_PROXY_ON :: false
GUIAUTO_CONTEXT :: WEB
GUIAUTO_MAX_WAIT :: 10.0
GUIAUTO_SLOMO_ON :: false
GUIAUTO_SLOMO_INTERVAL :: 2.0
MOBILE_OS_NAME :: ANDROID
MOBILE_OS_VERSION :: not_set
MOBILE_DEVICE_NAME :: Android Emulator
MOBILE_DEVICE_UDID :: not_set
MOBILE_APP_FILE_PATH :: not_set
SELENIUM_DRIVER_PROP :: webdriver.chrome.driver
SELENIUM_DRIVERS_DIR :: G:\__work__\tm\oss_ws\arjuna-ex/guiauto/drivers
SELENIUM_DRIVER_PATH :: G:\__work__\tm\oss_ws\arjuna-ex/guiauto/drivers/windows/chromedriver.exe
APPIUM_HUB_URL :: http://127.0.0.1:4723/wd/hub
APPIUM_AUTO_LAUNCH :: false
IMAGE_COMPARISON_MIN_SCORE :: 0.7
```