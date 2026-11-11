# Ata da Entrevista

Data: 06/11/2026
Duração real: 10 minutos  
Cliente: Nome não informado.  
Negócio: Transporte de passageiros.  
Projeto: Plataforma de Controle de Viagens e Ordens de Serviço.  
Equipe: Cliente e equipe de desenvolvimento participaram da entrevista. Os nomes e a distribuição dos papéis de entrevistador, anotador, cronometrista e observador não foram informados.

## Objetivo da Entrevista

Compreender as necessidades do cliente, o funcionamento do negócio, os dados que precisam ser armazenados e as funcionalidades esperadas para um sistema de gerenciamento de viagens, motoristas e ordens de serviço.

## Resumo por Bloco

### 1. Negócio e Processos

O cliente deseja uma plataforma simples, básica, de fácil utilização e baixo custo, destinada ao controle interno das viagens e ordens de serviço. A proposta é ajudar os motoristas a registrar suas atividades e permitir que gestores acompanhem a operação e o faturamento.

A simplicidade operacional de aplicativos como Uber e 99 foi apresentada como referência. Nas anotações iniciais, a solução também foi caracterizada como uma ferramenta de CRM, sem detalhamento das funcionalidades específicas de relacionamento com clientes.

O negócio possui inicialmente cinco veículos disponíveis e pretende expandir suas atividades para motoristas particulares que não fazem parte da empresa.

O público pretendido inclui motoristas de aplicativos, motoristas autônomos, pequenas empresas de transporte, empresas de mobilidade urbana, gestores de pequenas frotas e operadores de transporte executivo, com possibilidade de utilização internacional.

Foram identificadas duas modalidades de viagem:

- Agendada: programada antecipadamente, com data, horário, locais de embarque e desembarque e identificação do motorista e do veículo.
- Imediata ou “maçaneta”: atendimento em que o cliente se dirige diretamente ao veículo e a viagem é registrada de forma simplificada, conforme descrito no briefing complementar.

As ordens de serviço são provenientes do WhatsApp. O motorista deverá conseguir registrar informações das viagens por mensagens, e o sistema deverá interpretar e organizar os dados recebidos.

Foram previstos dois modelos de utilização:

- Gestor e motorista: o gestor supervisiona as viagens, acompanha o faturamento e controla os veículos; o motorista registra e acompanha suas viagens.
- Somente motorista: utilização individual para registrar viagens, consultar o histórico e acompanhar o faturamento, sem necessidade de estrutura administrativa.

O desenvolvimento inicial deverá priorizar um MVP, com foco no registro das viagens pelo WhatsApp e no acompanhamento das informações pelo gestor.

### 2. Dados e Entidades

Foram identificados os seguintes conjuntos de informações a serem registrados:

#### Clientes e Passageiros

- Nome.
- Telefone.
- CPF, mencionado nas anotações iniciais, sem definição de obrigatoriedade.
- Associação às viagens realizadas.
- Locais de embarque e desembarque de cada atendimento.

O cadastro inicial deverá solicitar pelo menos nome e telefone.

#### Motoristas

- Nome completo.
- Telefone com código internacional.
- Veículo utilizado.
- Identificação das viagens realizadas.
- Disponibilidade e posição na fila, conforme regras ainda a definir.

#### Veículos

- Placa.
- Modelo.
- Cor.
- Motorista vinculado.
- Status de disponibilidade.
- Histórico de viagens.

#### Viagens

- Modalidade: agendada ou imediata.
- Data e horário previstos, no caso dos agendamentos.
- Data e horário de início.
- Data e horário de encerramento.
- Cliente.
- Motorista responsável.
- Veículo utilizado.
- Origem e destino.
- Distância percorrida.
- Status da viagem.
- Informações financeiras e de pagamento.
- Descontos e vouchers aplicados.

#### Ordens de Serviço

- Número identificador.
- Data e horário.
- Motorista responsável.
- Dados do veículo.
- Nome e telefone do cliente.
- Local de embarque.
- Local de desembarque.
- Valor da viagem.
- Tipo de pagamento.
- Status da viagem.

#### Informações Financeiras

- Valor da viagem.
- Valor recebido.
- Valor de desconto.
- Valor faturado.
- Forma de pagamento.
- Vouchers utilizados.

Também foi mencionada a necessidade de acompanhar o preço por quilômetro, o ganho por quilômetro e a quantidade de viagens realizadas. A forma de cálculo e apresentação dessas informações ainda precisa ser detalhada.

A busca de clientes e motoristas deverá ser possível por nome ou número de telefone.

### 3. Regras e Exceções

- Cada viagem registrada deverá gerar uma ordem de serviço.
- O gestor deverá acompanhar e supervisionar ordens de serviço em andamento, concluídas e canceladas.
- Cada viagem concluída deverá compor o histórico operacional e financeiro.
- O sistema deverá permitir o controle da ordem de fila e da disponibilidade dos motoristas.
- Os veículos deverão possuir informação de disponibilidade e histórico de viagens.
- A plataforma deverá contemplar a utilização dos veículos para fins pessoais e empresariais.
- O sistema deverá registrar a forma de pagamento utilizada em cada viagem, mas as opções aceitas não foram especificadas.
- Deverá ser possível aplicar descontos e utilizar vouchers promocionais.
- O faturamento deverá ser acompanhado por viagem, motorista e veículo.
- O sistema deverá apoiar o cálculo do preço por quilômetro e o acompanhamento do ganho por quilômetro.
- O WhatsApp deverá permitir o registro das informações das viagens por mensagens.
- Foi mencionada a possibilidade de integração com o Google Maps para identificação de endereços, geolocalização dos pontos, cálculo de distância, estimativa de preço e visualização de rotas.
- A plataforma deverá ser acessível por smartphones Android e iOS, computadores desktop e navegadores modernos.
- A interface deverá priorizar poucos comandos, informações organizadas, facilidade de navegação, operação rápida e layout responsivo.
- A utilização e a manutenção deverão priorizar baixo custo.

