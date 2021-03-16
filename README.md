# functions-love-java

Azure Function examples in Java

To run it on your machine just use the following commands:

```bash
cd {folder}
mvn clean install
mvn azure-functions:run
```

Deploy to Azure Functions with `mvn azure-functions:deploy`:

```bash
mvn azure-functions:deploy
```

Run the following command to view near real-time [streaming logs](https://docs.microsoft.com/azure/azure-functions/functions-run-local?tabs=macos%2Ccsharp%2Cbash#enable-streaming-logs&WT..mc_id=java-20736-sakriema):

```bash
func azure functionapp logstream <APP_NAME> 
```

You need to have an Azure Subscription to deploy to Azure. [Checkout Azure's free offerings](https://aka.ms/az-free)
And you need to be logged-in to your Azure Account within your [az-cli](https://aka.ms/install-az-cli). Run `az login` to log in.

Make sure to follow the [best practices for Azure Functions](https://aka.ms/az-best-functions):

- Avoid long running functions
- Take care of cross function communication
- Make your functions stateless
- Write defensive functions
- Organize functions for performance and scaling
- Don't mix test and production code in the same function app

more at the [official documentation for best practices](https://aka.ms/az-best-functions).

## Vanilla Java

To build this project yourself, you can leverage from maven archetype.

```bash
mvn archetype:generate -DarchetypeGroupId=com.microsoft.azure -DarchetypeArtifactId=azure-functions-archetype -DjavaVersion=11
```

More details can be find [here](https://aka.ms/az-java-function).

## Quarkus

Azure Functions are available for Java 8 and 11 since 1.12.0.Final.

To build this project yourself, you can leverage from maven archetype.

```bash
mvn archetype:generate \                    
    -DarchetypeGroupId=io.quarkus \
    -DarchetypeArtifactId=quarkus-azure-functions-http-archetype \
    -DarchetypeVersion=1.12.1.Final
```

Find more details for Azure Functions and Quarkus [here](https://quarkus.io/guides/azure-functions-http).

## Micronaut

Let [micronaut.io](https://micronaut.io/launch/) generate your starting project.

Java 11 is not supported yet and will fall back to 8.

This repo used [https://micronaut.io/launch/?javaVersion=JDK_8&lang=JAVA&build=MAVEN&test=JUNIT&name=demo&package=com.example&type=DEFAULT&features=azure-function&version=2.4.0&activity=preview&showing=/pom.xml](https://micronaut.io/launch/?javaVersion=JDK_11&lang=JAVA&build=MAVEN&test=JUNIT&name=demo&package=com.example&type=DEFAULT&features=azure-function&version=2.4.0&activity=preview&showing=/pom.xml)
