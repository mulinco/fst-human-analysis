---
title: "Análise de Diferenciação Genética Humana com FST"
author: "Maria Clara Pereira Rodrigues"
date: "2024-11-22"
output: github_document
---


# Relatório Técnico: Diferenciação Genética Humana com FST

Este relatório apresenta os resultados da análise de diferenciação genética entre superpopulações humanas com base no índice de fixação FST, usando dados do 1000 Genomes Project.

## 1. Introdução

O índice de fixação **FST** é uma medida estatística que expressa a proporção da variação genética total que pode ser atribuída a diferenças entre populações. Valores próximos a 0 indicam pouca diferenciação, enquanto valores próximos a 1 indicam diferenciação significativa. Essa métrica é importante para compreender padrões evolutivos, históricos e adaptativos entre populações humanas.

## 2. Objetivos

- Calcular FST para SNPs em diferentes cromossomos.
- Comparar a variação de FST entre os autossomos e o cromossomo X.
- Identificar SNPs com alta diferenciação genética (outliers) e associá-los a genes e fenótipos.
- Calcular a heterozigosidade esperada e observada.
- Estimar o tamanho populacional efetivo (Ne) para cada superpopulação.

## 3. Metodologia

- Linguagem: R (RStudio)
- Pacotes principais: `ggplot2`, `dplyr`, `tidyverse`
- Cálculo de FST por SNP
- Gráficos de distribuição de FST e identificação de outliers
- Cálculo de heterozigosidade observada (Ho)
- Estimativa de Ne com base em Ho e taxa de mutação (1.5 × 10⁻⁸)

## 4. Resultados

### 4.1 Comparação de FST entre cromossomos

📷 `figures/compfstcromhum.png`  
Os autossomos mostraram baixa diferenciação genética (FST < 0.05 na maioria dos SNPs). O cromossomo X apresentou FST mais elevados, indicando possível ação de deriva genética mais intensa ou seleção específica.

### 4.2 SNPs Outliers

📷 `figures/outliers.png`  
Foram identificados 5 SNPs com FST altos nos cromossomos X, 11, 15, 16 e 18.

- **Cromossomo 16 (SPRY3)**  
  Regula sinalização celular. Variações podem afetar desenvolvimento embrionário e predisposição a cânceres.

- **Cromossomo 18 (SMAD3)**  
  Atua na via TGF-β. Variações associadas a fibrose em órgãos como pulmão, fígado e rins.

- **Cromossomo X (FMR1)**  
  Responsável pela Síndrome do X Frágil, causa hereditária comum de deficiência intelectual e comportamentos autistas.

### 4.3 Heterozigosidade esperada vs. observada

- **He (esperada)**: 0.0009
- **Ho (observada)**:
  - Autossomos: 0.0287
  - Cromossomo X: 0.0162

A heterozigosidade observada é bem maior que a esperada, refletindo a expansão populacional recente, fluxo gênico e seleção equilibrada.

### 4.4 Tamanho populacional efetivo (Ne)

Calculado a partir de Ho:

| Superpopulação      | Ne estimado     |
|---------------------|-----------------|
| Africanos           | 582.740         |
| Asiáticos do Sul    | 497.975         |
| Asiáticos do Leste  | 482.024         |
| Europeus            | 499.216         |
| Americanos          | 521.170         |

Populações africanas apresentam o maior Ne, refletindo sua maior diversidade genética, de acordo com a origem africana da espécie humana.

## 5. Discussão

A diferenciação observada entre os cromossomos pode ser explicada por fenômenos como seleção natural, deriva genética e desequilíbrio de ligação. O cromossomo X, por possuir um Ne menor e herança desigual entre os sexos, tende a ser mais sensível à seleção e à deriva, o que justifica os valores mais altos de FST.

## 6. Desafio: Viés de Aquisição

Para reduzir o viés causado pela análise apenas de posições variantes, é recomendável:

- Incluir posições conservadas.
- Trabalhar com dados genômicos completos (exoma ou genoma inteiro).
- Corrigir viés de cobertura em dados de sequenciamento.
- Aplicar métodos estatísticos que ajustem esse viés.

## 7. Referências

- Jobling, M. A. et al. (2013). *Human Evolutionary Genetics*.
- 1000 Genomes Project Consortium (2015). *Nature*, 526, 68–74.
- Tishkoff, S. A., Verrelli, B. C. (2003). *Ann Rev Genomics Hum Genet*.
- Li, H., Durbin, R. (2009). *Bioinformatics*, 25(14), 1754–1760.

---

