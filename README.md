# NPS Predictive Analysis

Este projeto foi desenvolvido como parte do Tech Challenge da pós-graduação em AI Scientist. O objetivo é analisar dados de um e-commerce para entender quais fatores podem estar relacionados à satisfação dos clientes e construir um modelo preditivo simples para identificar clientes com maior risco de serem detratores.

## Objetivo do projeto

O objetivo principal do projeto é entender quais pontos da jornada de compra podem influenciar o NPS do cliente.

A análise busca responder perguntas como:

- Quais fatores parecem estar mais relacionados à satisfação do cliente?
- O que pode estar gerando clientes detratores?
- Existe algum ponto de ruptura na experiência, como muitos dias de atraso?
- Que tipo de cliente tende a ter NPS mais alto ou mais baixo?
- Como um modelo preditivo poderia ajudar a empresa a identificar clientes com risco de insatisfação?

Além da análise exploratória, também foi criado um modelo preditivo inicial para classificar clientes como detratores ou não detratores.

## Descrição da base de dados

A base utilizada contém informações de clientes, pedidos, entrega, atendimento e satisfação.

O arquivo principal está em:

```text
data/raw/desafio_nps_fase_1.csv
```

A base possui 2.500 registros e 19 colunas. Algumas das principais variáveis são:

- `customer_id`: identificação do cliente;
- `customer_age`: idade do cliente;
- `customer_region`: região do cliente;
- `customer_tenure_months`: tempo de relacionamento do cliente com a empresa;
- `order_id`: identificação do pedido;
- `order_value`: valor do pedido;
- `items_quantity`: quantidade de itens no pedido;
- `discount_value`: valor de desconto aplicado;
- `payment_installments`: número de parcelas;
- `delivery_time_days`: tempo total de entrega;
- `delivery_delay_days`: dias de atraso na entrega;
- `freight_value`: valor do frete;
- `delivery_attempts`: número de tentativas de entrega;
- `customer_service_contacts`: quantidade de contatos com atendimento;
- `resolution_time_days`: tempo de resolução de problemas;
- `complaints_count`: quantidade de reclamações;
- `repeat_purchase_30d`: indicação de recompra em até 30 dias;
- `csat_internal_score`: nota interna de satisfação;
- `nps_score`: nota de NPS dada pelo cliente.

A variável `nps_score` foi usada como base para entender a satisfação do cliente e também para criar a target do modelo preditivo.

## Metodologia utilizada

A metodologia seguida foi baseada nas etapas de um projeto de ciência de dados, com foco em entendimento do negócio, definição da target, análise exploratória e modelo preditivo.

### 1. Entendimento do negócio

Primeiro, foi feita uma análise do problema de negócio. A ideia foi entender por que o NPS é importante para um e-commerce e quais áreas poderiam se beneficiar dos insights, como logística, atendimento, pricing, produto e estratégia.

### 2. Definição da target

A variável escolhida para representar a satisfação do cliente foi o `nps_score`, porque ela mostra a percepção final do cliente depois da jornada de compra.

Para o modelo preditivo, essa variável foi transformada em uma target binária chamada `is_detractor`:

- `1`: cliente detrator, com `nps_score` até 6;
- `0`: cliente não detrator, com `nps_score` acima de 6.

Essa escolha foi feita porque, para o negócio, pode ser mais útil identificar clientes com risco de insatisfação do que tentar prever exatamente a nota do NPS.

### 3. Análise exploratória dos dados

Na análise exploratória, foram analisadas variáveis relacionadas à jornada de compra e à experiência do cliente, como:

- atraso na entrega;
- tempo total de entrega;
- contatos com atendimento;
- reclamações;
- tempo de resolução;
- recompra em até 30 dias;
- região;
- idade;
- tempo de relacionamento com a empresa.

As análises indicaram que fatores operacionais, como atraso na entrega, reclamações e muitos contatos com atendimento, parecem estar mais relacionados a notas menores de NPS.

Também foi observado que clientes que recompraram em até 30 dias tiveram NPS médio mais alto, o que pode indicar uma relação entre satisfação e fidelização.

### 4. Modelo preditivo

Foi criado um modelo inicial de classificação usando Regressão Logística.

As variáveis de entrada foram selecionadas a partir dos dados da jornada de compra, entrega, atendimento e perfil do cliente. A base foi separada em treino e teste, usando 80% dos dados para treino e 20% para teste.

Como a target estava desbalanceada, foi utilizado `class_weight="balanced"` no modelo para reduzir o impacto da diferença entre as classes.

O modelo teve acurácia de aproximadamente 79,6% na base de teste. Mesmo assim, a avaliação mostrou que ele ainda deixou passar alguns clientes detratores. Por isso, o modelo foi tratado como um primeiro teste, e não como uma solução pronta para uso em produção.

## Como reproduzir os resultados

Para reproduzir o projeto, siga os passos abaixo.

### 1. Clonar o repositório

```bash
git clone git@github.com:vitoriags/nps-predictive-analysis.git
cd nps-predictive-analysis
```

### 2. Criar e ativar o ambiente virtual

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 4. Abrir o projeto no VS Code

```bash
code .
```

### 5. Executar o notebook

Abra o notebook:

```text
notebooks/01_eda_nps.ipynb
```

Execute as células em ordem para reproduzir:

- carregamento da base;
- análise exploratória dos dados;
- criação da target;
- separação entre treino e teste;
- treinamento do modelo;
- avaliação do modelo.

## Estrutura do projeto

```text
nps-predictive-analysis/
├── data/
│   ├── raw/
│   │   └── desafio_nps_fase_1.csv
│   └── processed/
├── models/
├── notebooks/
│   └── 01_eda_nps.ipynb
├── reports/
│   └── business_understanding.md
├── requirements.txt
└── README.md
```

## Conclusão

O projeto mostrou que a satisfação do cliente parece estar mais relacionada a fatores da experiência de compra do que apenas ao perfil do cliente.

Atrasos na entrega, reclamações, muitos contatos com atendimento e tempo de resolução aparecem como pontos importantes para o negócio acompanhar. O modelo preditivo também mostrou que existe algum padrão nos dados, mas ainda precisaria ser melhorado antes de ser usado em uma operação real.