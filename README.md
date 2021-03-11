# functions-love-java

Azure Function examples in Java

## Vanilla Java

To run it on your machine just use the following commands.

```bash
mvn clean install
mvn azure-functions:run
```

Deploy to Azure Functions with `mvn azure-functions:deploy`.

```bash
mvn azure-functions:deploy
```

## Quarkus

Azure Functions are available for Java 8 and 11 since 1.12.0.Final.

To run it on your machine just use the following commands.

```bash
mvn clean install
mvn azure-functions:run
```

Deploy to Azure Functions with `mvn azure-functions:deploy`.

```bash
mvn azure-functions:deploy
```

You need to have an Azure Subscription to deploy to Azure. [Checkout Azure's free offerings](https://aka.ms/az-free)
And you need to be logged-in to your Azure Account within your [az-cli](https://aka.ms/install-az-cli). Run `az login` to log in.

To build this project yourself, you can leverage from maven archetype.

```bash
mvn archetype:generate \                    
    -DarchetypeGroupId=io.quarkus \
    -DarchetypeArtifactId=quarkus-azure-functions-http-archetype \
    -DarchetypeVersion=1.12.1.Final
```
