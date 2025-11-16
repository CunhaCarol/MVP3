# MVP3
FUNDOS DE INVESTIMENTOS - Pipeline de Dados com Databricks e Power BI

MVP – Pipeline de Dados com Databricks e Power BI
Este repositório documenta o desenvolvimento de um MVP de pipeline de dados utilizando a plataforma Databricks Community Edition e visualizações no Power BI. O projeto tem como objetivo analisar a distribuição, gestão e desempenho dos fundos de investimento no Brasil, a partir de dados públicos da ANBIMA e da CVM.

O trabalho busca responder às seguintes perguntas de negócio:
- Quais tipos de fundos são mais comuns?
- Qual o patrimônio líquido médio por tipo de fundo?
- Quais gestores concentram mais fundos?

Etapas do Projeto
1. Coleta
- Fontes: ANBIMA e CVM
- Arquivos CSV públicos contendo dados de fundos e seus respectivos gestores
- Upload realizado na plataforma Databricks
2. Modelagem
- Modelo em esquema estrela com:
- Tabela fato: fundos
- Tabela dimensão: gestores
- Catálogo de Dados documentado com tipos, descrições e domínios esperados
3. Carga e Transformações
- ETL realizado via SQL no Databricks
- Junção dos datasets por CNPJ do fundo
- Criação de tabelas tratadas para análise
4. Análise
- Avaliação da qualidade dos dados
- Respostas às perguntas de negócio via SQL
- Visualizações complementares no Power BI
5. Autoavaliação
- Reflexão sobre os objetivos atingidos, dificuldades enfrentadas e melhorias futuras.

 Tecnologias Utilizadas
- Databricks Community Edition
- Power BI Desktop
- GitHub
- 
Estrutura do Repositório
📂 /notebooks_sql
    └── consultas.sql
📂 /data
    └── arquivos_originais.csv
📂 /screenshots
    └── evidencias_etapas.png
📂 /powerbi
    └── dashboard.pbix
📄 README.md
📄 objetivos.md
📄 autoavaliacao.md
📄 catalogo_dados.md



