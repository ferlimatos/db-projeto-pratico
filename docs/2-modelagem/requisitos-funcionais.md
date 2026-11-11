# Requisitos Funcionais

## 1. Objetivo

Este documento apresenta os requisitos funcionais identificados na ata da entrevista e no briefing da Plataforma de Controle de Viagens e Ordens de Serviço.

Os requisitos descrevem as funcionalidades esperadas para o sistema. Quando houver informações incompletas ou decisões ainda não confirmadas, a pendência estará indicada na descrição.

## 2. Cadastros e Consultas

| Código | Requisito funcional |
|---|---|
| RF01 | O sistema deverá permitir o cadastro de clientes, com nome, telefone e demais informações definidas para o atendimento. |
| RF02 | O sistema deverá permitir o cadastro de motoristas, incluindo nome completo e telefone com código internacional. |
| RF03 | O sistema deverá permitir o cadastro de veículos, incluindo placa, modelo e cor. |
| RF04 | O sistema deverá permitir o vínculo entre motoristas e veículos. As regras para múltiplos vínculos ainda precisam ser validadas. |
| RF05 | O sistema deverá permitir a busca de clientes e motoristas por nome ou número de telefone. |

## 3. Registro e Acompanhamento das Viagens

| Código | Requisito funcional |
|---|---|
| RF06 | O sistema deverá permitir o registro de viagens agendadas, com data e horário previstos. |
| RF07 | O sistema deverá permitir o registro simplificado de viagens imediatas, denominadas “viagens maçaneta”. |
| RF08 | O sistema deverá registrar, para cada viagem, cliente, motorista responsável, veículo, origem e destino. |
| RF09 | O sistema deverá registrar as datas e os horários de início e encerramento das viagens. |
| RF10 | O sistema deverá registrar a distância percorrida em cada viagem. |
| RF11 | O sistema deverá permitir o acompanhamento das viagens em andamento, concluídas e canceladas. |
| RF12 | O sistema deverá manter um histórico das viagens concluídas, com suas informações operacionais e financeiras. |
| RF13 | O sistema deverá permitir ao motorista consultar e acompanhar suas próprias viagens. |

## 4. Ordens de Serviço

| Código | Requisito funcional |
|---|---|
| RF14 | O sistema deverá gerar uma ordem de serviço para cada viagem registrada. |
| RF15 | O sistema deverá atribuir um número identificador a cada ordem de serviço. |
| RF16 | O sistema deverá registrar na OS data, horário, motorista, veículo, cliente, embarque, desembarque, valor, forma de pagamento e status. |
| RF17 | O sistema deverá permitir ao gestor consultar e supervisionar as ordens de serviço em andamento, concluídas e canceladas. |

## 5. Controle de Motoristas e Veículos

| Código | Requisito funcional |
|---|---|
| RF18 | O sistema deverá permitir o controle da disponibilidade dos motoristas. |
| RF19 | O sistema deverá permitir o controle da ordem de fila dos motoristas. Os critérios de ordenação ainda precisam ser definidos. |
| RF20 | O sistema deverá permitir o controle da disponibilidade dos veículos. |
| RF21 | O sistema deverá permitir a consulta do histórico de viagens de cada veículo. |
| RF22 | O sistema deverá contemplar o uso dos veículos em atividades pessoais e empresariais. A forma de registrar e distinguir esses usos ainda precisa ser validada. |

## 6. Gestão Financeira

| Código | Requisito funcional |
|---|---|
| RF23 | O sistema deverá permitir o cálculo do preço por quilômetro rodado. A fórmula ainda precisa ser confirmada. |
| RF24 | O sistema deverá registrar o valor recebido, o valor de desconto e o valor faturado de cada viagem. |
| RF25 | O sistema deverá registrar a forma de pagamento utilizada em cada viagem. |
| RF26 | O sistema deverá permitir o acompanhamento do faturamento individual por viagem. |
| RF27 | O sistema deverá permitir o acompanhamento do faturamento por motorista. |
| RF28 | O sistema deverá permitir o acompanhamento do faturamento por veículo. |
| RF29 | O sistema deverá permitir o acompanhamento do ganho por quilômetro. A fórmula do indicador ainda precisa ser validada. |

