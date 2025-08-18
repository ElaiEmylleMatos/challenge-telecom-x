# Análise e Identificação de Fatores de Churn em Clientes da Telecom X

Este notebook contém uma análise exploratória de dados (EDA) focada na identificação dos principais fatores associados ao cancelamento de clientes (Churn) em uma base de dados de uma empresa de telecomunicações (TelecomX).

O objetivo principal é compreender padrões e características de clientes que possuem maior probabilidade de cancelar seus contratos, fornecendo insights para ações de retenção e estratégias de negócio.

## Estrutura do Notebook

O notebook está organizado nas seguintes seções:

1.  **Extração**: Carregamento dos dados a partir da URL fornecida.
2.  **Transformação**:
    *   Desaninhamento da estrutura JSON para um formato tabular mais acessível.
    *   Limpeza de colunas desnecessárias (`customerID`).
    *   Conversão de tipos de dados (tratamento da coluna `Charges.Total` para numérico).
    *   Tratamento de valores ausentes (`NaN`) e inconsistentes (valor vazio na coluna `Churn`).
3.  **Carga e Análise (EDA)**:
    *   Descrição estatística das variáveis numéricas e categóricas.
    *   Análise da proporção geral de Churn na base.
    *   Análise do Churn por variáveis categóricas (Demográficas, Relacionamento com a empresa, Serviços contratados) com visualizações em barras.
    *   Análise do Churn por variáveis numéricas (Tenure, Charges.Monthly, Charges.Total) com visualizações (Boxplots, KDEs) e análise de correlação. Criação de faixas para análise percentual.
    *   Identificação das características com maior taxa de Churn.
4.  **Relatório Final**:
    *   Introdução com o contexto e objetivo da análise.
    *   Sumário das etapas de Limpeza e Tratamento de Dados.
    *   Discussão dos achados da Análise Exploratória de Dados com base nos gráficos gerados.
    *   Recomendações de ações estratégicas para redução do Churn.

## Dados

O conjunto de dados utilizado é o `TelecomX_Data.json`, disponível em um repositório público do GitHub. Ele contém informações sobre clientes, incluindo dados demográficos, serviços contratados, informações de conta e o status de Churn.

## Bibliotecas Utilizadas

*   `pandas`: Para manipulação e análise de dados.
*   `numpy`: Para operações numéricas.
*   `matplotlib.pyplot`: Para criação de visualizações estáticas.
*   `seaborn`: Para criação de visualizações estatísticas mais atraentes.
*   `json`: Para trabalhar com o formato JSON.

## Como Executar

1.  Abra o notebook em um ambiente que suporte Jupyter Notebooks (como Google Colab, JupyterLab, etc.).
2.  Execute as células sequencialmente.
3.  Observe as saídas e visualizações geradas em cada etapa.

## Conclusões Principais

*   Clientes com **contrato mensal** e que utilizam **cheque eletrônico** como forma de pagamento apresentam taxas de churn significativamente mais altas.
*   A ausência de serviços de **segurança online** e **suporte técnico** também está associada a um maior percentual de cancelamento.
*   Clientes com **pouco tempo de contrato (tenure baixo)** são mais propensos a cancelar.
*   **Cobranças mensais mais altas** tendem a se correlacionar positivamente com o Churn.

## Recomendações Estratégicas

As recomendações detalhadas para mitigar o Churn, como programas de retenção para novos clientes, incentivos para adoção de planos de maior duração e formas de pagamento automáticas, e oferta de bundles de segurança/suporte, estão apresentadas na seção "Recomendações" do notebook.
