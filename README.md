# Análise Preditiva de Popularidade de Jogos na Steam (Steam Dataset 2025)

Este repositório contém os códigos e experimentos desenvolvidos para o artigo científico **"Previsão de Popularidade de Jogos"**, submetido como requisito avaliativo da disciplina de Inteligência Artificial.

## 📄 Descrição do Projeto

O objetivo deste projeto é aplicar algoritmos de Machine Learning supervisionado para classificar jogos da plataforma Steam em duas categorias: **"Popular"** (Sucesso) ou **"Nicho"**.

Utilizando o [Steam Dataset 2025](https://www.kaggle.com/datasets/crainbramp/steam-dataset-2025-multi-modal-gaming-analytics), o projeto implementa um pipeline completo de Ciência de Dados:

1.  **Coleta Automatizada:** Integração via API `kagglehub` para download dinâmico dos dados mais recentes.
2.  **Pré-processamento e Limpeza:**
    * Filtragem de consistência monetária (apenas transações em USD).
    * Tratamento de ruídos em colunas numéricas (ex: correção de dados de idade corrompidos).
    * Engenharia de Features para criação da variável alvo baseada na mediana de recomendações.
3.  **Balanceamento de Classes:** Aplicação de **Random Undersampling** para corrigir a desproporção severa (12:1) entre jogos de nicho e populares, garantindo um treinamento imparcial.
4.  **Modelagem:** Treinamento e comparação de dois modelos distintos:
    * **Random Forest Classifier** (Ensemble)
    * **Multilayer Perceptron (MLP)** (Rede Neural Artificial)

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.x
* **Ambiente de Execução:** Google Colab / Jupyter Notebook
* **Principais Bibliotecas:**
    * `pandas` & `numpy`: Manipulação e álgebra linear.
    * `scikit-learn`: Modelagem preditiva, métricas e pré-processamento.
    * `kagglehub`: Download do dataset.
    * `matplotlib` & `seaborn`: Visualização de dados e matrizes de confusão.

## 🚀 Como Executar o Código

Você pode executar este projeto de duas formas: via Google Colab (recomendado) ou localmente.

### Opção 1: Google Colab (Recomendado)

1.  Faça o upload do arquivo `.ipynb` deste repositório para o seu Google Drive.
2.  Abra o arquivo com o **Google Colab**.
3.  No menu superior, clique em **Ambiente de Execução** > **Executar tudo** (ou *Runtime* > *Run all*).
    * *Nota: O código instalará automaticamente a biblioteca `kagglehub` necessária.*

### Opção 2: Execução Local

Certifique-se de ter o Python instalado. Recomenda-se o uso de um ambiente virtual (`venv`).

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/Samtlokomemo/projetofinalia.git
    cd projetofinalia
    ```

2.  **Instale as dependências:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn kagglehub
    ```

3.  **Execute o script:**
    Se estiver usando um arquivo Python (.py):
    ```bash
    python projetofinalia.py
    ```
    Se estiver usando Jupyter Notebook:
    ```bash
    jupyter notebook projetofinalia.ipynb
    ```

## 📊 Resultados Esperados

Ao rodar o código, serão gerados:
* Relatórios de classificação (`precision`, `recall`, `f1-score`) para ambos os modelos.
* Matrizes de Confusão gráficas comparando o desempenho nos dados de teste.
* Gráfico de importância das features (Feature Importance) do modelo Random Forest.

## 👥 Autores

* [Hugo Ryan da Conceição Lima](https://github.com/hugo-ryan)
* [Ingrid Vitória da Silva Conceição](https://github.com/Ingrid-Vitoriaa)
* [Samuel Rocha Maranhão](github.com/Samtlokomemo)
