# credit-card-customer-segmentation

# Segmentação de Clientes de Cartão de Crédito (Clustering)

## Descrição do Projeto
Este projeto realiza uma **segmentação de clientes de cartão de crédito** utilizando técnicas de **aprendizado não supervisionado (Clustering)**.  
O objetivo é **traduzir os clusters identificados em insights acionáveis** que possam apoiar as **equipes de Marketing e Produto** em estratégias de retenção, personalização e aumento de valor do cliente.

### Objetivo
Identificar grupos de clientes com comportamentos semelhantes e interpretar suas características, de forma a gerar **ações direcionadas** para cada perfil, como campanhas específicas, melhorias de produto ou políticas de crédito mais eficazes.

### Fonte de Dados
Dataset público disponível no Kaggle:  
🔗 [Credit Card Data (Kaggle)](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/data)

O conjunto de dados contém variáveis comportamentais e de uso de cartão de crédito, como:
- Limite de crédito
- Frequência de uso
- Saldo médio
- Transações mensais
- Pagamentos mínimos e totais

---

## Etapas do Projeto

### 1. Importação e Limpeza dos Dados
- Leitura das bases de dados originais em formato CSV.
- Tratamento de valores nulos, duplicados e inconsistências.
- Conversão de tipos de dados e padronização de colunas.

### 2. Pré-Processamento e Escalonamento
- Aplicação do **StandardScaler** para normalização.
- Codificação de variáveis categóricas via **OneHotEncoder**.
- Utilização de **PowerTransformer**, **log** e **Box-Cox** para correção de assimetria e aproximação da normalidade das distribuições.

### 3. Redução de Dimensionalidade
- Uso de **PCA (Principal Component Analysis)** para explorar a estrutura dos dados e visualizar separações entre grupos.

### 4. Modelagem de Cluster
Foram testados diferentes algoritmos de agrupamento:
- **K-Means**  
- **DBSCAN**  
- **Agglomerative Clustering (Hierárquico)**  

A escolha do modelo final foi baseada na análise de métricas como:
- **Silhouette Score**
- **Inércia (para K-Means)**
- **Interpretação visual dos clusters (via PCA)**

### 5. Análise de Variância (ANOVA)
Aplicação de **ANOVA unidirecional** para identificar variáveis com diferenças estatisticamente significativas entre os clusters, utilizando:
- `scipy.stats.f_oneway`
- Análise complementar de **p-values**, **F-stat**, **skewness** e **kurtosis**.

### 6. Perfil dos Clusters
Construção de uma tabela resumo com:
- Média das variáveis por cluster.  
- Interpretação do comportamento e características de cada grupo.  
- Sugestões de possíveis estratégias (ex: retenção, engajamento, risco, etc.).

---

## Principais Bibliotecas Utilizadas

```bash
pandas
numpy
seaborn
matplotlib
scipy
scikit-learn
```

## Contato  
Se precisar de mais informações, entre em contato:  
E-mail: thiago.a.v.souza@gmail.com  
Linkedin: [Thiago Souza](https://www.linkedin.com/in/thiagoavsouza/)
