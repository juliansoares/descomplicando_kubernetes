# Kubernetes Labs com Kind

Este repositório contém uma coleção de exercícios, anotações e configurações relacionadas ao estudo e prática com **Kubernetes**, utilizando o **Kind (Kubernetes IN Docker)** como ambiente local de testes.

## Objetivo

Documentar o progresso diário de aprendizado com Kubernetes, organizando os arquivos em pastas por dia (`day-1`, `day-2`, etc.), com foco em:

- Criação de clusters locais com Kind
- Aplicação de manifestos (pods, services, deployments etc.)
- Testes e validações de comportamento no cluster
- Comandos úteis e boas práticas

## Estrutura
├── day-1/
│ └── kind/
│ ├── kind-cluster.yaml
│ ├── pod.yaml
│ └── README.md
├── day-2/
│ └── ...
└── README.md

## Pré-requisitos

- [Docker](https://www.docker.com/)
- [Kind](https://kind.sigs.k8s.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Começando

Clone o repositório:

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