## 7. Descontos, Vouchers e Promoções

| Código | Requisito funcional |
|---|---|
| RF30 | O sistema deverá permitir a aplicação e o registro de descontos nas viagens. |
| RF31 | O sistema deverá permitir a utilização e o registro de vouchers promocionais nas viagens. |
| RF32 | O sistema deverá manter no histórico da viagem os descontos e vouchers aplicados. |
| RF33 | O sistema deverá permitir o registro de vouchers fornecidos por terceiros para prestação de contas, conforme mencionado nas anotações complementares. O procedimento ainda precisa ser definido. |

## 8. Relatórios

| Código | Requisito funcional |
|---|---|
| RF34 | O sistema deverá disponibilizar relatórios de faturamento diário, semanal e mensal. |
| RF35 | O sistema deverá disponibilizar informações sobre a quantidade de viagens realizadas. |
| RF36 | O sistema deverá permitir a consulta das informações financeiras e operacionais das viagens, incluindo distância, valores, descontos e forma de pagamento. |

## 9. Interação pelo WhatsApp

| Código | Requisito funcional |
|---|---|
| RF37 | O sistema deverá permitir que o motorista registre informações das viagens por mensagens no WhatsApp. |
| RF38 | O sistema deverá interpretar e organizar as informações recebidas pelo WhatsApp, gerando os registros correspondentes. |
| RF39 | O sistema deverá permitir o recebimento de informações de ordens de serviço provenientes do WhatsApp. |

## 10. Integração com Google Maps

O briefing apresenta essa integração como uma possibilidade. Portanto, os requisitos abaixo foram identificados, mas sua inclusão na primeira versão ainda precisa de confirmação.

| Código | Requisito funcional |
|---|---|
| RF40 | O sistema deverá permitir a identificação dos endereços de embarque e desembarque por integração com o Google Maps. |
| RF41 | O sistema deverá permitir a obtenção da localização dos pontos de embarque e desembarque. |
| RF42 | O sistema deverá permitir o cálculo da distância entre origem e destino. |
| RF43 | O sistema deverá permitir a estimativa do preço da viagem com base na quilometragem. |
| RF44 | O sistema deverá permitir a visualização de rotas. |

## 11. Modelos de Utilização e Acesso

| Código | Requisito funcional |
|---|---|
| RF45 | O sistema deverá contemplar a utilização conjunta por gestor e motorista, permitindo ao gestor supervisionar viagens, faturamento e veículos. |
| RF46 | O sistema deverá permitir a utilização individual por motoristas autônomos, com registro das próprias viagens, consulta ao histórico e acompanhamento do faturamento. |

## 12. Funcionalidades Pendentes de Confirmação

Os itens abaixo não devem ser considerados requisitos aprovados sem validação com o cliente:

- Selecionar automaticamente o motorista mais próximo do passageiro.
- Distribuir automaticamente as ordens de serviço.
- Permitir que o motorista aceite ou recuse uma viagem.
- Permitir a solicitação de viagens diretamente pelo passageiro.
- Processar pagamentos pelo sistema.
- Criar vouchers com regras específicas de validade, limites e acumulação.
- Emitir recibos ou notas fiscais.
- Enviar notificações automáticas.
- Acompanhar veículos em tempo real.
- Exportar relatórios para PDF ou planilha.
- Exigir login e senha como método de autenticação.

## 13. Observações sobre o Escopo

- Esta lista representa as funcionalidades identificadas para a solução pretendida pelo cliente, e não a confirmação de que todas serão implementadas na primeira versão.
- O escopo do MVP deverá ser validado com o cliente.
