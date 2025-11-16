Catálogo de Dados

Este catálogo documenta as tabelas tratadas utilizadas no projeto de análise de fundos de investimento, com foco em padronização, governança e qualidade dos dados.

Tabela: fundos_tratado

| Coluna                    | Tipo    | Descrição técnica                                      | Domínio esperado                     |
|---------------------------|---------|--------------------------------------------------------|--------------------------------------|
| CNPJ_FUNDO_PADRONIZADO    | string  | CNPJ do fundo sem formatação (somente números)         | 14 dígitos numéricos                 |
| CNPJ_CLASSE_PADRONIZADO   | string  | CNPJ da classe do fundo sem formatação                 | 14 dígitos numéricos                 |
| CODIGO_ANBIMA             | string  | Código de registro do fundo na ANBIMA                  | Alfanumérico                         |
| Estrutura                 | string  | Tipo de estrutura do fundo                             | Classe, Fundo, Subclasse             |
| NOME_COMERCIAL            | string  | Nome comercial do fundo                                | Texto livre                          |
| DATA_INICIO_ATIVIDADE     | date    | Data de início das atividades do fundo                 | Formato: yyyy-MM-dd                  |
| DATA_REF_DADOS_PERIODICOS | date    | Data de referência dos dados periódicos                | Formato: yyyy-MM-dd                  |
| QTDE_SUBCLASSES           | int     | Quantidade de subclasses associadas ao fundo           | Inteiros positivos                   |
| QTDE_COTISTAS             | int     | Quantidade de cotistas do fundo                        | Inteiros positivos                   |
| PL_ATUAL                  | double  | Patrimônio líquido atual do fundo                      | Valores monetários (R$)              |
| VALOR_COTA_ATUAL          | double  | Valor atual da cota do fundo                           | Valores monetários (R$)              |


Tabela: gestor_tratado

| Coluna         | Tipo   | Descrição técnica                          | Domínio esperado                     |
|----------------|--------|--------------------------------------------|--------------------------------------|
| CNPJ_FUNDO     | string | Identificador do fundo                     | 14 dígitos numéricos                 |
| CNPJ_GESTOR    | string | Identificador do gestor                    | 14 dígitos numéricos                 |
| GESTOR         | string | Nome da instituição gestora                | Texto livre                          |
| PF_PJ_GESTOR   | string | Tipo de gestor (Pessoa Física ou Jurídica) | PF, PJ                               |
| DT_REG         | date   | Data de registro do fundo                  | Formato: yyyy-MM-dd                  |
| DT_INICIO      | date   | Data de início da gestão                   | Formato: yyyy-MM-dd                  |
| DT_FIM         | date   | Data de fim da gestão                      | Pode ser nulo (gestão ativa)         |


Linhagem dos Dados

- **Fonte**: ANBIMA e CVM
- **Coleta**: Arquivos CSV carregados manualmente no Databricks
- **Transformações**: Padronização de CNPJs, conversão de datas, renomeação de colunas, correção de tipos
- **Armazenamento**: Tabelas `fundos_tratado` e `gestor_tratado` no catálogo `default` do Databricks
- **Objetivo**: Preparar dados confiáveis para análise, visualização e integração com outras fontes
