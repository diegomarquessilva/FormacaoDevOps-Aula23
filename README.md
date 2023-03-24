# FormacaoDevOps-Aula23
Demonstração e codigo fonte da Aula 23 da formação DevOps.

O exemplo abaixo cria uma Service Connection, Web Hook e Pipeline. Esse pipeline é automaticamente enfileirado no momento de aprovação com sucesso de um Pull Request. Na finalização do Pipeline, a automação move o Status do Work Item vinculado ao Pull Request para o status Resolved.

Abaixo seguem os passos para reprodução da demonstração

## Criação da Service Connection

![image](https://user-images.githubusercontent.com/8333012/227521407-19179f18-892f-49c8-97ad-242d94e8106c.png)

![image](https://user-images.githubusercontent.com/8333012/227521574-ccf176d2-8be0-4052-9483-4f0cf4334bf8.png)

## Criação do Service Hook

![image](https://user-images.githubusercontent.com/8333012/227521802-644adec1-ef07-4874-b514-59305be543d9.png)

![image](https://user-images.githubusercontent.com/8333012/227521846-8d15ab16-0020-467c-b591-06da79357434.png)

```
URL: https://dev.azure.com/{ORGANIZATION}/_apis/public/distributedtask/webhooks/{WEBHOOKNAME}?api-version=6.0-preview
```
## Pipeline YAML

Verifique o YAML no Code do Repositorio

```
azure-pipelines.yml
```
## Documentação Referência

[Define a webhooks resource](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/resources?view=azure-devops&tabs=schema#define-a-webhooks-resource)
