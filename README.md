# 📊 GrafosAV1 - Trabalho

Projeto desenvolvido para a disciplina de **Grafos / Algoritmos**, utilizando **Java** e a biblioteca **algs4 (Princeton)** para leitura de arquivos e manipulação de dados.

O objetivo do projeto é **ler um dataset real de citações científicas**, construir um **grafo não direcionado**, calcular **graus dos vértices** e gerar **arquivos auxiliares para análise**.

---

# 📁 Estrutura do Projeto

| Arquivo | Descrição |
|------|------|
| `Main.java` | Classe principal responsável por executar o programa |
| `Grafo.java` | Implementação do grafo utilizando listas de adjacência |
| `Cit-HepTh.txt` | Dataset de entrada contendo as arestas do grafo |
| `graus.txt` | Arquivo gerado contendo o grau de cada vértice |
| `algs4.txt` | Arquivo convertido para o formato utilizado pela biblioteca algs4 |
| `grafosatt.ipynb` | Notebook utilizado para análise e geração de métricas do grafo |

---

# 📦 Dataset Utilizado

O projeto utiliza o dataset **Cit-HepTh**, que representa uma rede de **citações entre artigos científicos da área de High Energy Physics Theory**.

Cada linha do arquivo representa uma **aresta entre dois vértices**, indicando uma relação de citação entre artigos.

Linhas iniciadas com `#` são **comentários** e são ignoradas pelo programa durante a leitura.

---

# ⚙️ Funcionamento do Programa

O programa executa as seguintes etapas:

## 1️⃣ Leitura do Dataset

O arquivo `Cit-HepTh.txt` é lido linha por linha utilizando:

- `Scanner`
- `In` (biblioteca **algs4**)

Durante a leitura:

- Linhas vazias são ignoradas  
- Linhas iniciadas com `#` são descartadas  

---

## 2️⃣ Mapeamento dos Vértices

Os identificadores dos vértices presentes no dataset possuem valores muito grandes.  
Para facilitar o processamento e o armazenamento em memória, o programa realiza um **mapeamento desses identificadores para índices inteiros compactos**.

Esse processo permite que os vértices sejam representados internamente por valores sequenciais, tornando a manipulação da estrutura do grafo mais eficiente.

---

## 3️⃣ Construção do Grafo

O grafo é implementado utilizando **listas de adjacência**, uma estrutura eficiente para representar grafos.


---

# ▶️ Como Executar o Projeto

O projeto é dividido em **duas etapas principais**:

1. **Execução do código Java** para processar o dataset e gerar os arquivos auxiliares.  
2. **Execução do código Python** para análise do grafo e geração das métricas solicitadas.

---

# ☕ Etapa 1 — Executar o Código Java

Execute o programa Java para gerar os arquivos:
- graus.txt
- algs4.txt

- 
Esses arquivos serão utilizados posteriormente no código Python.

---

# 🐍 Etapa 2 — Utilizar o Arquivo no Código Python

Após gerar os arquivos `.txt` pelo programa Java, utilize o arquivo **`algs4.txt`** no notebook Python.

### Passos

1. Fazer **upload do arquivo `algs4.txt`** no notebook `grafosatt.ipynb`.

2. O código Python irá:

- Ler o grafo no **formato algs4**  
- Construir a **estrutura do grafo**  
- Gerar **visualizações**  
- Calcular **todas as métricas solicitadas no trabalho**

---

# 📊 Análises Realizadas

Entre as análises realizadas estão:

- Visualização do grafo  
- Métricas estruturais da rede  
- Análise de conectividade  
- Outras métricas de grafos solicitadas na atividade

---

# 🧰 Tecnologias Utilizadas

- **Java**
- **Python**
- **Biblioteca algs4**
- **Jupyter Notebook**
- **Estrutura de Dados – Grafos**

---


