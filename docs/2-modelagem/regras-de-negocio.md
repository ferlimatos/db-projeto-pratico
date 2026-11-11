# Regras de Negócio

## 1. Objetivo

Este documento apresenta as regras de negócio identificadas na ata da entrevista e no briefing da Plataforma de Controle de Viagens e Ordens de Serviço.

As regras orientam o funcionamento da operação e deverão ser relacionadas às restrições do banco de dados ou aos controles implementados na aplicação.

## 2. Situação das Regras

- **Documentada:** regra descrita na ata ou no briefing, sem pressupor aprovação formal posterior.
- **Pendente de validação:** regra ainda não esclarecida ou que representa uma proposta da equipe.

As formas de implementação apresentadas são propostas técnicas. A definição definitiva dependerá do modelo de dados adotado.

## 3. Regras Identificadas

### 3.1 Cadastros e Identificação

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN01 | O cadastro inicial do cliente deverá conter, no mínimo, nome e telefone. | Documentada | `NOT NULL` nos campos correspondentes. A rejeição de valores vazios deverá ser tratada por `CHECK` ou pela aplicação. |
| RN02 | O telefone cadastrado para o motorista deverá incluir o código internacional. | Documentada | Validação na aplicação. A forma de armazenamento será definida no modelo lógico. |
| RN03 | Uma viagem registrada deverá estar associada a um cliente, a um motorista responsável e a um veículo. | Documentada | Chaves estrangeiras e obrigatoriedade dos vínculos no registro completo. A possibilidade de agendamento ainda sem motorista ou veículo precisa ser validada. |
| RN04 | O sistema deverá contemplar tanto motoristas vinculados à empresa quanto motoristas particulares que utilizem a plataforma individualmente. | Documentada | Tratamento no modelo de dados e na aplicação. A separação dos registros entre operações ainda precisa ser definida. |

### 3.2 Modalidades e Dados das Viagens

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN05 | As modalidades de viagem inicialmente previstas serão agendada e imediata, também denominada “maçaneta”. | Documentada | `CHECK` ou chave estrangeira para uma estrutura de modalidades. |
| RN06 | Uma viagem agendada deverá possuir data e horário previstos para sua realização. | Documentada | `CHECK` condicional ou estrutura própria para o agendamento, conforme a modelagem. |
| RN07 | Uma viagem imediata representa o atendimento em que o cliente se dirige diretamente ao veículo, sem agendamento prévio. | Documentada | Tratada na aplicação e na classificação da modalidade. |
| RN08 | Toda viagem deverá registrar local de embarque e local de desembarque. | Documentada | `NOT NULL` nos campos ou vínculos correspondentes. |
| RN09 | O histórico de uma viagem concluída deverá conter data e horário de início e encerramento, cliente, motorista, veículo, origem, destino, distância e informações financeiras. | Documentada | Restrições condicionais no banco e validação da aplicação ao concluir a viagem. |

### 3.3 Ordens de Serviço

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN10 | Cada viagem registrada deverá gerar uma ordem de serviço. | Documentada | Se viagem e OS forem estruturas distintas, a correspondência deverá ser garantida pelo modelo e pelo processo transacional. |
| RN11 | Cada ordem de serviço deverá possuir um número identificador que permita distingui-la das demais. | Documentada | `PRIMARY KEY` ou `UNIQUE`, conforme a definição do identificador. |
| RN12 | A OS deverá apresentar data, horário, motorista, veículo, nome e telefone do cliente, embarque, desembarque, valor, forma de pagamento e status. | Documentada | Dados próprios e relacionamentos com outras estruturas. A obrigatoriedade por etapa da operação ainda precisa ser validada. |
| RN13 | O gestor deverá conseguir acompanhar as ordens de serviço em andamento, concluídas e canceladas. | Documentada | Consultas e controle de acesso na aplicação. Esses status não devem ser considerados uma lista exaustiva sem confirmação. |

### 3.4 Motoristas e Veículos

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN14 | A operação deverá manter informações de disponibilidade dos motoristas e dos veículos. | Documentada | Campos ou relacionamentos de disponibilidade, com valores permitidos definidos após validação. |
| RN15 | A operação deverá permitir o controle da ordem de fila dos motoristas. | Documentada | Tratada no modelo e na aplicação após definição dos critérios de ordenação e atualização. |
| RN16 | Deverá ser possível identificar o motorista e o veículo utilizados em cada viagem, mesmo que seus vínculos atuais sejam alterados posteriormente. | Documentada quanto à identificação no histórico | Chaves estrangeiras no registro da viagem. A política de alteração e exclusão dos cadastros deverá preservar a consulta histórica. |
| RN17 | A solução deverá contemplar a utilização dos veículos para fins pessoais e empresariais. | Documentada | Tratada na aplicação e, se necessário, por classificação do uso no banco. O detalhamento depende de validação. |

