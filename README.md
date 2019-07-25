# Curso Alura de Kubernates

Projeto de estudo curso de kubernates

### Pré-requisitos

Instalações nescessárias para rodar o projeto

```
* [Docker](https://docs.docker.com/install/)
* [Docker compose](https://docs.docker.com/compose/install/)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* [Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/)
* [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
```

## Rodar

Comandos para rodar o projeto

Inicialize o minikube com o comando:
```
minikube start
```

Na sequência, caso estejamos trabalhando com diferentes clusters, é importante especificarmos que queremos trabalhar com o minikube, para isso coloque o comando:
```
kubectl config use-context minikube
```

Subir pods
```
cd kubernates/db/
kubectl create -f statefulset.yaml
kubectl create -f servico-banco.yaml
kubectl create -f permissoes.yaml

cd ../app/
kubectl create -f deployment.yaml
kubectl create -f servico-aplicacao.yaml
```


