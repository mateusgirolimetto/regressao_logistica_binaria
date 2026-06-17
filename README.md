# Regressão Logística Binária — Predição de Diabetes

Este projeto aplica um modelo de **regressão logística binária** (GLM) para prever o diagnóstico de diabetes a partir de variáveis clínicas e sociodemográficas.

## Conteúdo

- `Regressão Logística Binária.Rmd`: script em R Markdown com todo o pipeline de análise.

## Pipeline da análise

1. **Carregamento e pré-processamento dos dados**: leitura do dataset e conversão de variáveis categóricas em fatores (sexo, etnia, escolaridade, renda, status de emprego, tabagismo, histórico familiar, entre outras).
2. **Divisão treino/teste**: separação dos dados em 90% treino e 10% teste, de forma estratificada.
3. **Validação cruzada (10-fold)**: controle de treinamento com predições out-of-fold (OOF) e métrica ROC.
4. **Ajuste do modelo GLM logístico**: treinamento do modelo com padronização das variáveis (centralização e escala).
5. **Avaliação do modelo**: coeficientes, intervalos de confiança, odds ratios (exponencial dos coeficientes).
6. **Curva ROC e AUC**: cálculo da área sob a curva a partir das predições OOF.
7. **Definição de threshold**: escolha do ponto de corte que garante sensibilidade ≥ 0.9.
8. **Avaliação no conjunto de teste**: matriz de confusão aplicando o threshold definido.

## Requisitos

- R (versão recente)
- Pacotes: `readr`, `caret`, `dplyr`, `pROC`

## Autor

Mateus Vieira Girolimetto
