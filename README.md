# Detecção de Outliers em Dados de Mercado 📊

Este projeto visa resolver um problema recorrente em **Inteligência de Mercado**: a inconsistência em bases de dados formadas por coleta manual.

Através da aplicação de métodos estatísticos descritivos, desenvolvi uma rotina para identificar valores anômalos (outliers) em listas de preços semanais, evitando distorções nas análises de média e tendências.

## 🎯 O Problema
No processo de monitoramento de mercado, a coleta de preços é feita semanalmente. Como a entrada de dados é muitas vezes manual, ocorrem erros de digitação (ex: um produto de valor 50 ser digitado como 500).
Sem uma validação estatística, esses erros ("sujeira nos dados") impactavam diretamente os indicadores e a tomada de decisão da empresa.

## 🛠 A Solução (Metodologia)
Utilizei o método do **Intervalo Interquartil (IQR)** para criar faixas de aceitação automática de valores, independente do tipo de produto.

A lógica aplicada:
1. **Cálculo dos Quartis:** Identificação do Q1 (25%) e Q3 (75%) da amostra semanal.
2. **IQR (Amplitude):** Q3 - Q1.
3. **Definição de Limites:**
   - *Limite Inferior* = Q1 - 1.5 * IQR
   - *Limite Superior* = Q3 + 1.5 * IQR
4. **Filtro Automático:** Valores que ultrapassam esses limites são segregados para revisão antes de entrarem na base final.

## 🚀 Resultados
- Maior agilidade no fechamento dos relatórios semanais.
- Eliminação de viés causado por erros de digitação ou margens anômolas.
- Padronização do critério de "erro".

## 🛠 Ferramentas Utilizadas
- **Microsoft Excel:** Para implementação da lógica e uso imediato pela equipe.
- **Estatística Descritiva:** Medidas de posição e dispersão.
- **Próximos Passos:** Estudo para implementação da rotina em **Python/R** para escalabilidade.
