# 🚀 Guia de Instalação Rápida

## Pré-requisitos

- Python 3.8 ou superior
- pip ou conda
- Git (opcional)

---

## Opção 1: Instalação com pip + venv

### 1️⃣ Criar ambiente virtual

```bash
python -m venv venv
```

### 2️⃣ Ativar ambiente virtual

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 3️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

### 4️⃣ Executar Jupyter

```bash
jupyter notebook notebooks/Projeto_03.ipynb
```

---

## Opção 2: Instalação com Conda

### 1️⃣ Criar ambiente Conda

```bash
conda create -n eda python=3.9
conda activate eda
```

### 2️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

### 3️⃣ Executar Jupyter

```bash
jupyter notebook notebooks/Projeto_03.ipynb
```

---

## Verificação de Instalação

Para verificar se tudo foi instalado corretamente:

```bash
python -c "import pandas; import numpy; import matplotlib; print('✓ Instalação OK!')"
```

---

## Solução de Problemas

### ❌ Erro: "jupyter not found"

```bash
pip install jupyter
```

### ❌ Erro: "No module named pandas"

```bash
pip install pandas
```

### ❌ Ambiente virtual não ativa

- Windows: Tente usar `python -m venv venv` ao invés de `virtualenv`
- Linux/Mac: Use `source venv/bin/activate`

### ❌ Porta Jupyter já em uso

```bash
jupyter notebook --port 8889 notebooks/Projeto_03.ipynb
```

---

## Próximos Passos

1. Abra o notebook em seu navegador
2. Execute as células sequencialmente
3. Experimente modificar análises
4. Verifique a documentação em `/docs`

---

**Dúvidas?** Consulte o README.md principal para mais informações.
