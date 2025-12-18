# 🌾 Análise de Outliers em Vendas Agrícolas

Este projeto tem como objetivo demonstrar técnicas de **Análise Exploratória de Dados (EDA)** e **Detecção de Anomalias** utilizando Python e Excel. 

O script gera uma base de dados fictícia de vendas de produtos agrícolas e aplica métodos estatísticos para identificar transações com valores discrepantes (outliers), que podem indicar erros de digitação ou fraudes.

## 🎯 Objetivo do Projeto
- **Gerar dados sintéticos:** Criação de um dataset realista de vendas (com clientes, datas e produtos agrícolas) sem expor dados sensíveis reais, utilizando a biblioteca `Faker`.
- **Análise Estatística:** Cálculo de Quartis (Q1, Q3) e Intervalo Interquartil (IQR) para estabelecer limites de preços aceitáveis.
- **Detecção de Anomalias:** Classificação automática de vendas como "Normal" ou "Outlier" se o valor fugir do padrão estatístico do produto.

## 🛠️ Tecnologias Utilizadas
- **Python** (Linguagem principal)
- **Pandas** (Manipulação e análise de dados)
- **Faker** (Geração de dados fictícios)
- **Excel** (Exportação e visualização final)

## 📊 Metodologia (Como funciona)
O algoritmo segue a lógica do **Box Plot** para identificar outliers:

1.  Agrupa as vendas por `Produto`.
2.  Calcula o **1º Quartil (25%)** e o **3º Quartil (75%)** dos preços unitários.
3.  Define o **IQR** (Amplitude Interquartil).
4.  Calcula os limites de corte:
    - *Limite Superior* = Q3 + 1.5 * IQR
    - *Limite Inferior* = Q1 - 1.5 * IQR
5.  Qualquer venda acima do limite superior ou abaixo do inferior é marcada como **"Outlier"**.

## 🚀 Como Executar 
Trabalhando em Excel:
Crie ou colete dados ficticios.
Exporte seus dados para Excel, desevolva os quartis no excel.
Utilize uma coluna auxiliar para determinar quais dados são outliers.
Faça a média desconsiderando os outliers.

Em Python:
Instale as bibliotecas: faker pandas openpyxl
Desenvolva seus dados
Crie um comando que detecta quais são os Outleirs

---
*Este projeto foi desenvolvido para fins de estudo e portfólio na área de Análise de Dados.*
Análise de outliers diretamente no Excel: [dados_ficticios_vendas.xlsx](https://github.com/user-attachments/files/24243851/dados_ficticios_vendas.xlsx)
Análise de outliers diretamente no Python: [analise_outliers.xlsx](https://github.com/user-attachments/files/24243867/analise_outliers.xlsx)

