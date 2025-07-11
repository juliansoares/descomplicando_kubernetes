# Day 1 - Kind

Esta pasta contém os arquivos e anotações relacionadas ao uso do **[Kind (Kubernetes IN Docker)](https://kind.sigs.k8s.io/)**.

## Objetivo

Configurar e executar um cluster Kubernetes local usando o Kind para fins de testes e aprendizado, além de aplicar recursos como pods diretamente no cluster.

## Conteúdo

- `kind-cluster.yaml`: configuração do cluster Kind
- `pod.yaml`: definição de um pod simples para teste
- Comandos úteis para gerenciamento do cluster
- Scripts e observações importantes

## Requisitos

- Docker instalado
- Kind instalado (`go install sigs.k8s.io/kind@latest` ou via `apt`, `brew`, etc.)
- kubectl configurado (geralmente `kind` já integra o cluster ao `kubectl`)

## Comandos iniciais

```bash
# Criar cluster com arquivo de configuração
kind create cluster --config kind-cluster.yaml --name giropops

# Verificar clusters Kind existentes
kind get clusters

# Aplicar o pod de teste
kubectl apply -f pod.yaml

# Verificar o pod em execução
kubectl get pods

# Deletar pod
kind delete pods giropops-nginx
