Ata da Entrevista com o Cliente
1. Informações gerais
Data: Não informada.
Participantes: Cliente e equipe de desenvolvimento.
Projeto: Sistema de gerenciamento de viagens e motoristas.
Objetivo: Compreender as necessidades do cliente, os processos do negócio, os dados que precisam ser armazenados e as funcionalidades esperadas para o sistema.
2. Resumo por bloco
2.1. Negócio e processos

O cliente deseja desenvolver um software simples, básico e de fácil utilização, semelhante a um aplicativo de transporte como Uber OTE.

O sistema terá alcance global e será voltado principalmente para ajudar motoristas a controlar e registrar suas viagens, funcionando também como uma ferramenta de CRM (Customer Relationship Management).

O cliente apresentou duas modalidades de início de viagem:

Viagem por agendamento: A viagem é programada antecipadamente.
Viagem imediata: A viagem é iniciada sem agendamento prévio. O cliente utilizou a expressão "viagem maçaneta", cujo significado precisa ser confirmado.

O sistema deverá registrar informações sobre as viagens, como data, horário, local de embarque, local de desembarque e informações do passageiro.

Atualmente, o negócio possui cinco carros disponíveis e pretende expandir suas atividades para o serviço de táxi.

O sistema também poderá ser comercializado para motoristas particulares que não fazem parte da empresa, permitindo que utilizem a plataforma para controlar suas próprias viagens.

2.2. Dados e informações que o sistema deverá armazenar

Clientes e passageiros:

Nome.
Telefone.
CPF.
Local de embarque.
Local de desembarque.

Motoristas e veículos:

Motorista responsável pela viagem.
Placa do veículo.
Cor do veículo.
Modelo do veículo.

Viagens:

Data de início.
Horário.
Origem.
Destino.
Quilometragem percorrida.
Valor faturado.
Ganho por quilômetro.
Tipo de viagem (agendada ou imediata).

O cadastro inicial deverá solicitar pelo menos nome e telefone.

2.3. Regras e funcionalidades identificadas

O sistema deverá contemplar:

Controle das ordens de serviço (OS).
Registro das viagens realizadas pelos motoristas.
Controle da ordem de fila e disponibilidade dos motoristas.
Registro de faturamento e ganhos por quilômetro.
Oferecimento de vouchers e promoções.
Suporte a diferentes formas de pagamento.
Integração com Google Maps para consulta de trajetos e quilometragem.
Recebimento de ordens de serviço provenientes do WhatsApp.
Acesso pelo computador (desktop) e pelo celular.
Baixo custo de utilização e manutenção.
2.4. Relatórios e decisões gerenciais

O cliente demonstrou interesse em acompanhar o faturamento e os ganhos dos motoristas, principalmente considerando a quilometragem percorrida.

Também foi mencionada a necessidade de controlar as viagens realizadas, mas os relatórios específicos desejados ainda precisam ser definidos.

3. Citações importantes

As seguintes frases foram registradas nas anotações da entrevista:

"Software simples, básico, de fácil atendimento."
"Parecido com a Uber OTE."
"Alcance do aplicativo: o mundo inteiro."
"Solução pro motorista ter o controle da ordem de serviço que executa."
"É um aplicativo para ajudar o motorista a registrar suas viagens."
"5 carros a pronto e quer expandir para o táxi."
"Pode ser vendido pra um motorista que faz viagens particulares também e que não é da empresa."
"A OS vem do WhatsApp."
"Baixo custo."
4. Decisões e requisitos identificados

Com base no que foi apresentado pelo cliente, foram identificados os seguintes requisitos iniciais:

O sistema deverá permitir o cadastro de clientes e motoristas.
O sistema deverá permitir o cadastro de veículos.
O sistema deverá registrar viagens agendadas e imediatas.
Cada viagem deverá possuir informações de origem, destino, data e horário.
O sistema deverá permitir o controle das ordens de serviço.
O sistema deverá registrar informações financeiras das viagens.
O sistema deverá permitir o controle da disponibilidade dos motoristas.
O sistema deverá oferecer suporte a vouchers e promoções.
O sistema deverá permitir integração com Google Maps.
O sistema deverá ser acessível por desktop e dispositivos móveis.
O sistema deverá considerar tanto motoristas vinculados à empresa quanto motoristas particulares.
O sistema deverá considerar a possibilidade de expansão para serviços de táxi.
5. Pendências

Algumas informações importantes não foram esclarecidas durante a entrevista:

Definir exatamente o significado de "viagem maçaneta".
Definir como funciona a distribuição das ordens de serviço entre os motoristas.
Definir se o passageiro poderá solicitar viagens diretamente pelo aplicativo.
Definir quais formas de pagamento serão efetivamente disponibilizadas.
Definir como será realizado o controle de vouchers e promoções.
Definir quais relatórios serão necessários.
Definir se o sistema emitirá recibos, notas fiscais ou outros documentos.
Definir quais informações serão obrigatórias no cadastro de clientes e motoristas.
Definir como será realizada a integração com WhatsApp e Google Maps.
6. Considerações finais

A entrevista permitiu identificar que o principal objetivo do projeto é desenvolver um sistema de gerenciamento de viagens e ordens de serviço, oferecendo aos motoristas maior controle sobre suas atividades e permitindo acompanhar informações operacionais e financeiras.

O sistema deverá priorizar simplicidade, baixo custo, acessibilidade e possibilidade de expansão.

As pendências deverão ser esclarecidas com o cliente antes da definição definitiva do modelo conceitual e lógico do banco de dados.