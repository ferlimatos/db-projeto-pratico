# BRIEFING DO SISTEMA
## Plataforma de Controle de Viagens e Ordens de Serviço

### 1. Objetivo do sistema

Desenvolver uma plataforma de tecnologia para controle, registro, acompanhamento e supervisão das viagens realizadas por motoristas de transporte por aplicativo, utilizando exclusivamente o WhatsApp como canal de comunicação e registro das informações.

O sistema deverá permitir que motoristas e gestores acompanhem as viagens, organizem o histórico operacional e controlem o faturamento de maneira simples e acessível.

O conceito é oferecer uma ferramenta básica, funcional e de fácil entendimento, semelhante à simplicidade operacional de aplicativos como Uber e 99, porém direcionada ao controle interno das viagens.

### 2. Cadastro e identificação

O sistema deverá permitir o registro das seguintes informações:

**Motorista**
- Nome completo;
- Telefone com código internacional;
- Veículo utilizado;
- Placa do veículo.

**Cliente**
- Nome;
- Telefone;
- Localização inicial;
- Localização final.

A busca de registros deverá ser realizada por nome ou número de telefone, tanto do motorista quanto do cliente.

### 3. Modalidades de viagem

O sistema deverá contemplar duas modalidades principais:

**A. Agendamento**
- Viagem previamente programada;
- Data e horário definidos;
- Local de embarque;
- Local de desembarque;
- Identificação do motorista e veículo;
- Acompanhamento da ordem de serviço.

**B. Maçaneta (atendimento imediato)**
- Cliente se dirige diretamente ao veículo;
- Registro simplificado da viagem;
- Nome e telefone do cliente;
- Localização inicial;
- Localização final;
- Motorista responsável.

### 4. Ordens de Serviço (OS)

O sistema deverá gerar uma Ordem de Serviço para cada viagem registrada.

A OS deverá conter:
- Número identificador;
- Data e horário;
- Motorista responsável;
- Dados do veículo;
- Nome e telefone do cliente;
- Local de embarque;
- Local de desembarque;
- Valor da viagem;
- Tipo de pagamento;
- Status da viagem.

O gestor deverá conseguir acompanhar e supervisionar as ordens de serviço em andamento, concluídas e canceladas.

### 5. Histórico de viagens

Cada viagem concluída deverá gerar um registro histórico contendo:

- Data e hora de início;
- Data e hora de encerramento;
- Motorista;
- Veículo;
- Cliente;
- Origem e destino;
- Distância percorrida;
- Valor recebido
- Valor desconto
- Valor faturado
- Tipo de pagamento;
- Quantidade de viagens realizadas;
- Descontos ou vouchers aplicados.

### 6. Gestão financeira

O sistema deverá possibilitar:

- Cálculo do preço por quilômetro rodado;
- Registro do faturamento individual por viagem;
- Controle do faturamento por motorista;
- Controle do faturamento por veículo;
- Identificação da forma de pagamento;
- Aplicação de descontos;
- Utilização de vouchers promocionais;
- Relatórios de faturamento diário, semanal e mensal.

### 7. Gestão de veículos

A plataforma deverá permitir o cadastro e controle de uma frota inicial de 5 veículos disponíveis para operação.

Cada veículo deverá possuir:
- Modelo;
- Placa;
- Motorista vinculado;
- Status de disponibilidade;
- Histórico de viagens.

O sistema deverá permitir a utilização dos veículos tanto para fins pessoais quanto para operações empresariais.

### 8. Perfis de acesso

O sistema deverá possuir dois modelos de utilização:

**Modelo 1 — Gestor e Motorista**
- Gestor supervisiona as viagens;
- Gestor acompanha faturamento;
- Gestor controla os veículos;
- Motorista registra e acompanha suas viagens.

**Modelo 2 — Somente Motorista**
- Uso individual;
- Registro das próprias viagens;
- Controle de faturamento;
- Consulta ao histórico;
- Sem necessidade de estrutura administrativa.

### 9. Interface e acessibilidade

A plataforma deverá ser compatível com:

- Smartphones Android;
- Smartphones iOS;
- Computadores desktop;
- Navegadores modernos.

A interface deverá priorizar:
- Simplicidade;
- Facilidade de navegação;
- Poucos comandos;
- Informações organizadas;
- Operação rápida;
- Layout responsivo.

### 10. Integração com WhatsApp

O WhatsApp será o canal principal de interação com o sistema.

O motorista deverá conseguir registrar as informações de uma viagem por meio de mensagens, sem precisar acessar constantemente uma plataforma externa.

O sistema deverá interpretar as informações recebidas, organizar os dados e gerar os registros correspondentes.

### 11. Integração com Google Maps

Possibilidade de integração com Google Maps para:

- Identificação dos endereços de embarque e desembarque;
- Geolocalização dos pontos;
- Cálculo de distância entre origem e destino;
- Estimativa do preço da viagem com base na quilometragem;
- Visualização de rotas;
- Apoio ao cálculo do faturamento.

### 12. Público-alvo

A plataforma deverá ser desenvolvida para utilização internacional, com possibilidade de atender:

- Motoristas de aplicativos;
- Motoristas autônomos;
- Pequenas empresas de transporte;
- Empresas de mobilidade urbana;
- Gestores de pequenas frotas;
- Operadores de transporte executivo.

### 13. Diretriz de desenvolvimento

O sistema deverá ser desenvolvido inicialmente com foco em um MVP (Produto Mínimo Viável).

A prioridade será garantir que o motorista consiga registrar suas viagens pelo WhatsApp e que o gestor consiga acompanhar, supervisionar e organizar as informações.

A plataforma deverá possuir estrutura tecnológica preparada para expansão futura, incluindo novos recursos, integrações, relatórios e diferentes mercados internacionais.
