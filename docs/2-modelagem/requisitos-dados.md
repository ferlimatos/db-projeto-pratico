# Requisitos de Dados

## 1. Objetivo

Este documento descreve as informações que precisam ser armazenadas pela Plataforma de Controle de Viagens e Ordens de Serviço, conforme a ata da entrevista e o briefing do cliente.

Os requisitos estão agrupados por assunto e servirão de base para a identificação de entidades, atributos e relacionamentos do banco de dados.

A organização abaixo não representa uma definição definitiva das tabelas. Essa definição será realizada durante a modelagem conceitual e lógica.

## 2. Clientes e Passageiros

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD01 | Nome do cliente. | Nome e telefone foram indicados como dados mínimos do cadastro inicial. |
| RD02 | Telefone do cliente. | Também deverá permitir a busca do cadastro. |
| RD03 | CPF do cliente. | Mencionado na ata; sua necessidade e obrigatoriedade ainda precisam ser confirmadas. |
| RD04 | Identificação do cliente associado a cada viagem. | Deverá permitir relacionar o cliente às viagens registradas. |

### Pendências

- Confirmar se o cliente que solicita a viagem será sempre o passageiro transportado.
- Confirmar se uma viagem poderá ter vários passageiros e se todos precisarão ser identificados.
- Confirmar se um cliente poderá possuir mais de um telefone.
- Confirmar se haverá necessidade de armazenar código internacional no telefone do cliente.

### Observação sobre endereços

Os locais de embarque e desembarque deverão ser registrados na viagem, pois podem variar entre os atendimentos de um mesmo cliente.

A necessidade de manter endereços favoritos ou fixos no cadastro do cliente ainda não foi informada.

## 3. Motoristas

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD05 | Nome completo do motorista. | Previsto no briefing. |
| RD06 | Telefone do motorista com código internacional. | Também deverá permitir a busca do cadastro. |
| RD07 | Vínculo entre motorista e veículo utilizado. | As regras e a necessidade de histórico desse vínculo ainda precisam ser definidas. |
| RD08 | Disponibilidade do motorista. | As situações possíveis e a forma de atualização ainda precisam ser confirmadas. |
| RD09 | Informações necessárias ao controle da ordem de fila dos motoristas. | Os critérios de fila ainda não foram definidos. |
| RD10 | Identificação do motorista responsável por cada viagem. | Deverá preservar a identificação de quem realizou o atendimento. |

### Pendências

- Confirmar quais dados do motorista serão obrigatórios.
- Confirmar se será necessário distinguir motoristas vinculados à empresa de motoristas autônomos.
- Confirmar se um motorista poderá trabalhar com diferentes veículos.
- Confirmar como será representada a disponibilidade.
- Confirmar quais dados serão utilizados para organizar a fila.

## 4. Veículos

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD11 | Placa do veículo. | Dado previsto para identificação do veículo. |
| RD12 | Modelo do veículo. | Previsto na ata e no briefing. |
| RD13 | Cor do veículo. | Prevista na ata. |
| RD14 | Motorista vinculado ao veículo. | As regras de vínculo ainda precisam ser validadas. |
| RD15 | Status de disponibilidade do veículo. | Os valores possíveis ainda precisam ser definidos. |
| RD16 | Identificação do veículo utilizado em cada viagem. | Deverá permitir consultar o histórico de viagens por veículo. |

### Pendências

- Confirmar se um veículo poderá ser utilizado por diferentes motoristas.
- Confirmar se será necessário guardar o histórico dos vínculos entre veículos e motoristas.
- Confirmar como distinguir o uso pessoal do uso empresarial.
- Confirmar quais campos serão obrigatórios.

### Observação sobre a frota

A frota inicial informada é de cinco veículos. Essa quantidade descreve a operação atual e não foi apresentada como limite máximo do sistema.