### 3.5 Valores, Pagamentos e Benefícios

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN18 | O registro financeiro da viagem deverá distinguir valor recebido, valor de desconto e valor faturado. | Documentada | Campos financeiros próprios. A relação matemática entre eles ainda precisa ser confirmada. |
| RN19 | A viagem deverá registrar a forma de pagamento utilizada. | Documentada | Chave estrangeira ou domínio de valores. O momento de preenchimento e as opções aceitas dependem de validação. |
| RN20 | Os descontos e vouchers utilizados deverão ficar associados à viagem correspondente. | Documentada | Chaves estrangeiras e, se necessário, estrutura associativa. A quantidade de benefícios por viagem ainda precisa ser definida. |
| RN21 | Vouchers fornecidos por terceiros deverão poder ser registrados para prestação de contas. | Documentada nas anotações complementares | Tratada no modelo e na aplicação após definição dos dados do terceiro e do processo de conferência. |
| RN22 | As informações financeiras deverão permitir o acompanhamento por viagem, motorista e veículo. | Documentada | Relacionamentos entre viagens, responsáveis, veículos e valores; consultas e views. |
| RN23 | O faturamento deverá poder ser acompanhado em períodos diários, semanais e mensais. | Documentada | Consultas e views. O valor e a data utilizados no cálculo ainda precisam ser definidos. |

### 3.6 Modelos de Utilização

| Código | Regra de negócio | Situação | Restrição ou tratamento previsto |
|---|---|---|---|
| RN24 | No modelo com gestor e motorista, o gestor supervisionará as viagens, acompanhará o faturamento e controlará os veículos. | Documentada | Controle de acesso na aplicação e, quando aplicável, permissões no banco. |
| RN25 | No modelo individual, o motorista poderá registrar suas viagens, consultar seu histórico e acompanhar seu faturamento sem estrutura administrativa. | Documentada | Controle de acesso e associação dos registros ao usuário responsável. |
| RN26 | O motorista deverá conseguir registrar informações das viagens pelo WhatsApp. | Documentada | Tratada na integração e na aplicação. O recebimento de uma mensagem não deverá ser confundido com a confirmação de um registro completo. |

## 4. Regras Pendentes de Validação

Os itens abaixo não representam decisões confirmadas do cliente. São questões que precisam ser resolvidas antes de se tornarem regras definitivas.

| Código | Questão a validar | Possível impacto na implementação |
|---|---|---|
| PV01 | O motorista será escolhido por proximidade, ordem de fila ou decisão do gestor? | Define o processo de atribuição das viagens. |
| PV02 | A escolha será automática, uma sugestão ou uma ação manual? | Define a atuação da aplicação e do gestor. |
| PV03 | O motorista poderá aceitar ou recusar uma OS? | Pode exigir estados de atribuição e histórico de recusas. |
| PV04 | Um motorista poderá ter mais de uma viagem em andamento? | Pode exigir controle de concorrência e restrição de disponibilidade. |
| PV05 | Um veículo poderá estar associado a viagens simultâneas? | Pode exigir validação de sobreposição de horários. |
| PV06 | Um agendamento poderá ser registrado antes da definição do motorista e do veículo? | Define a obrigatoriedade dos vínculos em cada etapa. |
| PV07 | Um motorista poderá utilizar vários veículos e um veículo poderá ser utilizado por vários motoristas? | Define cardinalidades e eventual histórico de vínculos. |
| PV08 | O solicitante poderá ser diferente do passageiro? Uma viagem poderá transportar vários passageiros identificados? | Define os relacionamentos entre pessoas e viagens. |
| PV09 | O passageiro poderá solicitar viagens diretamente? | Define usuários, permissões e origem das solicitações. |
| PV10 | Quais serão todos os status e quais mudanças entre eles serão permitidas? | Define domínio de status e regras de transição. |
| PV11 | Quem poderá alterar, concluir, cancelar ou excluir registros? | Define permissões e preservação do histórico. |
| PV12 | Como serão tratados cancelamentos, remarcações e ausência do passageiro? Haverá cobrança? | Define estados, motivos e possíveis valores adicionais. |
| PV13 | Qual será a fórmula do preço da viagem? Haverá tarifa fixa, por quilômetro ou valor negociado? | Define os dados de cobrança e os cálculos. |
| PV14 | O cálculo utilizará distância estimada ou efetivamente percorrida? | Define a origem e a finalidade de cada medida de distância. |
| PV15 | Qual é a relação entre valor da viagem, desconto, valor recebido e valor faturado? | Define fórmulas e restrições financeiras. |
| PV16 | Como será calculado o ganho por quilômetro? | Define o indicador e o tratamento de distância igual a zero. |
| PV17 | Quais formas de pagamento serão aceitas? Haverá pagamentos parciais, pendentes ou combinados? | Define o domínio de pagamento e a necessidade de registros separados. |
| PV18 | Haverá comissão da empresa ou repasse ao motorista? | Pode exigir estruturas de divisão dos valores. |
| PV19 | Quais serão
