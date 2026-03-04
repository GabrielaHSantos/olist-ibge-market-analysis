# Desafio Técnico — E-commerce & Demografia

Análise de oportunidades de expansão cruzando dados históricos da Olist
com dados demográficos do Censo IBGE 2022, com foco em identificar regiões
com maior potencial de crescimento.

O notebook contém toda a análise documentada, do pipeline de ingestão até
o storytelling final para a diretoria.

## Estrutura do Projeto
```
desafiomconf/
├── .env                   # Credenciais (não sobe pro GitHub)
├── .gitignore             
├── requirements.txt       # Dependências Python
└── notebook/              
    └── desafiomconf.ipynb # Notebook principal
```

## Como Rodar

1. Clone o repositório
2. Crie um ambiente virtual e instale as dependências:
```bash
   pip install -r requirements.txt
```
3. Configure suas credenciais do Kaggle no `.env`
4. Execute o notebook do início ao fim

## Fonte dos Dados

- [Olist — Brazilian E-commerce (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- [IBGE SIDRA — Tabela 4709](https://sidra.ibge.gov.br/tabela/4709)