## 5. Viagens

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD17 | Tipo da viagem. | Agendada ou imediata, também denominada “maçaneta”. |
| RD18 | Data e horário previstos para a viagem agendada. | Aplicável aos agendamentos. |
| RD19 | Data e horário efetivos de início da viagem. | Deverão compor o histórico. |
| RD20 | Data e horário efetivos de encerramento da viagem. | Deverão compor o histórico das viagens concluídas. |
| RD21 | Cliente associado à viagem. | A distinção entre solicitante e passageiro ainda precisa ser confirmada. |
| RD22 | Motorista responsável pela viagem. | Relacionamento com o registro do motorista. |
| RD23 | Veículo utilizado na viagem. | Relacionamento com o registro do veículo. |
| RD24 | Local de embarque ou origem. | Informação específica de cada viagem. |
| RD25 | Local de desembarque ou destino. | Informação específica de cada viagem. |
| RD26 | Distância percorrida em quilômetros. | A origem da informação, manual ou automática, ainda precisa ser definida. |
| RD27 | Status da viagem. | Foram mencionados: em andamento, concluída e cancelada. Outros estados dependem de validação. |
| RD28 | Valores e informações de pagamento associados à viagem. | Detalhados na seção de dados financeiros. |
| RD29 | Descontos e vouchers aplicados à viagem. | As regras de utilização ainda precisam ser definidas. |

### Pendências

- Confirmar se uma viagem poderá ter paradas intermediárias.
- Confirmar se haverá distinção entre distância estimada e distância efetivamente percorrida.
- Confirmar como serão registradas remarcações e alterações de motorista ou veículo.
- Confirmar se será necessário registrar motivo, data e responsável pelo cancelamento.
- Confirmar todos os status e suas regras de transição.

## 6. Ordens de Serviço

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD30 | Número identificador da ordem de serviço. | Previsto no briefing. |
| RD31 | Data e horário associados à OS. | Confirmar se representam a criação da OS, a previsão da viagem ou ambos. |
| RD32 | Associação entre a OS e a viagem correspondente. | O briefing determina a geração de uma OS para cada viagem registrada. |
| RD33 | Motorista responsável. | Informação vinculada à viagem e ao cadastro do motorista. |
| RD34 | Veículo utilizado. | Informação vinculada à viagem e ao cadastro do veículo. |
| RD35 | Cliente atendido. | Deverá permitir consultar nome e telefone. |
| RD36 | Locais de embarque e desembarque. | Informações vinculadas à viagem. |
| RD37 | Valor da viagem e forma de pagamento. | Informações financeiras associadas ao atendimento. |
| RD38 | Status do atendimento. | Deverá permitir acompanhar OS em andamento, concluídas e canceladas. |

### Observação de modelagem

Viagem e ordem de serviço apresentam informações em comum.

Durante a modelagem, a equipe deverá definir se representam conceitos distintos que exigem estruturas separadas ou se a OS será a identificação e a apresentação do próprio registro da viagem.

Não é necessário duplicar os dados do cliente, motorista e veículo em diferentes tabelas apenas para exibi-los na OS. A necessidade de preservar cópias históricas desses dados deverá ser avaliada separadamente.

## 7. Dados Financeiros e Pagamentos

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD39 | Valor da viagem. | Sua relação com desconto, faturamento e recebimento ainda precisa ser definida. |
| RD40 | Valor recebido. | Previsto no histórico da viagem. |
| RD41 | Valor do desconto aplicado. | Previsto no histórico da viagem. |
| RD42 | Valor faturado. | Previsto no histórico e no acompanhamento financeiro. |
| RD43 | Forma de pagamento utilizada. | As opções aceitas ainda precisam ser confirmadas. |
| RD44 | Valores de referência utilizados no cálculo por quilômetro, caso sejam configurados no sistema. | A fórmula e a necessidade de armazenar tarifas ainda dependem de validação. |

### Pendências

- Definir o significado e a relação entre valor da viagem, valor recebido e valor faturado.
- Confirmar quais formas de pagamento serão aceitas.
- Confirmar se uma viagem poderá ter vários pagamentos.
- Confirmar se haverá pagamentos parciais ou pendentes.
- Confirmar se será necessário armazenar data e horário do pagamento.
- Confirmar se haverá comissão da empresa ou repasse ao motorista.
- Confirmar a moeda utilizada e a necessidade de operar com diferentes moedas.

## 8. Descontos, Vouchers e Promoções

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD45 | Registro da utilização de voucher em uma viagem. | A utilização de vouchers foi prevista no briefing. |
| RD46 | Associação entre o voucher utilizado e a viagem correspondente. | Deverá permitir consultar as aplicações no histórico. |
| RD47 | Valor de desconto aplicado à viagem. | Deverá compor o registro financeiro. |
| RD48 | Informações de identificação da origem dos vouchers fornecidos por terceiros. | Necessárias à prestação de contas mencionada nas anotações; o detalhamento ainda precisa ser validado. |

