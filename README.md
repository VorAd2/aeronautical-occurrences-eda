# ✈️ Análise Exploratória de Dados: Ocorrências Aeronáuticas no Brasil

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Este repositório é o trabalho final desenvolvido para a disciplina **Análise Exploratória de Dados (2026.1)**. O projeto realiza uma análise exploratória de dados sobre uma base pública de ocorrências aeronáuticas registradas no Brasil, investigando padrões de segurança operacional, perfil dos voos e danos humanos nos diferentes segmentos da aviação.

**Relatório Completo:** [relatorio.pdf](/relatorio.pdf)

---

## Objetivos da Análise

- **Análise de Severidade:** Avaliar a distribuição entre *Acidentes* e *Incidentes Graves*.
- **Perfil Temporal:** Mapear a evolução das ocorrências ao longo dos anos.
- **Porte Estrutural:** Investigar o comportamento estatístico do Peso Máximo de Decolagem (PMD).
- **Danos Humanos:** Quantificar lesões e fatalidades e cruzá-las com os tipos de operação aeronáutica.

---

## Principais Descobertas
- **Viés de Notificação:** Predominância de eventos estrutural ou biologicamente severos (Acidentes) na base pública devido às exigências regulatórias para essas ocorrências.
- **Concentração na Aviação Geral:** Voos privados, agrícolas e de instrução (todos não comerciais) respondem pela maior fatia do volume total de ocorrências e, portanto, concentram a maioria esmagadora dos acidentes aeronáuticos.
- **Assimetria do Porte (PMD):** A imensa maioria dos eventos envolve aeronaves de pequeno e médio porte (consequência da concentração das operações), enquanto jatos comerciais de grande porte atuam como outliers estatísticos.
- **Danos Humanos**: A maioria das ocorrências não resulta em óbitos humanos, ainda que os eventos de maior severidade estrutural sejam predominantes. Entretanto, as ocorrências biologicamente letais, ainda que raras, estão presentes e associadas, sobretudo, aos voos de grande porte.

---

## Tecnologias Usadas
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- LaTex
- Visual Studio Code
- Google Gemini

---

## Como Executar
Para fins didáticos, o seguinte passo a passo levará em consideração que o leitor possui instaladas as seguintes ferramentas:
- **Git**.
- **pyenv** (recomendado) ou **Python 3.11.5** instalado globalmente.
- **Visual Studio Code** e suas extensions para Python e Jupyter.

**Nota:** Caso o leitor já possua o Python 3.11.5 instalado globalmente em sua máquina, ignore os dois primeiros comandos do **Passo 2**.

### 1. Clone o repositório
```bash
git clone https://github.com/VorAd2/aeronautical-occurrences-eda
cd aeronautical-occurrences-eda
```

### 2. Configure o ambiente virtual
```bash
pyenv install 3.11.5
pyenv local 3.11.5

python -m venv .venv

# Linux/macOS:
source .venv/bin/activate
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
```

### 3. Instale as dependências
```bash
# Opção A: Autonomia para o pip decidir as versões compatíveis mais recentes das dependências.

pip install -r requirements.txt

# Opção B: Reproduza exatamente o ambiente de pacotes no qual este projeto foi desenvolvido e testado.

pip install -r requirements-lock.txt
```

### 4. Run!!
Existem duas formas simples de executar o notebook.

#### Opção A: Via VS Code
1. Com o diretório do projeto aberto no editor, abra o arquivo `main.ipynb`.
2. Procure a opção **Select Kernel** e escolha `.venv (3.11.5) (Python 3.11.5)`.
3. Clique no botão **Run All**.

#### Opção B: Via Terminal Interativo (Jupyter Notebook)
Com o ambiente virtual ativado em um terminal aberto no diretório, execute:
```bash
jupyter notebook main.ipynb
```

O projeto será aberto automaticamente no seu navegador padrão.

