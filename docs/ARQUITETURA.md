# 📐 Documentação da Arquitetura do Projeto

## Visão Geral da Estrutura

```
explolatory-data-analysis/
│
├── 📄 README.md                    ← COMECE AQUI! Documentação principal
├── 📄 SETUP.md                     ← Guia rápido de instalação
├── 📄 requirements.txt             ← Dependências do projeto
├── 📄 .gitignore                   ← Configuração Git
│
├── 📁 data/                        ← Dados e metadados
│   ├── 📄 README.md               (Documentação dos dados)
│   └── 📊 World-Stock-Prices-Dataset.csv  (Dataset principal - baixar de link)
│
├── 📁 notebooks/                   ← Análises e experimentos
│   └── 📓 Projeto_03.ipynb        (Análise Exploratória completa)
│
├── 📁 docs/                        ← Documentação adicional
│   └── 📄 analise_setorial_resumo.md  (Resumo dos achados)
│
└── 📁 src/                         ← Código reutilizável (futuro)
    └── (Funções auxiliares, utilitários)
```

---

## 📂 Descrição de Cada Diretório

### 🔹 Raiz do Projeto

| Arquivo              | Propósito                              |
| -------------------- | -------------------------------------- |
| **README.md**        | Documentação completa do projeto       |
| **SETUP.md**         | Instruções de instalação passo-a-passo |
| **requirements.txt** | Lista de dependências Python           |
| **.gitignore**       | Arquivos ignorados pelo Git            |

### 🔹 `/data` - Dados

**Responsabilidade**: Armazenar dados brutos, processados e documentação relacionada.

```
data/
├── README.md                           (Documentação dos dados)
└── World-Stock-Prices-Dataset.csv      (Dataset principal)
```

**Convenção de Nomenclatura**:

- Dados brutos: `original_*` ou `raw_*`
- Dados processados: `processed_*`
- Dados intermediários: `interim_*`

**Como usar**:

```python
import pandas as pd
df = pd.read_csv('data/World-Stock-Prices-Dataset.csv')
```

### 🔹 `/notebooks` - Jupyter Notebooks

**Responsabilidade**: Análises exploratórias, experimentos e prototipagem.

```
notebooks/
└── Projeto_03.ipynb                    (Análise Exploratória de Dados)
```

**Convenção de Nomenclatura**:

- `01_data_exploration.ipynb`
- `02_eda_analysis.ipynb`
- `03_model_training.ipynb`

**Boas Práticas**:

- Mantenha notebooks limpos e bem documentados
- Use títulos e markdown para seções
- Documente descobertas importantes
- Reutilize código em `/src`

### 🔹 `/docs` - Documentação

**Responsabilidade**: Documentação do projeto, relatórios e insights.

```
docs/
├── analise_setorial_resumo.md          (Resumo da análise realizada)
└── (Outros relatórios e documentação)
```

**Tipos de Documentos**:

- `*_summary.md` - Resumos de análises
- `*_report.md` - Relatórios detalhados
- `methodology.md` - Explicação de metodologias
- `findings.md` - Descobertas principais

### 🔹 `/src` - Código Reutilizável

**Responsabilidade**: Código Python que pode ser importado e reutilizado.

```
src/
├── __init__.py
├── data_processing.py
├── visualization.py
└── utils.py
```

**Uso no Notebook**:

```python
import sys
sys.path.append('../src')
from data_processing import load_data, clean_data
```

---

## 🔄 Fluxo de Trabalho Recomendado

### 1️⃣ **Setup Inicial**

```bash
# Clone ou abra o repositório
cd explolatory-data-analysis

# Siga SETUP.md para instalar dependências
cat SETUP.md
```

### 2️⃣ **Compreender o Projeto**

- Leia [README.md](README.md) - Visão geral e contexto
- Leia [data/README.md](data/README.md) - Estrutura dos dados
- Leia [docs/analise_setorial_resumo.md](docs/analise_setorial_resumo.md) - Análises realizadas

### 3️⃣ **Executar Análise**

```bash
jupyter notebook notebooks/Projeto_03.ipynb
```

### 4️⃣ **Explorar e Modificar**

- Execute células sequencialmente
- Experimente alterações
- Documente suas descobertas

### 5️⃣ **Reutilizar Código**

- Mova funções úteis para `/src`
- Importe em novos notebooks
- Mantenha código DRY (Don't Repeat Yourself)

---

## 📊 Metadados do Projeto

| Propriedade         | Valor                                                    |
| ------------------- | -------------------------------------------------------- |
| **Nome**            | Análise Exploratória de Dados - Preços de Ações Mundiais |
| **Versão**          | 1.0.0                                                    |
| **Autores**         | João Augusto (ADS), Murilo Emanoel (BCC)                 |
| **Instituição**     | UFMS                                                     |
| **Linguagem**       | Python 3.8+                                              |
| **Licença**         | MIT                                                      |
| **Data de Criação** | 2026                                                     |
| **Status**          | ✅ Completo                                              |

---

## 🛠️ Padrões de Código

### Imports

```python
# Padrão recomendado
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Dados
from src.data_processing import load_data, clean_data

# Visualização
from src.visualization import plot_distribution, plot_correlation
```

### Documentação de Funções

```python
def analyze_sector(df, sector_name):
    """
    Analisa dados de um setor específico.

    Parameters
    ----------
    df : pd.DataFrame
        DataFrame com dados de ações
    sector_name : str
        Nome do setor a analisar

    Returns
    -------
    dict
        Estatísticas do setor
    """
    pass
```

### Variáveis

- `df`, `df_raw`, `df_clean` para DataFrames
- `fig`, `ax` para matplotlib
- `config`, `params` para parâmetros
- Use snake_case para variáveis

---

## 📈 Próximas Etapas

### Curto Prazo

- [ ] Documentar mais detalhadamente cada célula do notebook
- [ ] Criar testes unitários para funções em `/src`
- [ ] Adicionar mais análises específicas por setor

### Médio Prazo

- [ ] Treinar modelos de previsão com as features selecionadas
- [ ] Criar visualizações interativas com plotly
- [ ] Implementar pipeline de data processing automatizado

### Longo Prazo

- [ ] Desenvolver aplicação web para visualização
- [ ] Integrar dados em tempo real
- [ ] Criar API para consultas
- [ ] Expandir análise para más valores históricos

---

## 🤝 Como Contribuir

1. Crie uma branch para sua feature: `git checkout -b feature/nova-analise`
2. Commit suas mudanças: `git commit -m 'Adiciona nova análise'`
3. Push para a branch: `git push origin feature/nova-analise`
4. Abra um Pull Request

---

## 📞 Suporte

Para dúvidas ou problemas:

1. Consulte a documentação em `/docs`
2. Verifique o SETUP.md para problemas de instalação
3. Revise análises anteriores em `/notebooks`
4. Entre em contato com os autores

---

<div align="center">

**Versão 1.0.0** | Última atualização: 2026

Documentação da Arquitetura

</div>
