# 🏥 Análise e Tratamento de Dados na Área da Saúde

Projeto desenvolvido em Python utilizando Google Colab com foco em **limpeza, transformação e análise exploratória de dados (EDA)** aplicados a uma base de dados da área da saúde.

---

## 📖 Sobre o Projeto

Este projeto tem como objetivo demonstrar as principais etapas do processo de preparação de dados para projetos de Ciência de Dados.

A base utilizada contém informações fictícias de pacientes e foi criada com inconsistências intencionais para simular problemas encontrados em bases reais, como:

* Valores ausentes;
* Dados inconsistentes;
* Formatos diferentes para a mesma informação;
* Problemas de padronização textual;
* Campos incompletos.

Durante o projeto foram aplicadas técnicas de **Data Cleaning**, **Data Wrangling** e **Análise Exploratória de Dados (EDA)**.

---

## 🎯 Objetivos

* Identificar problemas de qualidade dos dados;
* Tratar valores ausentes;
* Padronizar informações categóricas;
* Corrigir formatos inconsistentes;
* Validar cálculos existentes;
* Produzir análises estatísticas;
* Gerar visualizações para apoio à tomada de decisão.

---

## 🛠️ Tecnologias Utilizadas

* Python 3
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn

---

## 📂 Estrutura da Base de Dados

| Variável         | Descrição                |
| ---------------- | ------------------------ |
| id_paciente      | Identificador único      |
| nome             | Nome do paciente         |
| idade            | Idade                    |
| sexo             | Sexo                     |
| cidade           | Cidade                   |
| estado           | Estado                   |
| peso_kg          | Peso corporal            |
| altura_m         | Altura                   |
| imc              | Índice de Massa Corporal |
| pressao_arterial | Pressão arterial         |
| glicemia         | Índice glicêmico         |
| colesterol       | Nível de colesterol      |
| diagnostico      | Diagnóstico clínico      |

---

## 🔎 Etapas Realizadas

### 1. Inspeção Inicial dos Dados

* Verificação da estrutura da base;
* Identificação dos tipos de dados;
* Estatísticas descritivas iniciais;
* Verificação de valores ausentes.

### 2. Limpeza dos Dados

Foram realizadas as seguintes correções:

#### Padronização da variável sexo

```text
M, m → Masculino
F, f → Feminino
```

#### Padronização de cidades e estados

```text
Campos Dos Goytacazes
RIO DE JANEIRO
```

#### Padronização da pressão arterial

```text
120/80 → 120x80
```

#### Conversão de valores numéricos

```text
75,5 → 75.5
```

#### Remoção de registros inválidos

* Idades nulas;
* Idades iguais a zero.

### 3. Engenharia de Atributos

Foi criado um novo campo:

* `imc_calculado`

Utilizando a fórmula:

```python
IMC = peso / (altura ** 2)
```

Também foram criadas categorias de faixa etária:

* Criança
* Adolescente
* Adulto Jovem
* Adulto
* Idoso

### 4. Tratamento de Diagnósticos Ausentes

Os diagnósticos faltantes foram preenchidos com base na classificação do IMC.

| IMC         | Classificação |
| ----------- | ------------- |
| < 18.5      | Baixo Peso    |
| 18.5 – 24.9 | Saudável      |
| 25.0 – 29.9 | Sobrepeso     |
| ≥ 30.0      | Obesidade     |

---

## 📊 Análise Exploratória de Dados (EDA)

Foram produzidas análises envolvendo:

* Distribuição etária;
* Distribuição por sexo;
* Frequência dos diagnósticos;
* Glicemia média por faixa etária;
* Colesterol médio por faixa etária;
* Comparação entre homens e mulheres;
* Heatmap de correlação.

---

## 📈 Principais Resultados

### Correlação entre IMC e Glicemia

```text
r = -0,04
```

Resultado indica ausência de correlação linear significativa.

### Correlação entre IMC e Colesterol

```text
r = -0,02
```

Também não foi observada correlação relevante.

### Distribuição Etária

A maior concentração de pacientes encontra-se na faixa de idosos, seguida pelos grupos adultos.

---

## 📚 Conceitos Aplicados

Durante o desenvolvimento foram aplicados conceitos de:

* Data Cleaning
* Data Wrangling
* Data Validation
* Missing Values Treatment
* Exploratory Data Analysis (EDA)
* Descriptive Statistics
* Correlation Analysis
* Feature Engineering
* Data Visualization

---

## 🚀 Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

### 2. Instale as dependências

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Execute o Notebook

Abra o notebook no Google Colab ou Jupyter Notebook e execute as células em sequência.

---

## 📁 Estrutura do Projeto

```text
📦 Analize_e_Tratamento_de_Dados_Saúde
├── 📁 Graficos
│
├── 📄 Analize_e_Tratamento_de_Dados_Saúde.ipynb
├── 📄 analize_e_tratamento_de_dados_saude.py
│
├── 📄 base_saude_1500_linhas.csv
├── 📄 Dados_brutos.xlsx
├── 📄 Dados_limpos.xlsx
│
├── 📄 README.md
├── 📄 Relatório de Progresso – Tratamento e Análise de Dados.pdf
└── 📄 requirements.txt
```


---

## 🎓 Objetivo Acadêmico

Este projeto foi desenvolvido como atividade prática de Ciência de Dados aplicada à área da saúde, com foco no aprendizado de técnicas de preparação, tratamento e análise exploratória de dados utilizando Python.

---

## 👨‍💻 Autor

**Jorge Dias**

* Engenharia de Computação – UCAM
* Pós-graduação em Java
* Estudante de Data Science e Análise de Dados

### Contato

* LinkedIn: https://www.linkedin.com/in/jfdias/
* GitHub: https://github.com/JorgeFilipi
