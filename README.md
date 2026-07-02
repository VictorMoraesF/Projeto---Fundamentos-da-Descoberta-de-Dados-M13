# Projeto: Fundamentos da Descoberta de Dados - Supermercado (Chile)

Neste projeto, trabalhei com uma base de dados de produtos de um supermercado do Chile com o objetivo de aplicar os conceitos estatísticos e de visualização de dados que estudei no último módulo do curso. O foco principal foi realizar uma Análise Exploratória de Dados (EDA) para entender o comportamento dos preços, descontos e distribuições entre diferentes categorias e marcas.

---

## 📌 Estrutura do Conjunto de Dados

O conjunto de dados contém informações sobre os produtos comercializados, composto pelas seguintes colunas:
* **Title:** Nome do produto.
* **Marca:** Marca do produto.
* **Preco_Normal:** O preço em que o produto costuma ser vendido quando não há desconto.
* **Preco_Desconto:** O preço vendido após o desconto ser aplicado.
* **Preco_Anterior:** Preço em que era comercializado o produto antes do desconto aplicado.
* **Desconto:** Total de desconto aplicado.
* **Categoria:** Categoria do produto (em espanhol).

*Nota: Os campos com valor `0` representam produtos que não sofreram aplicação de descontos.*

---

## 🚀 Etapas do Projeto & Descobertas

### 1. Análise de Tendência Central (Média e Mediana)
Analisei as métricas de média e mediana para a coluna `Preco_Normal` agrupadas por categoria para identificar distorções nos preços.
* **Descoberta:** Identifiquei que quase todas as categorias (como *belleza-y-cuidado-personal*, *frutas*, *verduras*, *lacteos*, *congelados* e *instantaneos-e-sopa*) apresentam a **Média ACIMA da Mediana**, o que indica uma distribuição assimétrica à direita (presença de produtos muito caros que puxam a média para cima). A única exceção observada foi a categoria de *comidas-preparadas*.

### 2. Análise de Dispersão (Desvio Padrão)
Calculei o desvio padrão por categoria para medir a variabilidade dos preços.
* **Descoberta:** A categoria **Lácteos** destacou-se com o maior desvio padrão do conjunto de dados, apresentando uma média de `2385` e uma mediana de `989`. Essa grande diferença reforça a alta volatilidade e dispersão de preços dentro desta categoria.

### 3. Distribuição e Outliers (Boxplot)
Gerei um gráfico de caixa (*Boxplot*) focado na categoria de **Lácteos** (maior desvio padrão) recorrendo ao método `.loc[]` do Pandas. O gráfico permitiu visualizar claramente a dispersão dos dados e a forte presença de *outliers* (valores discrepantes) nos limites superiores de preço.

### 4. Visualização de Descontos por Categoria
Construí um gráfico de barras para comparar visualmente qual categoria do supermercado recebe, em média, o maior volume de descontos monetários.

### 5. Mapa Interativo de Descontos (Treemap/Sunburst)
Criei um gráfico interativo utilizando a biblioteca `Plotly`, agrupando os dados de forma hierárquica por **Categoria** e **Marca**, exibindo a média de desconto em cada segmento através de uma escala de cores intuitiva.

---

## 🛠️ Tecnologias Utilizadas

* **Python** (Linguagem principal)
* **Pandas** (Manipulação e tratamento de dados)
* **Matplotlib & Seaborn** (Visualizações estatísticas e gráficos estáticos)
* **Plotly Express** (Gráficos interativos e mapas de árvores dinâmicos)
* **Jupyter Notebook** (Ambiente de desenvolvimento)

---

## 📈 Como Executar o Projeto

1. Clona este repositório:
   ```bash
   git clone [https://github.com/TEU-USUARIO/TEU-REPOSITORIO.git](https://github.com/TEU-USUARIO/TEU-REPOSITORIO.git)
