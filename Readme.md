# Desafio Técnico: Olist + IBGE (Censo 2022)

Este projeto cruza dados reais de e-commerce com dados demográficos oficiais
para identificar onde a Olist está perdendo dinheiro e quais são as maiores
oportunidades de expansão no Brasil.

## O que este projeto resolve?

O objetivo foi criar um pipeline de dados capaz de:

- Ingerir e tratar dados brutos do Kaggle (Olist) e SIDRA (IBGE)
- Calcular a penetração de mercado por município (clientes por 10k habitantes)
- Analisar sazonalidade e meios de pagamento por região
- Apresentar um storytelling estratégico para tomada de decisão da diretoria

## Tech Stack

- **Python 3.x** — linguagem base do pipeline
- **DuckDB** — banco de dados OLAP in-process para consultas SQL rápidas
- **Pandas** — manipulação e limpeza dos dados
- **Matplotlib / Folium** — visualizações e mapa de dispersão geográfica

## Estrutura do Projeto
```
olist-ibge-market-analysis/
├── .env                   # Variáveis de ambiente (não sobe pro GitHub)
├── .gitignore             
├── requirements.txt       # Dependências do projeto
└── notebook/              
    └── desafiomconf.ipynb # Análise completa e documentada
```

> **Obs.:** A pasta `data/` não está versionada. Os dados são públicos e o
> próprio notebook faz o download automático via Kaggle API e SIDRA ao
> ser executado.

## Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/GabrielaHSantos/olist-ibge-market-analysis.git
```

2. Crie um ambiente virtual e instale as dependências:
```bash
pip install -r requirements.txt
```

3. Configure o `.env` com suas credenciais do Kaggle:
```
KAGGLE_USERNAME=seu_usuario
KAGGLE_KEY=sua_chave
```

4. Abra e execute o notebook `notebook/desafiomconf.ipynb` do início ao fim.

## Destaques Técnicos

- **Normalização de strings** para garantir o JOIN entre bases de fontes diferentes
- **DuckDB** para modelagem e consultas SQL sobre os DataFrames em memória
- **Análise crítica** com limitações técnicas documentadas e sugestões de melhorias futuras

## Fontes de Dados

- [Olist — Brazilian E-commerce (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- [IBGE SIDRA — Tabela 4709](https://sidra.ibge.gov.br/tabela/4709)