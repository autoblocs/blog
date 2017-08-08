---
title: "Automatizando processos do DATASUS - Introdução"
excerpt: "Estimativa do custo anual das tabulações executas no **TabNET**"
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

Os dados de consulta ao [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) não são publicados com frequ6encia e estão desatualizados desde Maio/2016. Obtivemos no site do 15o. Congresso Nacional de Auditoria em Saúde e Qualidade da Gestão e da Assistência Hospitalar ([AUDHOSP](http://www.audhosp.com.br/)) uma apresentação da Divisão de Disseminação de Informações em Saúde que apresentou os dados totais de consultas ao [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) de Janeiro a Julho de 2016 com um total de [3.363.412 tabulações](/blog/assets/pdf/20160915-FEHOSP-DATASUS.pdf). Extrapolando esse número para o ano todo chegamos ao total de **5.765.849** tabulações no ano.

## Custo do funcionário por hora

Assumindo que a maioria das consultas é realizada por funcionários públicos nas esfereas federal, estadual e municipal, tomamos o salário médio mensal de [R$ 3.721,00](https://sidra.ibge.gov.br/tabela/5433#resultado) obtidos pela estimativa da [PNAD](http://www.ibge.gov.br/home/estatistica/indicadores/trabalhoerendimento/pnad_continua/) no site do [IBGE](http://www.ibge.gov.br/home/). Observe que o valor publicado pela pesquisa do [IBGE](http://www.ibge.gov.br/home/) não se refere ao custo do funcionário, mas ao **valor bruto mensal** recebido pelo indivíduo. Para facilitar as contas, iremos assumir um valor fixo igual a **1.333** referentes a férias, gratificação de natal (equivalente ao 13o. salário), etc.:

1. Custo mensal do servidor público : **R$ 4.961,33**;
2. Número de horas trabalhadas no mês:  **168**;
3. Custo total médiopor hora: **R$ 29,53**.

## Total de horas gasto por tabulação

Nossas estimativas internas são de que o tempo total de análise gasto para completar uma única tabulação é em média **5.5** horas. Esse processo compreende:

1. Ir no site do TabNET;
2. Escolher os parâmetros;
3. Fazer o download;
4. Organizar os dados;
5. Executar a análise;
6. Gerar os relatórios.

## Custo anual das tabulações executados no TabNET

O custo total anual é o produto do **número de tabulações** por ano pelo **tempo (horas)** gasto por tabulação pelo **valor hora** do trabalho:

1. Número de tabulações por ano: **5.765.849**;
2. Tempo (horas) gasto por tabulação: **5.5**;
3. Valor hora do trabalho: **R$ 29,53**.

Chegamos ao custo estimado ao ano de **R$ 936.515.735,79**.

## Análise
