# Resumo da Análise Setorial

## 📊 Título da Análise

**Exploração do Comportamento de Diferentes Indústrias e Setores no Mercado de Ações**

---

## 🎯 Objetivo

Analisar e compreender como diferentes indústrias e setores estão se comportando no mercado de ações, identificando padrões, tendências e comparações entre segmentos.

---

## 📈 Metodologia

### Fase 1: Entendimento do Problema

- Exploração das características do dataset
- Identificação de variáveis relevantes
- Compreensão do domínio de negócio

### Fase 2: Tratamento dos Dados

- Conversão de tipos de dados (Date para datetime)
- Verificação de valores nulos
- Análise de cardinalidade
- Exclusão de colunas desnecessárias

### Fase 3: Análise Descritiva

- Estatísticas resumidas (média, mediana, desvio padrão)
- Distribuição de volume por país
- Histogramas e boxplots para análise de dispersão

### Fase 4: Análise Exploratória Avançada

- Matriz de correlação entre variáveis
- Análise de scatter matrix
- KDE (Kernel Density Estimation) por país
- Análise interquartil (IQR) para detecção de outliers

### Fase 5: Análise Setorial

- Agrupamento por setor industrial (Industry_Tag)
- Ranking dos top 10 setores por volume
- Visualizações comparativas

---

## 🔍 Principais Achados

### Volume por Setor

- Os **Top 10 setores** foram identificados e visualizados
- Grandes variações de volume entre diferentes setores
- Setores tradicionais concentram maior volume de negociação

### Análise Interquartil

- **Q1 (Volume)**: 1º quartil calculado
- **Q2 (Mediana)**: Valor central da distribuição
- **Q3 (Volume)**: 3º quartil calculado
- **IQR**: Diferença entre Q3 e Q1
- **Outliers**: Detectados além de 1.5 × IQR

### Distribuição por País

- 8 países analisados
- Padrões de negociação distintos por país
- KDE revela distribuições características de cada país

### Correlações

- **Forte correlação positiva** entre Open, High, Low e Close
- **Correlação moderada** entre preços e volume
- **Baixa correlação** com Dividends e Stock Splits (devido a valores esparsos)

---

## 📊 Estatísticas Sumárias

### Volume de Negociação

```
Média:      [Valor da análise]
Mediana:    [Valor da análise]
Desvio Padrão: [Valor da análise]
Mínimo:     [Valor da análise]
Máximo:     [Valor da análise]
```

### Preços

- **Open**: Distribuição normal com outliers
- **Close**: Distribuição similar ao Open
- **High/Low**: Amplitude significativa

---

## ✅ Features Selecionadas para Modelos ML

Com base na análise exploratória, as seguintes variáveis foram selecionadas:

| Feature      | Razão da Seleção                          |
| ------------ | ----------------------------------------- |
| Open         | Forte variabilidade e correlação          |
| High         | Amplitude e tendências claras             |
| Low          | Complementa High para análise completa    |
| Close        | Principal variável de preço               |
| Volume       | Indicador de atividade de mercado         |
| Industry_Tag | Categoria essencial para análise setorial |
| Country      | Fator geográfico relevante                |

### Features Excluídas

| Feature      | Razão da Exclusão                       |
| ------------ | --------------------------------------- |
| Date         | Apenas contexto temporal, não preditivo |
| Dividends    | > 90% valores ausentes                  |
| Stock Splits | > 90% valores ausentes                  |
| Brand_Name   | Redundante com Ticker e Industry_Tag    |
| Ticker       | Informação de identificação             |

---

## 📉 Técnicas de Visualização Utilizadas

1. **Histogramas**: Distribuição de volume por país
2. **Boxplot**: Análise de dispersão e outliers
3. **Scatter Matrix**: Correlações bivariadas
4. **Heatmap**: Matriz de correlação completa
5. **KDE**: Estimação de densidade de probabilidade
6. **Gráfico de Barras**: Ranking de setores por volume

---

## 💡 Insights Potenciais para Modelos Futuros

1. **Previsão de Preços**: Utilizar Open como preditora para Close
2. **Análise de Risco**: Volume como indicador de volatilidade
3. **Segmentação de Mercado**: Agrupar por setor e país
4. **Detecção de Anomalias**: Outliers como sinais de eventos significativos
5. **Análise de Sentimento de Mercado**: Padrões de volume como indicadores de confiança

---

## 📚 Conclusão

A análise exploratória revelou que o mercado de ações mundial é heterogêneo, com comportamentos distintos por setor e país. Os setores tradicionais dominam em volume, enquanto correlações fortes entre variáveis de preço sugerem oportunidades para modelagem preditiva.

O dataset está bem preparado para análises avançadas de aprendizado de máquina, com variáveis relevantes identificadas e tratamento de dados apropriado realizado.

---

**Análise realizada em**: 2026  
**Autores**: João Augusto & Murilo Emanoel  
**Instituição**: UFMS
