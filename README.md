# Kubernetes Labs com Kind

Este repositório contém uma coleção de exercícios, anotações e configurações relacionadas ao estudo e prática com **Kubernetes**, utilizando o **Kind (Kubernetes IN Docker)** como ambiente local de testes.

## Objetivo

Documentar o progresso diário de aprendizado com Kubernetes, organizando os arquivos em pastas por dia (`day-1`, `day-2`, etc.), com foco em:

- Criação de clusters locais com Kind
- Aplicação de manifestos (pods, services, deployments etc.)
- Testes e validações de comportamento no cluster
- Comandos úteis e boas práticas

## Estrutura

```
.
├── day-1/
│   └── kind/
│       ├── kind-cluster.yaml
│       ├── pod.yaml
│       └── README.md
├── day-2/
│   └── ...
└── README.md
```

## Pré-requisitos

Antes de iniciar, certifique-se de ter instalado:

- [Docker](https://www.docker.com/get-started)
- [Kind](https://kind.sigs.k8s.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## Começando

1. Clone o repositório:

```bash
git clone https://github.com/juliansoares/descomplicando_kubernetes.git
cd descomplicando_kubernetes
```

2. Navegue até a pasta do dia que deseja estudar/executar:

```bash
cd day-1/kind
```

3. Siga as instruções no `README.md` daquela pasta para criar o cluster Kind e aplicar os manifests.

## Uso básico do Kind no repositório

```bash
# Criar cluster com arquivo de configuração
kind create cluster --config kind-cluster.yaml --name giropops

# Listar clusters ativos
kind get clusters

# Aplicar pod de teste
kubectl apply -f pod.yaml

# Verificar pods
kubectl get pods

# Deletar cluster
kind delete cluster --name giropops
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues, sugerir melhorias ou enviar pull requests.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

Feito por juliansoares 🚀
