# 🛒 Segmentação de Clientes de E-commerce com K-Means

Este notebook demonstra como segmentar clientes de um e-commerce usando o algoritmo **K-Means**.  
O dataset contém transações de uma varejista online do Reino Unido, registradas entre **01/12/2010** e **09/12/2011**.

A empresa analisada é uma varejista que opera exclusivamente online, especializada em presentes diferenciados para diversas ocasiões, atendendo tanto consumidores finais quanto atacadistas.

---

## 🚀 Fluxo de Análise

### 1. Importação de Bibliotecas  
Ferramentas para manipulação de dados, clustering e visualização são carregadas.

### 2. Carregamento do Dataset  
Cada registro representa uma transação, contendo informações como:  
- **CustomerID**  
- **InvoiceNo**  
- **Quantity**  
- **UnitPrice**  
- **InvoiceDate**

### 3. Exploração Inicial  
Análise do formato da base, estrutura das colunas e verificação de valores ausentes.

### 4. Limpeza de Dados  
- Remoção de registros sem `CustomerID`  
- Eliminação de duplicatas  
- Exclusão de transações com quantidades ou preços negativos

### 5. Criação de Métricas Adicionais  
- Conversão correta da coluna de datas  
- Cálculo do valor total da compra (`TotalPrice = Quantity × UnitPrice`)

### 6. Construção da Tabela RFM  
Cálculo das métricas fundamentais para análise de comportamento do cliente:  
- **Recência (R):** dias desde a última compra  
- **Frequência (F):** número de compras distintas  
- **Valor Monetário (M):** total gasto pelo cliente

### 7. Padronização dos Dados  
As métricas RFM são escaladas para manter proporcionalidade e evitar vieses no clustering.

### 8. Definição do Número de Clusters  
Aplicação do **Elbow Method** para identificar a melhor quantidade de grupos.

### 9. Aplicação do K-Means  
Clientes são agrupados conforme padrões de recência, frequência e valor monetário.

### 10. Avaliação dos Clusters  
Uso do **Silhouette Score** para mensurar coesão e separação entre grupos.

### 11. Visualização dos Clusters  
Redução dimensional via **PCA** e plotagem dos clusters para facilitar interpretação.

### 12. Visualização dos Centróides  
Análise do comportamento médio de cada cluster, destacando diferenças entre grupos.

### 13. Indicadores dos Clusters  
Cálculo de métricas estratégicas:  
- Média de RFM por cluster  
- Tamanho de cada grupo  
- Participação na receita total  

Identificação dos principais perfis:  
- **Clientes VIP / Alta fidelidade:** compram com frequência, gastam muito e são recentes  
- **Engajados médios:** compram periodicamente, mas gastam menos  
- **Inativos / Recuperáveis:** clientes antigos com baixo volume  
- **Sazonais / Baixo valor:** compras pontuais e retorno limitado

---

## 🎯 Conclusão

Esse pipeline permite **segmentar clientes com base em comportamento real de compra**, fornecendo insights úteis para:  
- Estratégias de marketing  
- Programas de fidelidade  
- Retenção e recuperação de clientes  
- Personalização de campanhas

---

