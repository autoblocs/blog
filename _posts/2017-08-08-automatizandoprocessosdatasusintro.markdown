---
title: "Automatizando os processos do DATASUS - I"
excerpt: "Estimativa do custo anual das análise executadas no **TabNET**"
date: "2017-08-08 10:36:29 -0400"
category:
  - Saude Publica
tags:
  - Brasil
  - DATASUS
  - Big Data
---

## Introdução

Mais de 5.7 milhões de consultas são realizadas no [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) por ano. Estimamos que o tempo gasto nessas operações custe em torno de 900 milhões de reais. Utilizamos os dados da [PNAD](http://www.ibge.gov.br/home/estatistica/indicadores/trabalhoerendimento/pnad_continua/) e das consultas realizadas no [DATASUS](http://www2.datasus.gov.br/DATASUS/Estatisticas_TABNET_5_2016/Mtab2016.htm) extrapoladas para o ano de 2016.

## Número de consultas

Os dados de consulta ao [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) não são publicados com frequência e estão desatualizados desde Maio/2016. Obtivemos no site do 15o. Congresso Nacional de Auditoria em Saúde e Qualidade da Gestão e da Assistência Hospitalar ([AUDHOSP](http://www.audhosp.com.br/)) uma apresentação da Divisão de Disseminação de Informações em Saúde que apresentou os dados totais de consultas ao [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) de Janeiro a Julho de 2016 com um total de [3.363.412 tabulações](/blog/assets/pdf/20160915-FEHOSP-DATASUS.pdf). Extrapolando esse número para o ano todo chegamos ao total de **5.765.849** tabulações no ano de 2016.

## Custo do funcionário por hora

Assumindo que a maioria das consultas é realizada por funcionários públicos nas esferas federal, estadual e municipal, tomamos o salário médio **mensal** de [R$ 3.721,00](https://sidra.ibge.gov.br/tabela/5433#resultado) obtidos pela estimativa da [PNAD](http://www.ibge.gov.br/home/estatistica/indicadores/trabalhoerendimento/pnad_continua/) no site do [IBGE](http://www.ibge.gov.br/home/). Observe que o valor publicado pela pesquisa do [IBGE](http://www.ibge.gov.br/home/) não se refere ao custo do funcionário, mas ao **valor bruto mensal** recebido.

Para calcular o custo mensal do funcionário, adicionamos a provisão mensal dos valores pagos anualmente a título de férias, gratificação de Natal, etc. Esses valores são calculados como:

1.  Férias: 1/12 do salário mensal
2.  Gratificação de Natal (equivalente ao 13&ordm; salário): 1/12 do salário mensal

De modo que chegamos ao fator de ajuste do salário mensal igual a **1,17**. Devemos multiplicar esse fator ao salário médio [R$ 3.721,00](https://sidra.ibge.gov.br/tabela/5433#resultado) oriundo da pesquisa da [PNAD](http://www.ibge.gov.br/home/estatistica/indicadores/trabalhoerendimento/pnad_continua/). Para calcular o custo do funcionário por hora temos que dividir o custo total médio mensal pelo número de horas trabalhadas:

1.  Custo mensal total médio do servidor público: **R$ 4.341,17**;
2.  Número de horas trabalhadas no mês:  **168**;
3.  Custo total médio por hora: **R$ 25,84**.

## Total de horas gasto por análise

Estimamos que o tempo total gasto para completar uma análise por tabulação é de aproximadamente **6** horas. Esse trabalho é feito manualmente, todos os meses, em todas secretarias de saúde do Brasil. O processo tem os seguintes passos:

1.  Ir no site do TabNET;
2.  Escolher os parâmetros;
3.  Fazer o download;
4.  Organizar os dados;
5.  Executar a análise;
6.  Gerar os relatórios.

## Custo anual das análises executados no TabNET

O custo total anual é o produto do **número de tabulações** por ano pelo **tempo (horas)** gasto por tabulação pelo **valor hora** do trabalho:

1.  Número de tabulações por ano: **5.765.849**;
2.  Tempo (horas) gasto por tabulação: **6**;
3.  Valor hora do trabalho: **R$ 25,84**.

Assim, estimamos que o custo anual pelo sistema vigente é de **R$ 893.946.838,71**.
