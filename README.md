from fpdf import FPDF

# Texto simples do README sem caracteres especiais para evitar erros
content_simple = """
Kubernetes Labs com Kind

Este repositorio contem uma colecao de exercicios, anotacoes e configuracoes relacionadas ao estudo e pratica com Kubernetes, utilizando o Kind (Kubernetes IN Docker) como ambiente local de testes.

Objetivo

Documentar o progresso diario de aprendizado com Kubernetes, organizando os arquivos em pastas por dia (day-1, day-2, etc.), com foco em:

- Criacao de clusters locais com Kind
- Aplicacao de manifestos (pods, services, deployments etc.)
- Testes e validacoes de comportamento no cluster
- Comandos uteis e boas praticas

Estrutura

.
├── day-1/
│   └── kind/
│       ├── kind-cluster.yaml
│       ├── pod.yaml
│       └── README.md
├── day-2/
│   └── ...
└── README.md

Pre-requisitos

Antes de iniciar, certifique-se de ter instalado:

- Docker (https://www.docker.com/get-started)
- Kind (https://kind.sigs.k8s.io/)
- kubectl (https://kubernetes.io/docs/tasks/tools/)

Comecando

1. Clone o repositorio:

git clone https://github.com/juliansoares/descomplicando_kubernetes.git
cd descomplicando_kubernetes

2. Navegue ate a pasta do dia que deseja estudar/executar:

cd day-1/kind

3. Siga as instrucoes no README.md daquela pasta para criar o cluster Kind e aplicar os manifests.

Uso basico do Kind no repositorio

# Criar cluster com arquivo de configuracao
kind create cluster --config kind-cluster.yaml --name giropops

# Listar clusters ativos
kind get clusters

# Aplicar pod de teste
kubectl apply -f pod.yaml

# Verificar pods
kubectl get pods

# Deletar cluster
kind delete cluster --name giropops

Contribuicao

Contribuicoes sao bem-vindas! Sinta-se a vontade para abrir issues, sugerir melhorias ou enviar pull requests.

Licenca

Este projeto esta licenciado sob a MIT License (LICENSE).

---

Feito por juliansoares
"""

# Criar PDF
pdf = FPDF()
pdf.add_page()
pdf.set_auto_page_break(auto=True, margin=15)
pdf.set_font("Arial", size=12)

# Adicionar linhas ao PDF
for line in content_simple.split('\n'):
    pdf.multi_cell(0, 8, line)

# Salvar arquivo PDF
path = "/mnt/data/README_descomplicando_kubernetes.pdf"
pdf.output(path)

path
