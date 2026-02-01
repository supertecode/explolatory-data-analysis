# Análise Exploratória de Dados - Preços de Ações Mundiais

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/Status-Completo-success)]()

</div>

## 📋 Sumário

- [Visão Geral](#visão-geral)
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Análise Realizada](#análise-realizada)
- [Estrutura do Repositório](#estrutura-do-repositório)
- [Requisitos](#requisitos)
- [Como Utilizar](#como-utilizar)
- [Principais Descobertas](#principais-descobertas)
- [Autores](#autores)
- [Licença](#licença)

---

## 🎯 Visão Geral

Este projeto apresenta uma **Análise Exploratória de Dados (EDA)** completa sobre preços históricos de ações de empresas mundiais. O trabalho segue uma metodologia estruturada que inclui entendimento do problema, tratamento de dados, visualização e análise profunda dos padrões de mercado.

O dataset contém informações de preços de abertura, fechamento, máxima, mínima, volume de negociação e outras métricas de ações de múltiplas empresas, setores industriais e países.

---

## 🎓 Objetivo do Projeto

### Objetivo Geral

Realizar uma análise exploratória completa do comportamento do mercado de ações mundial, com foco especial em **Análise Setorial**, identificando padrões de negociação entre diferentes indústrias e compreender como diversos setores se comportam no mercado de valores.

### Objetivos Específicos

1. **Limpeza e Preparação de Dados**: Identificar e tratar valores ausentes, corrigir tipos de dados
2. **Análise Descritiva**: Compreender a distribuição, centralidade e dispersão das variáveis
3. **Análise Setorial**: Comparar volumes de negociação entre diferentes setores industriais
4. **Correlação de Variáveis**: Identificar relações entre preços (Open, Close, High, Low) e volume
5. **Identificação de Outliers**: Detectar anomalias usando técnicas estatísticas (boxplot, IQR)
6. **Seleção de Features**: Determinar quais variáveis seriam úteis para modelos de ML

---

## 📊 Análise Realizada

### Análise Setorial: Desempenho por Indústria

A análise escolhida foi a **Análise Setorial**, que explora como diferentes indústrias e setores estão se comportando no mercado de ações.

#### Etapas Executadas:

1. **Entendimento do Problema**
   - Exploração das características principais do dataset
   - Identificação dos campos relevantes para análise

2. **Tratamento dos Dados**
   - Conversão de tipos de dados (Date para datetime)
   - Verificação de valores nulos
   - Cálculo de cardinalidade das variáveis

3. **Visualização dos Dados**
   - Histogramas de volume por país
   - Boxplots para análise de dispersão
   - Scatter matrix e pairplot para correlações
   - KDE (Kernel Density Estimation) por país

4. **Análise Exploratória**
   - Análise interquartil (Q1, Q2, Q3) do volume
   - Heatmap de correlação entre variáveis numéricas
   - Identificação dos top 10 setores por volume de negociação

---

## 📁 Estrutura do Repositório

```
explolatory-data-analysis/
│
├── README.md                          # Este arquivo
├── requirements.txt                   # Dependências do projeto
├── .gitignore                         # Arquivo Git ignore
│
├── data/
│   └── README.md                      # Documentação sobre os dados
│   └── World-Stock-Prices-Dataset.csv # Dataset principal
│
├── notebooks/
│   └── Projeto_03.ipynb               # Notebook com análise completa
│
├── docs/
│   └── analise_setorial_resumo.md     # Resumo da análise executada
│
└── src/
    └── utils.py                       # Funções auxiliares (futuro)
```

### Descrição das Pastas

| Pasta        | Descrição                                        |
| ------------ | ------------------------------------------------ |
| `data/`      | Contém os arquivos de dados brutos e processados |
| `notebooks/` | Jupyter notebooks com análises e experimentos    |
| `docs/`      | Documentação complementar e relatórios           |
| `src/`       | Código reutilizável em Python                    |

---

## 🔧 Requisitos

### Sistema

- Python 3.8 ou superior
- pip ou conda

### Bibliotecas Principais

```
pandas==1.3.0+
numpy==1.21.0+
matplotlib==3.4.0+
seaborn==0.11.0+
jupyter==1.0.0+
ydata-profiling==3.1.0+
```

---

## 🚀 Como Utilizar

### 1. Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/explolatory-data-analysis.git
cd explolatory-data-analysis
```

### 2. Criar Ambiente Virtual (Recomendado)

```bash
# Com Python venv
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

# Ou com Conda
conda create -n eda python=3.9
conda activate eda
```

### 3. Instalar Dependências

```bash
pip install -r requirements.txt
```

### 4. Executar o Notebook

```bash
jupyter notebook notebooks/Projeto_03.ipynb
```

### 5. Gerar Relatório de Profiling (Opcional)

```bash
# O notebook já possui código para gerar o relatório
# Basta executar as células finais
```

---

## 💡 Principais Descobertas

### Dados Gerais

- **Total de Registros**: Múltiplas linhas com histórico de preços
- **Campos Principais**: Date, Open, High, Low, Close, Volume, Dividends, Stock Splits
- **Países Analisados**: 8 países representados no dataset
- **Setores**: Múltiplas indústrias e segmentos

### Insights Setoriais

- Os **Top 10 setores** foram identificados por volume de negociação
- Variação significativa de volume entre setores
- Setores tradicionais apresentam maior volume de negociação

### Padrões Identificados

- Forte correlação entre Open, High, Low e Close
- Volume apresenta distribuição variável por país
- Outliers detectados através da técnica de IQR
- KDE revela distribuições distintas por país

### Features para Modelos ML

As seguintes variáveis foram selecionadas como relevantes para modelos de aprendizado de máquina:

- ✅ Open (Preço de Abertura)
- ✅ High (Preço Máximo)
- ✅ Low (Preço Mínimo)
- ✅ Close (Preço de Fechamento)
- ✅ Volume (Volume de Negociação)

Variáveis excluídas:

- ❌ Date (informação de contexto, não preditiva)
- ❌ Dividends (muitos valores ausentes)
- ❌ Stock Splits (muitos valores ausentes)
- ❌ Brand_Name e Ticker (informações categóricas redundantes)

---

## 📈 Técnicas Utilizadas

| Técnica            | Descrição                                        |
| ------------------ | ------------------------------------------------ |
| **Histogramas**    | Visualização da distribuição de volume por país  |
| **Boxplot**        | Identificação de outliers e análise de dispersão |
| **Scatter Matrix** | Análise de correlações bivariadas                |
| **KDE**            | Estimação de densidade por kernel                |
| **Heatmap**        | Correlação entre variáveis numéricas             |
| **Cardinalidade**  | Análise de valores únicos por coluna             |
| **Análise IQR**    | Cálculo de Q1, Q2, Q3 e detecção de outliers     |
| **Profiling**      | Relatório automático com ydata-profiling         |

---

## 📚 Referências

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [ydata-profiling](https://pypi.org/project/ydata-profiling/)
- [Jupyter Notebook](https://jupyter.org/)

---

## 📝 Licença

Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para mais detalhes.

---

## 📧 Contato e Contribuições

Para dúvidas ou sugestões sobre este projeto:

- 📧 Entre em contato com os autores
- 🐛 Reporte problemas através de Issues
- 🔀 Contribuições são bem-vindas via Pull Requests

---

<div align="center">

**Desenvolvido para fins educacionais**

Última atualização: 2026

</div>
