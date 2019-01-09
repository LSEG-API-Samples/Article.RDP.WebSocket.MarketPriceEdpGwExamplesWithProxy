These examples are the modified version of [EDP Java Examples](https://github.com/Refinitiv/websocket-api/tree/master/Applications/Examples/EDP/java) with the new optional arguments for proxy settings.

|Arguement Name|Description|Default Value|
|--------------|-----------|-------------|
|--proxy_hostname|The hostname or IP address of the proxy|127.0.0.1|
|--proxy_port|The TCP port listened by the proxy|8888|

Before running the examples, the Fiddler Root certificate must be imported to the Java KeyStore. Typically, the Java KeyStory file (cacerts) is in the **JAVA_HOME\jre\lib\security\cacerts** directory. The following command can be used to import the Fiddler Root certificate file.

```
C:\Program Files\Java\jdk1.8.0_131\jre\lib\security>keytool -import -alias fiddl
er -file FiddlerRoot.crt -keystore cacerts  -storepass changeit

```

The **FiddlerRoot.crt** file was created in the [Export and convert the Fiddler Root certificate file](https://github.com/TR-API-Samples/Article.EDPRT.WebSocket.MarketPriceEdpGwExamplesWithProxy) step. 

The Fiddler Root certificate can be removed from the Java KeyStore with the following command.

```
C:\Program Files\Java\jdk1.8.0_131\jre\lib\security>keytool -delete -alias fiddler -keystore cacerts -storepass changeit
```
