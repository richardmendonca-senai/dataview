# Projeto de Análise e Exploração de Dados - Pipeline de Vendas

## Objetivo do Projeto
Este projeto foi desenvolvido como parte da disciplina de análise de dados com o objetivo de construir um pipeline (fluxo) completo de Ciência de Dados. O fluxo compreende desde a geração automatizada de dados sintéticos propositalmente corrompidos (dados sujos), passando por etapas rigorosas de limpeza, tratamento de inconsistências, detecção e remoção de outliers, engenharia de novas variáveis, até a exportação de métricas gerenciais e gráficos informativos para tomada de decisão.

---

## Instruções de Instalação e Execução

### Pré-requisitos
Para rodar este projeto, você precisará de acesso ao **Google Colab** (recomendado) ou a um ambiente local com **Python 3.8+** instalado.

### Como Executar no Google Colab:
1. Faça o download do arquivo `dataview.ipynb` deste repositório.
2. Abra o [Google Colab](https://colab.research.google.com/) e faça o upload do notebook.
3. Execute as células sequencialmente, de cima para baixo (pressionando `Shift + Enter` em cada uma).
4. O próprio script criará automaticamente a estrutura de pastas (`data/` e `outputs/`) e gerará todos os arquivos locais no ambiente virtual.

---

## Conceitos de Python e Análise de Dados Aplicados

O projeto cobre os requisitos técnicos exigidos na grade de avaliação, demonstrando maturidade em lógica e manipulação de dados:

* **Lógica de Programação & Estruturas de Dados:** Uso de loops (`for`), estruturas condicionais (`if/elif/else`), operadores lógicos/relacionais, e tipos de dados nativos (como dicionários compostos para relatórios).
* **Modularização e Boas Práticas:** Código 100% encapsulado em funções com parâmetros, retornos explícitos e documentado por `docstrings`.
* **Programação Funcional:** Demonstração de funções lambda e implementação de uma **Função de Ordem Superior** (`aplicar_transformacao`) que aceita funções de *callback*.
* **Tratamento de Strings com Regex:** Utilização do módulo `re` (`re.sub`) para colapsar espaços em branco extras em colunas textuais.
* **Manipulação Avançada de Dados (Pandas):** Uso de filtros booleanos, conversão de tipos (`astype`), tratamento de datas com o módulo `datetime` e agregação de dados com `.groupby()` e `.agg()`.
* **Performance Computacional (NumPy):** Conversão de colunas em Arrays, uso de operações vetorizadas, *Broadcasting* matemático para cálculo de participação percentual e uso do `np.select` para transformações condicionais de faixas de valor.
* **Estatística e Tratamento de Outliers (IQR):** Identificação e tratamento de valores discrepantes utilizando o Intervalo Interquartil ($1.5 \times IQR$).
* **Visualização de Dados (Matplotlib & Seaborn):** Geração de gráficos de Linha (sazonalidade mensal), Barras Horizontais (ranking de produtos) e Boxplot (distribuição por região), exportados em formato `.png`.
* **Persistência de Arquivos (I/O):** Leitura e escrita de arquivos em formatos distintos: **CSV** (com codificação `utf-8-sig` para compatibilidade com acentos no Excel) e **JSON** (com validação e leitura de confirmação de volta para a memória).

---

## Decisão de Versão do Dataset Final
Conforme orientação do projeto, a versão escolhida para consolidar a análise final e ser salva em `data/final/vendas_final.csv` foi a **Versão 2 (v2 - Outliers Tratados)**. 

* **Justificativa:** Optamos pela remoção dos outliers para garantir que as métricas de faturamento médio, ticket médio por região e resumos estatísticos gerenciais não fossem distorcidos por compras discrepantes e fora do padrão comum do dataset, gerando assim relatórios mais realistas para o negócio. A versão v1 (com outliers) foi devidamente preservada na pasta `data/processed/v1_com_outliers/` para fins de auditoria histórica.

---

##  Links do Projeto
* **Repositório Oficial:** https://github.com/richardmendonca-senai/dataview.git
* **Vídeo de Demonstração:** https://youtu.be/QGQQRb9il6Q
