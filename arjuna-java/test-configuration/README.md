# Test Configuration in Arjuna

Arjuna supports a layered configuration. Hence a configuration is updated a t a certain layer the subsequent inherits the updated configuration.
### Project Level Configuration 
> A file based configuration
Under the project config directory you will fins a file project.conf contating the followinf structure
```
arjunaOptions {

}
userOptions {

}
```
arjunaOptions are the options which were provided by arjuna to manipulate your automator properties

| Option Name        | default value |
| ------------- |:-------------:|
| BROWSER_NAME | chrome |
| BROWSER_MAXIMIZE | false |
| BROWSER_HEADLESS_MODE | off |
| GUIAUTO_MAX_WAIT | 30 |
| GUIAUTO_SLOMO_ON | off|


Let's change the BROWSER_NAME value from chrome to firefox ans see what happens.
Update the config to 
```
arjunaOptions {
    BROWSER_NAME = firefox
}
userOptions {

}
```
Run the following Class
[Basic1WithCentralTestContext](https://github.com/test-mile/arjuna-java/blob/master/arjuna-java-examples/src/test/java/arjex/s01config/Basic1WithCentralTestContext.java

### Creating configuration programatically

Arjuna `init()` returns a `TestContext` allows to build a custom config through `ConfigBuilder`.

```java
TestContext context = Arjuna.init();
context
.ConfigBuilder()
.firefox()
.build("ff");
```

### Configuration through command line.
Add the jvm args --aco --ato to update arjuna options
`-Daco:BROWSER_NAME=firefox`
lly
arjuna test options `-Dato:<ARJUNA_OPTION>=value`
user central options `-Duco:<ARJUNA_OPTION>=value`
user test options `-Duto:<ARJUNA_OPTION>=value`
Command line configuration will override the file based configuration and configuration created programtically.