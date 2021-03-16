## Micronaut 2.4.0 Documentation

- [User Guide](https://docs.micronaut.io/2.4.0/guide/index.html)
- [API Reference](https://docs.micronaut.io/2.4.0/api/index.html)
- [Configuration Reference](https://docs.micronaut.io/2.4.0/guide/configurationreference.html)
- [Micronaut Guides](https://guides.micronaut.io/index.html)

---

# Micronaut and Azure Function

## Prerequisites

- Latest [Function Core Tools](https://docs.microsoft.com/azure/azure-functions/create-first-function-cli-java?tabs=bash%2Cazure-cli%2Cbrowser&WT.mc_id=java-20736-sakriema)
- Azure CLI. This plugin use Azure CLI for authentication, please make sure you have Azure CLI installed and logged in.

## Setup

```cmd
az login
az account set -s <your subscription id>

## Running the function locally

```cmd
./mvnw clean package azure-functions:run
```

And visit http://localhost:7071/api/demo

## Deploying the function

To deploy the function run:

```bash
./mvnw clean package azure-functions:deploy
```

## Feature azure-function documentation

- [Micronaut Azure Function documentation](https://micronaut-projects.github.io/micronaut-azure/latest/guide/index.html#simpleAzureFunctions)

- [https://docs.microsoft.com/azure](https://docs.microsoft.com/azure/?WT.mc_id=java-20736-sakriema)

## Feature azure-function-http documentation

- [Micronaut Azure Function documentation](https://micronaut-projects.github.io/micronaut-azure/latest/guide/index.html#azureHttpFunctions)
