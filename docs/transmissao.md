---
id: transmissao
title: Transmissão de dados
sidebar_label: Transmissão de dados
---

O módulo “Transmissão de Dados” permite fazer o controle de envio dos dados realizados por uma instalação PEC e-SUS AB, bem como controlar o recebimento de dados oriundos de outras aplicações.

Este módulo possui três funcionalidades principais: configurações da transmissão de dados, controle de envio de dados e controle de recebimento de dados.

### Conceitos relacionados

- Registro de Atendimento Simplificado (RAS): É um modelo de documento que possui o conjunto essencial de informações gerado a partir dos eventos de saúde individualizados registrados no CDS e PEC. Documentos RAS são transmitidos para o SISAB e podem ser enviado para outras instalações do PEC e-SUS AB ou sistemas de terceiros.
- Instalação de destino: É o endereço eletrônico de uma aplicação que pode ser cadastrada para receber os dados enviados por uma instalação PEC e-SUS AB.
- Geração de lotes: [colocar descrição...]
- Lotes para envio: [colocar descrição...]
- Fichas inválidas: [colocar descrição...]
- Fichas repetidas: [colocar descrição...]

## 1. Configurações

Este módulo possui funcionalidades para realizar o cadastro de Instalações de Destino e para configurar o Horário de geração de lotes e processamentos de fichas. Estas funcionalidades podem ser utilizadas apenas pelo Instalador do PEC e-sus AB.

![Figura 1 - Tela de Configurações de Transmissão de dados](/docs/assets/Figura1.png "teste") **Figura 1 - Tela de Configurações de Transmissão de dados**

### 1.1 Cadastrar Instalações de destino para envio online

As instalações de destino são servidores que possuem uma instalação do PEC e-SUS AB que foram cadastradas para receber dados enviados por outra instalação. Elas podem ser, por exemplo, o Centralizador da Secretaria Municipal de Saúde ou da Secretaria Estadual de Saúde. Desse modo, esses órgãos poderão fazer uso dos relatórios disponíveis para realizar a gestão dos serviços públicos de saúde em sua área de atuação. Nestes casos, Estado ou Município irá fornecerá o endereço eletrônico (link) para inclusão da instalação de destino na configuração de envio.
O Centralizador Nacional do Ministério da Saúde já é previamente cadastrado nas instalações do PEC e-SUS AB, para que o Governo Federal possa fazer a gestão dos serviços públicos de saúde em todo o território nacional.

**Para cadastrar uma Instalação de Destino:**

1. Acesse a tela “Configurações” no módulo “Transmissão de Dados”;
2. Clique na opção “Adicionar instalação”.

![Figura 2 - Formulário de cadastro de Instalação de destino](/docs/assets/Figura2.png "teste") **Figura 2 - Formulário de cadastro de Instalação de destino**

3. Preencha o campo “Nome da instalação”. O nome da instalação deve se referir ao local para onde os dados serão enviados (ex.: Centralizador municipal);
4. Preencha o campo “Endereço do servidor”. O endereço informado deve ser o endereço eletrônico do computador que possui a instalação do PEC e-sus AB que receberá os dados;
5. Clique no botão “Adicionar”.
6. Para editar as informações de uma Instalação de destino, clique no botão ![](/docs/assets/pen-outline.png "Editar");
7. Para inativar uma Instalação de destino, clique no botão ![](/docs/assets/dots.png "Mais opções") e na opção “Inativar”;
8. Para excluir uma Instalação de destino, clique no botão ![](/docs/assets/dots.png "Mais opções") e na opção “Excluir”;
9. Para testar a conexão com o servidor de uma Instalação de destino, clique no botãoe na opção “Testar conexão” .

Observações: Por padrão, as Instalações de Destino são adicionadas “Ativas”.

**Impacto em outros módulos:**

### 1.2 Configurar Horário de geração de lotes e processamento de fichas

Esta funcionalidade permite configurar o horário de início da geração de lotes e do processamento dos dados de saúde registrados no sistema. O horário previamente cadastrado é 00:00 hora. É recomendado iniciar a geração de lotes fora do horário de funcionamento da Unidade de Saúde.

**Para configurar o Horário de geração de lotes e processamento de fichas:**

1. Acesse a tela Configurações no módulo “Transmissão de Dados”;
2. Preencha o campo “Horário”;
3. Clique no botão “Salvar”.

**Impacto em outros módulos:**

## 2. Envio de dados

Este módulo permite que o Administrador municipal monitore o envio das informações do PEC e-SUS AB para outras aplicações. É possível acompanhar o envio de dados que foram enviados de forma online ou enviados manualmente por arquivo ZIP.
O sistema apresenta uma lista de lotes gerados, com data de criação dos lotes, quantidade de fichas e status de envio (Enviado, Não enviado).

![Figura 3 - Tela de Envio de dados](/docs/assets/Figura3.png) **Figura 3 - Tela de Envio de dados**

### 2. 1 Gerar lotes para envio

A geração de lotes para envio pode ser realizada de forma automática ou manual.

**Geração de lotes automática:**

A geração de lotes para envio ocorre no horário configurado no módulo de Configurações da Transmissão de dados. Para que os lotes sejam gerados no horário definido, é necessário que o computador que possui a instalação do PEC e-sus AB esteja ligado, caso contrário os lotes serão gerados no momento em que o servidor for reiniciado.

**Geração de lotes manual:**

[Descrever a geração manual ]

**Impacto em outros módulos:**

