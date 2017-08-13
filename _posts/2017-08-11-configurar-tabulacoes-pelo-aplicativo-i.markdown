---
title: Configurar tabulações no aplicativo [Autoblocs Saúde](http://app.autoblocs.com) - Parte I
excerpt: Exemplos de tabulações para o sistema [SIH/SUS](http://sihd.datasus.gov.br/principal/index.php) na cidade de Campinas (SP) - Junho/2016.
date: "2017-08-11 17:08"
header:
  teaser: /assets/images/pexels-photo-256517.jpeg
category:
  - Saude Publica
tags:
  - Brasil
  - DATASUS
  - Big Data
  - Autoblocs Saude
  - SIH
---

No último post apresentamos os princípios utilizados no desenvolvimento do aplicativo Autoblocs Saúde: **Disponibilidade**, **Usabilidade**, **Qualidade** e **Automação**. Discutiremos os elementos da interface que facilitam a construção de tabulações pelos usuários.

## Nomenclatura dos campos

O sistema TabNET/TabWIN utiliza uma nomenclatura própria para definir quais transformações serão aplicadas nas colunas das tabelas. Vejamos um exemplo para a cidade de Campinas/SP.

1.  Sistema SUS: Sistema de Informação Hospitalar [SIH/SUS](http://sihd.datasus.gov.br/principal/index.php);
2.  Arquivo do Sistema: Arquivos de internação hospitalar resumidos [RD](/assets/pdf/IT_SIHSUS_1603.pdf);

Esse arquivo possui 121 colunas, portanto utilizaremos apenas 3 colunas para facilitar a explicação:

`Diag CID10 (capit)`|`Hospital SP (CNES)`|`Valor Serv.Hospit.`
-----------|------|-------
T87|3001466|170,12
I60|2081695|6377,05
S33|2081695|941,88

A descrição dos campos é a seguinte:

1.  `Diag CID10 (capit)`: Código de diagnóstico principal de acordo com a tabela [CID-10](http://www.datasus.gov.br/cid10/V2008/download.htm);
2.  `Hospital SP (CNES)`: Código de cadastro no *Cadastro Nacional de Estabelecimentos de Saúde* [CNES](http://cnes.saude.gov.br/);
3.  `Valor Serv.Hospit.`: Valor dos serviços hospitalares (em [R$](<https://pt.wikipedia.org/wiki/Real_(moeda)>)).
1.  Linhas são os campos que serão tabulados nas linhas;
2.  Colunas são os campos que serão tabulados nas colunas;
3.  Incrementos são os campos numéricos que serão tabulados nas colunas.

### Exemplo 1 :

Executar a tabulação do *diagnóstico* em função do *estabelecimento*:

1.  Linha: `Diag CID10 (capit)`
2.  Coluna: `Hospital SP (CNES)`
3.  Incremento: `Valor Serv.Hospit.`

`Diag CID10 (capit)`|3001466|2081695
-------------|---------|--------
T87|170,12|NA
I60|NA|6377,05
S33|NA|941,88

### Exemplo 2 :

Executar a tabulação do *estabelecimento* em função do *diagnóstico*:

1.  Linha: `Hospital SP (CNES)`
2.  Coluna: `Diag CID10 (capit)`
3.  Incremento: `Valor Serv.Hospit.`

`Hospital SP (CNES)`|T87|I60|S33
-------|------|------|-----
3001466|170,12|NA|NA
2081695|NA|6377,05|941,88

### Exemplo 3 :

Executar a tabulação do *estabelecimento* em função do *valor dos serviços*:

1.  Linha: `Diag CID10 (capit)`
2.  Coluna: `Ignora`
3.  Incremento: `Valor Serv.Hospit.`

`Hospital SP (CNES)`|`Valor Serv.Hospit.`
-------|------
3001466|170,12
2081695|7318,93

> O aplicativo Autoblocs Saúde facilita enormemente a extração dessas informações do DATASUS