Não foram detalhadas as regras de distribuição das OS, alterações de viagens, cancelamentos, remarcações, ausência do passageiro ou aplicação dos benefícios promocionais.

### 4. Relatórios e Decisões

O cliente demonstrou interesse em acompanhar o faturamento e os ganhos dos motoristas, especialmente em relação à quilometragem percorrida.

O briefing complementar especifica:

- Relatórios de faturamento diário, semanal e mensal.
- Acompanhamento do faturamento por motorista.
- Acompanhamento do faturamento por veículo.
- Consulta ao histórico de viagens.
- Acompanhamento da quantidade de viagens realizadas.
- Registro de valores recebidos, descontos, valores faturados e vouchers aplicados.

As fórmulas dos indicadores, os filtros, as permissões de consulta e os relatórios adicionais ainda precisam ser definidos.

Como direcionamento inicial, a solução deverá:

- Priorizar o registro das viagens pelo WhatsApp.
- Permitir a supervisão das informações pelo gestor.
- Contemplar a utilização individual por motoristas autônomos.
- Manter simplicidade, acessibilidade e baixo custo.
- Possuir possibilidade de expansão para novos recursos, integrações e mercados.

## Citações Importantes — Palavras do Cliente

As frases abaixo foram preservadas conforme as anotações fornecidas:

- “Software simples, básico, de fácil atendimento.”
- “Parecido com a Uber OTE.”
- “Alcance do aplicativo: o mundo inteiro.”
- “Solução pro motorista ter o controle da ordem de serviço que executa.”
- “É um aplicativo para ajudar o motorista a registrar suas viagens.”
- “5 carros a pronto e quer expandir para o táxi.”
- “Pode ser vendido pra um motorista que faz viagens particulares também e que não é da empresa.”
- “A OS vem do WhatsApp.”
- “Baixo custo.”

## Pendências e Dúvidas

As dúvidas foram priorizadas para esclarecer os pontos que mais afetam a modelagem do banco de dados. Os detalhes técnicos das integrações e as funcionalidades de expansão serão tratados posteriormente.

### 1. Distribuição das Ordens de Serviço

Como é escolhido o motorista responsável por cada viagem?

Justificativa: definir o papel da fila, da disponibilidade e da proximidade. A seleção do motorista mais próximo é uma hipótese da equipe, ainda não confirmada pelo cliente.

### 2. Vínculo entre Motoristas e Veículos

Como funciona o uso dos veículos pelos motoristas ao longo do tempo?

Justificativa: identificar se os veículos são fixos ou compartilhados e se será necessário manter histórico dos vínculos.

### 3. Ciclo da Ordem de Serviço

Pode descrever o que acontece com uma OS desde o registro até o encerramento, incluindo quando o atendimento não é realizado?

Justificativa: esclarecer a relação entre OS e viagem, os status e o momento de definição do motorista e do veículo.

### 4. Registro Financeiro

Como vocês registram e conferem o valor de uma viagem até considerar o atendimento financeiramente encerrado?

Justificativa: esclarecer a relação entre valor cobrado, desconto, valor recebido e valor faturado, considerando as formas de pagamento e os vouchers utilizados.

### 5. Dados Indispensáveis

Quais informações não podem faltar para cadastrar um cliente, um motorista e um veículo?

Justificativa: confirmar os campos obrigatórios. Nome e telefone já foram indicados como dados mínimos do cadastro inicial do cliente.

## Observação sobre o Escopo

As demais questões permanecerão em um registro de detalhamento futuro, sem serem consideradas regras aprovadas.

A ausência de uma resposta não será interpretada como confirmação de uma hipótese da equipe. Quando necessário, a equipe apresentará uma proposta de modelagem e registrará sua validação com o cliente.

## Esclarecimentos Encontrados no Briefing Complementar

- A expressão “viagem maçaneta”, inicialmente registrada como dúvida, foi descrita como atendimento imediato em que o cliente se dirige diretamente ao veículo.
- Os relatórios inicialmente não especificados foram parcialmente detalhados como relatórios de faturamento diário, semanal e mensal, com acompanhamento por motorista e veículo.
- Foram descritos dois modelos de utilização: gestor e motorista ou somente motorista.
- Foi detalhado que cada viagem deverá gerar uma OS e que as viagens concluídas deverão compor um histórico operacional e financeiro.

Esses esclarecimentos constam no material complementar fornecido pela equipe. Não foram informadas datas ou responsáveis por uma validação posterior com o cliente.

## Considerações Finais

A entrevista e o briefing permitiram identificar como objetivo central o desenvolvimento de uma plataforma para gerenciamento de viagens e ordens de serviço, com registro pelo WhatsApp e acompanhamento operacional e financeiro.

A solução deverá priorizar simplicidade, baixo custo, acessibilidade e possibilidade de expansão.

As pendências deverão ser registradas e esclarecidas com o cliente para orientar a definição das regras de negócio, dos relacionamentos e do modelo de dados.

Esta ata consolida as duas anotações fornecidas. Somente as frases apresentadas na seção de citações foram tratadas como transcrições das palavras do cliente.