- Fichas CDS que foram processadas e inseridas em um lote não podem mais ser alteradas ou excluídas do sistema.
- Fichas CDS e atendimentos registrados no PEC que foram processados passam a ser contabilizados nos relatórios.

### 2.2 Envio de lotes

O envio de lotes pode ser realizado de forma online ou de forma offline.

**Envio Online:**

No envio Online os lotes gerados pelo sistema são enviados automaticamente para todas as Instalações de Destino ativas cadastradas nas Configurações da Transmissão de dados. Tentativas de envio de dados ocorrem a cada 10 minutos, obedecendo a uma regra de agendamento automático do Centralizador Nacional. O agendamento tem o objetivo de distribuir o fluxo e reduzir os acessos aos servidores das instalações de destino. Dessa forma, a transmissão de dados para as instalações de destino serão executadas conforme disponibilidade do servidor destino.

Está funcionalidade só é oferecida para instalações configuradas para funcionamento Online.

Observação: É necessário que o município possua ao menos uma instalação on-line para realizar o envio das informações ao Centralizador Nacional.

**Envio Offline:**

Instalações do PEC e-sus AB que não possuam conexão com Internet podem fazer o envio dos dados por meio do salvamento dos Lotes em um arquivo que posteriormente poderá ser importado em outras instalações.

**Para salvar um lote em arquivo:**

1. Acesse a tela Envio no módulo “Transmissão de Dados”;
2. Clique no botão ![](/docs/assets/dots.png "Mais opções") e na opção “Salvar em arquivo”, para salvar um lote que já havia sido gerado.
3. Para visualizar informações adicionais sobre o lote, clique no botão ![](/docs/assets/dots.png "Mais opções") e na opção “Testar conexão” .

![Figura 4 - Tela de visualização de lote](/docs/assets/Figura4.png) **Figura 4 - Tela de visualização de lote**

## 3. Recebimento de dados

Este módulo permite que o Administrador municipal monitore o recebimento de informações oriundas de outras aplicações que também utilizam o formato RAS. Estas informações podem ser recebidas de forma online ou offline (através da importação de arquivo ZIP). Os dados recebidos podem ser visualizados agrupados por Lotes ou por CNES de origem (estabelecimento que registrou a informação).

### 3.1 Visualizar dados recebidos agrupados por lote

O sistema apresenta uma lista dos lotes recebidos, com nome do profissional responsável pela instalação que realizou o envio, data de recebimento, quantidade de fichas válidas, inválidas e repetidas. O módulo permite imprimir um relatório de inconsistências para lotes recebidos que possuem registros inválidos ou duplicados.

![Figura 5 - Tela de Recebimento - Agrupamento por lotes](/docs/assets/Figura5.png) **Figura 5 - Tela de Recebimento - Agrupamento por lotes**

**Para visualizar os dados de um lote:**

1. Acesse a tela Recebimento no módulo “Transmissão de Dados”;
2. Clique no botão ![](/docs/assets/dots.png "Mais opções") e na opção “Visualizar”.
3. Para gerar o relatório de inconsistências de um lote:
4. Acesse a tela Recebimento no módulo “Transmissão de Dados”;
5. Clique no botão ![](/docs/assets/printer-outline.png "Impressora") para imprimir o relatório de inconsistências.

**Para gerar o relatório de inconsistências de múltiplos lotes:**

1. Acesse a tela Recebimento no módulo “Transmissão de Dados”;
2. Clique no botão “Gerar relatório de inconsistências”;
3. Na modal “Gerar relatório de inconsistências”, informe o período, responsável ou tipo de recebimento para os quais deseja gerar o relatório.
4. Clique no botão Gerar.

<img src="/docs/assets/Figura6.png" width="50%"> **Figura 6 - Modal para gerar relatório de inconsistências**

### 3.2 Visualizar dados recebidos agrupados por CNES

É apresentada uma lista dos lotes recebidos agrupados por estabelecimento de saúde e mês de envio. Para cada registro da listagem é apresentado o nome do estabelecimento de origem, mês no qual o envio foi realizado e a quantidade de fichas contidas nos lotes que já foram processadas na competência selecionada.

![Figura 7 - Visualizar dados recebidos agrupados por CNES](/docs/assets/Figura7.png "teste") **Figura 7 - Visualizar dados recebidos agrupados por CNES**

**Para visualizar os dados enviados por um CNES em uma competência específica:**

1. Acesse a tela Recebimento no módulo “Transmissão de Dados”;
2. Clique no botão do CNES que deseja visualizar os dados recebidos.

### 3.3 Recebimento de dados de forma online

As instalações PEC e-SUS AB podem receber de forma online dados oriundos de diferentes aplicações:

- Para receber dados de outras instalações do PEC e-SUS AB é necessário que elas estejam cadastradas como Instalação de Destino nas instalações de origem.
- Para receber dados de aplicativos mobile como o e-SUS AB Território, e-SUS AB AC e e-SUS Atenção Domiciliar elas devem ser cadastradas como servidor de sincronização.

As informações recebidas serão processadas no horário configurado nas Configurações de Transmissão de dados.

Está funcionalidade só pode ser utilizada por instalações configuradas para funcionamento Online.

### 3.4 Recebimento de dados de forma offline - via importação de arquivo

As instalações PEC e-SUS AB podem importar arquivos gerados em outras instalações PEC e-SUS AB ou em sistemas de terceiros que também utilizem o modelo RAS.
Essa funcionalidade permite receber

**Para importar um arquivo com dados produzidos em outras instalações:**

[Descrição dos passos]
