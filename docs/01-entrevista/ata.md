# Respostas da Entrevista com o Cliente

## 1. Abertura e apresentação

- **Qual é o seu negócio e a atividade que realiza atualmente?**  
  O cliente atua no setor de transporte, com uma frota inicial de cinco veículos e pretende expandir as atividades para o serviço de táxi.

- **Qual é o principal problema ou necessidade que levou você a procurar um sistema?**  
  A necessidade de controlar e registrar as viagens realizadas pelos motoristas, organizar as ordens de serviço e acompanhar o faturamento de forma simples.

- **O que você espera que o sistema resolva?**  
  O cliente espera que o sistema permita ao motorista ter controle das ordens de serviço que executa, registrar viagens, acompanhar faturamento e organizar o histórico operacional.

- **Quem utilizará o sistema?**  
  O sistema poderá ser utilizado por gestores e motoristas. Também poderá ser usado por motoristas autônomos que não fazem parte da empresa.

- **Existe prazo, orçamento ou prioridade para a primeira versão?**  
  O cliente deseja uma solução de baixo custo, simples, básica e de fácil utilização. A prioridade é desenvolver um MVP funcional.

- **Podemos registrar as informações desta conversa?**  
  Sim. As informações foram registradas para orientar o levantamento de requisitos e o desenvolvimento do sistema.

## 2. Contexto do negócio

- **Quais tipos de transporte a empresa realiza?**  
  A empresa realiza transporte de passageiros e pretende expandir para o serviço de táxi.

- **A empresa atende apenas clientes próprios ou também motoristas autônomos?**  
  O sistema poderá ser comercializado para motoristas particulares que não fazem parte da empresa.

- **Quantos veículos e motoristas existem hoje?**  
  Atualmente, existem cinco carros disponíveis para operação.

- **Quais tipos de veículos são utilizados?**  
  O sistema deverá cadastrar modelo, placa e cor dos veículos.

- **A empresa pretende expandir para outros serviços?**  
  Sim. O cliente mencionou a intenção de expandir para o serviço de táxi.

- **O sistema será usado apenas internamente ou também será comercializado?**  
  O sistema poderá ser utilizado internamente pela empresa e também comercializado para motoristas autônomos.

- **Existe algum aplicativo, planilha ou sistema utilizado atualmente?**  
  Não foi informado um sistema específico. O cliente mencionou que a solução deverá ser semelhante, em simplicidade, a aplicativos como Uber e 99, porém voltada ao controle interno das viagens.

- **Quais são as maiores dificuldades encontradas hoje?**  
  A principal dificuldade é o controle das viagens, das ordens de serviço, do faturamento e das informações dos motoristas.

## 3. Processo atual das viagens

- **Como uma viagem é solicitada atualmente?**  
  As ordens de serviço chegam principalmente pelo WhatsApp.

- **Quem recebe a solicitação?**  
  O cliente não especificou claramente quem recebe a solicitação, mas o sistema deverá permitir que o gestor acompanhe e supervise as ordens de serviço.

- **Por quais meios as solicitações chegam?**  
  As ordens de serviço são recebidas pelo WhatsApp.

- **Como o motorista é escolhido para realizar cada viagem?**  
  O cliente mencionou a integração com o Google Maps. Com base nessa informação, entende-se que o motorista mais próximo do cliente poderá ser indicado para realizar a viagem. Portanto, o sistema deverá considerar a localização dos motoristas disponíveis e a localização do cliente para sugerir ou selecionar o motorista mais próximo.  

- **Existe controle de fila, disponibilidade ou escala dos motoristas?**  
  Sim. O sistema deverá controlar a ordem de fila e a disponibilidade dos motoristas.

- **Como é feito o acompanhamento da viagem em andamento?**  
  O sistema deverá permitir o acompanhamento das ordens de serviço em andamento pelo gestor.

- **O que acontece quando uma viagem é cancelada?**  
  O sistema deverá registrar o status da viagem, incluindo ordens de serviço canceladas.

- **Como são registrados os dados da viagem após o atendimento?**  
  Cada viagem concluída deverá gerar um registro histórico com dados de início, encerramento, motorista, veículo, cliente, origem, destino, distância, valores e forma de pagamento.

## 4. Modalidades de viagem

- **Quais são os tipos de viagem realizados?**  
  O sistema deverá contemplar viagens agendadas e viagens imediatas.

- **O que significa “viagem maçaneta”?**  
  “Viagem maçaneta” significa atendimento imediato. Nesse caso, o cliente se dirige diretamente ao veículo e a viagem é registrada de forma simplificada.

- **Em uma viagem por agendamento, quais informações são informadas antecipadamente?**  
  Devem ser informados data, horário, local de embarque, local de desembarque, motorista responsável e veículo utilizado.

- **Em uma viagem imediata, quais informações são registradas?**  
  Devem ser registrados nome e telefone do cliente, localização inicial, localização final e motorista responsável.

- **O cliente pode solicitar a viagem diretamente pelo sistema?**  
  Não há indicação de que o passageiro solicitará viagens diretamente pelo aplicativo. O WhatsApp será o canal principal de registro pelo motorista.

- **Uma mesma viagem pode sofrer alterações?**  
  O sistema deverá permitir o acompanhamento das ordens de serviço em andamento, concluídas e canceladas, mas as regras de alteração ainda precisam ser definidas.

- **Como é definido o valor da viagem?**  
  O valor deverá considerar a quilometragem percorrida. O sistema deverá calcular o preço por quilômetro rodado.

- **A viagem pode ter mais de um passageiro?**  
  Não foi informado. Essa regra ainda precisa ser esclarecida.

## 5. Cadastros necessários

- **Quais informações são necessárias sobre o cliente?**  
  Nome, telefone, CPF, local de embarque e local de desembarque.

- **O CPF do cliente será obrigatório ou opcional?**  
  O CPF foi mencionado como dado a ser armazenado, mas ainda não foi definido se será obrigatório.

- **Quais informações são necessárias sobre o motorista?**  
  Nome completo, telefone com código internacional, veículo utilizado e placa do veículo.

- **O motorista terá acesso individual ao sistema?**  
  Sim. O sistema deverá possuir perfis de acesso para gestor e motorista.

- **Quais informações sobre o veículo devem ser cadastradas?**  
  Modelo, placa, cor, motorista vinculado, status de disponibilidade e histórico de viagens.


## Pendências

- Confirmar se o motorista mais próximo será selecionado automaticamente ou se o gestor fará a atribuição manual.
- Definir se o passageiro poderá solicitar viagens diretamente pelo sistema.
- Definir as regras de criação, validade e uso dos vouchers.
- Definir se o sistema emitirá recibos, notas fiscais ou outros documentos.