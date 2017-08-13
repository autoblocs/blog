---
title: Automatizando os processos do DATASUS - Parte II
excerpt: Princípios do aplicativo Autoblocs Saúde.
date: '2017-08-10 16:24'
header:
  teaser: /assets/images/pexels-photo-325229.jpeg
category:
  - Saude Publica
tags:
  - Brasil
  - DATASUS
  - Big Data
---

No post anterior estimamos que o custo anual do processo de análise utilizando o [TabNET](http://www2.datasus.gov.br/DATASUS/index.php?area=02) seria próximo de **900 milhões de reais**. Apresentaremos o sistema de gerenciamento de dados de saúde pública da [Autoblocs](http://autoblocs.com) que diminui o tempo gasto para a execução desse processo em até 10x.

## Princípios Básicos

Os princípios aplicados podem ser agrupados em 4 grupos:

1.  Disponibilidade: utilizar tecnologias modernas da Web;
2.  Usabilidade: interface próxima às interfaces do TabNET e do TabWIN;
3.  Qualidade: disponibilizar as informações com rapidez e precisão;
4.  Automação: automatizar o máximo possível para economizar o tempo do usuário.

## Disponibilidade

O aplicativo de gestão de dados de saúde pública pode ser utilizado pelos browsers Safari, Chrome ou Firefox:

1.  Computador: PC ou MacOS;
2.  Tablets: Android ou iOS;
3.  Smartphones: Android ou iOS.

## Usabilidade

Utilizamos a mesma nomenclatura de campos definida pelo DATASUS. A utilização da mesma nomenclatura permite que o usuário não tenha dificuldade em migrar de sistemas:

1.  Linhas são os campos que serão tabulados nas linhas;
2.  Colunas são os campos que serão tabulados nas colunas;
3.  Incrementos são os campos numéricos que serão tabulados nas colunas;
4.  Filtrar e Selecionar são operações nos dados disponíveis no sistema.

## Qualidade

A utilização das tecnologias mais modernas de bases de dados e programação, permitem que a utilização do sistema seja otimizada de acordo com a quantidade de usuários de maneira totalmente flexível. Assim é possível manter a qualidade do serviço via um tempo de resposta pequeno, diminuindo o tempo de espera do usuário.

## Automação

Desenvolvemos esse sistema com um único objetivo:

> Minimizar o tempo gasto para analisar os dados de saúde pública do Brasil.

O usuário segue três passos simples para receber a tabulação desejada:

1.  Configurar os campos: Estado, cidade, sistema, arquivo, linha, coluna, incremento, etc.
2.  Configurar os filtros: Datas, tipo de gestão do recurso, registros desejados, etc.
3.  Agendar a tabulação: Enviar o pedido de tabulação para o sistema.

O sistema se encarrega de gerar as tabulações solicitadas e enviar uma mensagem ao usuário quando os dados estiverem disponíveis. O usuário executa essa tarefa uma única vez.

> O sistema atualiza os dados e faz as tabulações solicitadas automaticamente após a divulgação pelo DATASUS.
