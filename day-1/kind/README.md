# Day 1 - Kind

Esta pasta contém os arquivos e anotações relacionadas ao uso do **[Kind (Kubernetes IN Docker)](https://kind.sigs.k8s.io/)**.

## Objetivo

Configurar e executar um cluster Kubernetes local usando o Kind para fins de testes e aprendizado.

## Conteúdo

- Arquivos de configuração do cluster (`kind-cluster.yaml`)
- Comandos úteis para gerenciamento do cluster
- Scripts de automação (se houver)
- Notas e observações importantes

## Requisitos

- Docker instalado
- Kind instalado (`go install sigs.k8s.io/kind@latest` ou via `apt`, `brew`, etc.)

## Comandos iniciais

```bash
# Criar cluster com arquivo de config

kind create cluster --config kind-cluster.yaml --name giropops

# Listar clusters Kind
kind get clusters

# Deletar cluster
kind delete cluster --name meu-cluster