### Pendências

Os seguintes dados são candidatos ao armazenamento, mas ainda não foram confirmados:

- Código identificador do voucher.
- Nome ou identificação do terceiro responsável.
- Tipo de benefício: valor fixo ou percentual.
- Valor ou percentual do benefício.
- Data de início e término da validade.
- Limite de utilização.
- Status do voucher.
- Valor a receber de terceiros.
- Situação da prestação de contas.

Também será necessário confirmar se promoções terão cadastro próprio ou serão representadas apenas pelos descontos e vouchers aplicados.

## 9. Usuários e Perfis de Acesso

| Código | Informação a armazenar | Observação |
|---|---|---|
| RD49 | Identificação do usuário que utiliza o sistema. | O método de identificação ainda precisa ser definido. |
| RD50 | Papel do usuário na operação. | O briefing contempla gestor e motorista. |
| RD51 | Associação entre o usuário e o motorista, quando aplicável. | Necessária para identificar as viagens do motorista que utiliza o sistema. |

### Pendências

- Confirmar se haverá cadastro separado de usuários.
- Confirmar o método de autenticação.
- Confirmar as permissões de cada perfil.
- Confirmar como serão separados os dados de diferentes empresas e usuários autônomos.
- Confirmar se haverá histórico de alterações e identificação do responsável por cada ação.

## 10. Dados Relacionados às Integrações

### 10.1 WhatsApp

O sistema deverá receber informações de viagens por mensagens e organizá-las nos respectivos registros.

Ainda é necessário validar se deverão ser armazenados:

- Identificador da mensagem recebida.
- Número do remetente.
- Data e horário do recebimento.
- Conteúdo original da mensagem.
- Situação do processamento.
- Associação entre a mensagem e a viagem ou OS gerada.
- Informações sobre erros e correções.

Esses itens são propostas para detalhamento técnico, e não dados confirmados pelo cliente.

### 10.2 Google Maps

O briefing prevê a possibilidade de identificar endereços, geolocalizar pontos e calcular distâncias.

Ainda é necessário validar se deverão ser armazenados:

- Coordenadas dos pontos de embarque e desembarque.
- Distância estimada do trajeto.
- Tempo estimado de deslocamento.
- Identificadores dos locais retornados pela integração.
- Localização dos motoristas e horário de sua atualização.

O armazenamento da localização dos motoristas depende da confirmação da funcionalidade de localização ou distribuição por proximidade. Essa funcionalidade ainda não está aprovada.

## 11. Informações Calculadas para Relatórios

Os itens abaixo deverão estar disponíveis para consulta, mas não precisam necessariamente ser armazenados como campos independentes.

| Informação | Dados de origem | Pendência |
|---|---|---|
| Quantidade de viagens realizadas. | Registros das viagens e seus status. | Definir quais status entram na contagem. |
| Faturamento diário, semanal e mensal. | Valores financeiros e datas de referência. | Definir qual valor e qual data serão considerados. |
| Faturamento por motorista. | Valores das viagens e motorista responsável. | Confirmar a fórmula do faturamento. |
| Faturamento por veículo. | Valores das viagens e veículo utilizado. | Confirmar a fórmula do faturamento. |
| Ganho por quilômetro. | Valores financeiros e distância percorrida. | Confirmar a fórmula e o tratamento de distância igual a zero. |
| Total de descontos aplicados. | Valores de desconto das viagens. | Confirmar o tratamento de viagens canceladas. |
| Histórico por cliente, motorista e veículo. | Relacionamentos e registros das viagens. | Confirmar as permissões de consulta. |

## 12. Decisões para a Modelagem

Antes de concluir o modelo lógico, a equipe deverá:

- Definir quais informações serão obrigatórias ou opcionais.
- Definir os identificadores de cada entidade.
- Confirmar as cardinalidades dos relacionamentos.
- Definir os valores permitidos para status e tipos.
- Confirmar as regras de unicidade de telefone, CPF, placa e número da OS.
- Separar informações armazenadas de indicadores calculados.
- Definir como preservar o histórico das viagens.
- Registrar quais decisões foram confirmadas pelo cliente e quais permanecem como hipóteses.
- Relacionar os requisitos de dados aos requisitos funcionais e às regras de negócio.