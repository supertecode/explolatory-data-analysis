# Documentação dos Dados

## 📊 Dataset: World Stock Prices Dataset

### Fonte dos Dados

- **URL**: [Google Drive](https://drive.google.com/file/d/1nmefT107HGBN2WsrrBpVWxzWrMFSPtIq/view?usp=sharing)
- **Nome do Arquivo**: `World-Stock-Prices-Dataset.csv`
- **Formato**: CSV (Comma Separated Values)

### 📋 Descrição das Colunas

#### Colunas de Preços

| Campo     | Tipo     | Descrição                                       |
| --------- | -------- | ----------------------------------------------- |
| **Date**  | DateTime | Data de referência dos dados de preço           |
| **Open**  | Float    | Preço de abertura da ação nessa data            |
| **High**  | Float    | Maior preço que a ação atingiu durante o pregão |
| **Low**   | Float    | Menor preço que a ação atingiu durante o pregão |
| **Close** | Float    | Preço de fechamento da ação nessa data          |

#### Colunas de Volume e Ajustes

| Campo            | Tipo    | Descrição                                             |
| ---------------- | ------- | ----------------------------------------------------- |
| **Volume**       | Integer | Volume de negociação (número de ações negociadas)     |
| **Dividends**    | Float   | Dividendos pagos nessa data (se houver)               |
| **Stock Splits** | Float   | Informações sobre desdobramentos de ações (se houver) |

#### Colunas de Identificação

| Campo            | Tipo   | Descrição                                                |
| ---------------- | ------ | -------------------------------------------------------- |
| **Brand_Name**   | String | Nome da marca ou empresa                                 |
| **Ticker**       | String | Símbolo de ticker para identificar a ação                |
| **Industry_Tag** | String | Categoria de indústria ou setor ao qual a marca pertence |
| **Country**      | String | País onde a marca está sediada ou opera principalmente   |

---

### 🌍 Países Representados

O dataset contém dados de ações de empresas em 8 países diferentes, permitindo análises comparativas internacionais.

### 🏢 Setores Industriais

Múltiplos setores estão representados, incluindo:

- Tecnologia
- Saúde/Farmacêutica
- Financeiro
- Consumo
- Energia
- E outros

---

### 🔍 Características Estatísticas

#### Métricas de Qualidade

- **Valores Nulos**: Verificados durante a análise exploratória
- **Cardinalidade**: Variável por coluna (alguns campos com muitos valores únicos)
- **Outliers**: Detectados através de análise IQR e boxplot

#### Distribuição

- Volume de negociação apresenta distribuição variável por país
- Preços (Open, High, Low, Close) apresentam forte correlação positiva
- Dividendos e Stock Splits são campos esparsos (poucos valores)

---

### 💾 Como Acessar os Dados

1. **Diretamente no Notebook**: O arquivo CSV deve estar no mesmo diretório do notebook
2. **Com Pandas**:

```python
import pandas as pd
df = pd.read_csv('World-Stock-Prices-Dataset.csv')
```

### 📊 Tamanho do Dataset

- **Linhas**: Múltiplos registros históricos
- **Colunas**: 12 colunas principais
- **Tamanho**: Variável (confirir ao baixar)

---

### 🔄 Tratamento de Dados Aplicado

Durante a análise exploratória, foram aplicados os seguintes tratamentos:

1. **Conversão de Tipo**
   - Coluna `Date` convertida de Object para DateTime

2. **Análise de Valores Ausentes**
   - Verificação de NaN e valores nulos
   - Campos `Dividends` e `Stock Splits` com alta densidade de nulos

3. **Exclusão de Colunas**
   - `Date` (utilizada apenas para contexto)
   - `Dividends` e `Stock Splits` (muitos valores ausentes)
   - `Brand_Name` e `Ticker` (redundantes com Industry_Tag)

### ✅ Features Selecionadas para ML

As seguintes colunas foram selecionadas para futuros modelos de aprendizado de máquina:

- Open
- High
- Low
- Close
- Volume
- Industry_Tag (categórica)
- Country (categórica)

---

### 📚 Referências

- Dataset disponível em: [Google Drive](https://drive.google.com/file/d/1nmefT107HGBN2WsrrBpVWxzWrMFSPtIq/view?usp=sharing)
- Formato baseado em padrão OHLCV (Open-High-Low-Close-Volume)

---

**Última atualização**: 2026
