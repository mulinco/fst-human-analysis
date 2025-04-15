
## 👩‍🔬 Autora

Maria Clara Pereira Rodrigues  
Graduanda em Ciências Biológicas - Genética (UFRJ)  
Contato: [LinkedIn](https://www.linkedin.com/in/mariaclararodrigues3113)

## 📚 Referências

- Jobling et al., 2013. Human Evolutionary Genetics.
- 1000 Genomes Project Consortium, 2015.
- Tishkoff & Verrelli, 2003.


# Análise de Diferenciação Genética Humana com FST

Este projeto foi desenvolvido como parte da disciplina de Genética de Populações no curso de Ciências Biológicas - Genética (UFRJ), com foco na análise de diferenciação genética entre superpopulações humanas utilizando o índice de fixação **FST**.

## 🔍 Objetivo

Calcular e explorar os valores de **FST** entre cinco superpopulações humanas a partir de dados de SNPs (polimorfismos de nucleotídeo único), comparando os cromossomos autossômicos com o cromossomo X e identificando regiões do genoma com alta diferenciação genética.

## 🧬 Dados

- Fonte: [1000 Genomes Project](https://www.internationalgenome.org)
- SNPs localizados em diferentes cromossomos (autossomos e cromossomo X)
- Superpopulações humanas:
  - Africanos
  - Europeus
  - Asiáticos do Leste
  - Asiáticos do Sul
  - Americanos

## ⚙️ Metodologia

- Cálculo de FST por SNP entre as populações.
- Identificação de outliers (valores de FST elevados).
- Análise de heterozigosidade observada vs. esperada.
- Estimativa do tamanho populacional efetivo (Ne).
- Visualização gráfica dos resultados.

Ferramentas utilizadas:

- `R` / `RStudio`
- Pacotes: `ggplot2`, `dplyr`, `tidyr`

## 📊 Resultados

- O cromossomo X apresentou maior diferenciação genética média que os autossomos.
- SNPs outliers foram identificados nos cromossomos 16, 18 e X.
- Genes associados aos outliers:
  - **SPRY3** (cromossomo 16)
  - **SMAD3** (cromossomo 18)
  - **FMR1** (cromossomo X)

Imagens geradas:
- `compfstcromhum.png`: comparação da distribuição de FST entre cromossomos.
- `outliers.png`: valores de FST para SNPs outliers.

## 📁 Organização do Projeto

📦 fst-human-analysis 
  ├── data/ # Dados utilizados 
  ├── figures/ # Gráficos gerados (.png) 
  ├── scripts/ # Scripts em R 
  ├── report.md # Relatório técnico detalhado 
  └── README.md # Apresentação geral do projeto
