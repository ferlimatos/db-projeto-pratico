# Roteiro da Entrevista com o Cliente

## 1. Abertura e apresentação

**Objetivo:** Apresentar a equipe, explicar o objetivo da conversa e compreender inicialmente o projeto.

- Podemos registrar as informações desta conversa para orientar o desenvolvimento do projeto?
- Bom dia/boa tarde! Poderia nos contar brevemente sobre o seu negócio e a atividade que realiza atualmente?
- Qual é o principal problema ou necessidade que levou você a procurar um sistema?
- O que você espera que o sistema resolva?
- Quem utilizará o sistema: gestores, motoristas, atendentes ou outras pessoas?
- Existe algum prazo, orçamento ou prioridade para a primeira versão do sistema?


## 2. Contexto do negócio

**Objetivo:** Entender o modelo de negócio, os serviços oferecidos e o público atendido.

- Atualmente, quais tipos de transporte a empresa realiza?
- A empresa atende apenas clientes próprios ou também motoristas autônomos?
- Quantos veículos e motoristas existem hoje?
- Quais tipos de veículos são utilizados?
- A empresa pretende expandir para outros serviços, como táxi, transporte executivo ou entregas?
- O sistema será usado apenas internamente ou também será comercializado para outros motoristas?
- Existe algum aplicativo, planilha ou sistema que já seja utilizado para controlar as viagens?
- Quais são as maiores dificuldades encontradas no controle atual das viagens?

## 3. Processo atual das viagens

**Objetivo:** Compreender como uma viagem é solicitada, organizada, executada e registrada atualmente.

- Como uma viagem é solicitada atualmente?
- Quem recebe a solicitação: o gestor, o motorista ou outra pessoa?
- Por quais meios as solicitações chegam: WhatsApp, telefone, indicação pessoal ou outro canal?
- Como o motorista é escolhido para realizar cada viagem?
- Existe controle de fila, disponibilidade ou escala dos motoristas?
- Como é feito o acompanhamento da viagem enquanto ela está em andamento?
- O que acontece quando uma viagem é cancelada?
- Como são registrados os dados da viagem após o atendimento?

## 4. Modalidades de viagem

**Objetivo:** Esclarecer os tipos de viagem e as informações necessárias em cada caso.

- Quais são os tipos de viagem realizados pela empresa?
- Você mencionou “viagem maçaneta”. O que exatamente esse termo significa no seu negócio?
- Em uma viagem por agendamento, quais informações são informadas antecipadamente?
- Em uma viagem imediata, quais informações são registradas?
- O cliente pode solicitar a viagem diretamente pelo sistema ou apenas por WhatsApp, telefone ou outro meio?
- Uma mesma viagem pode sofrer alterações, como troca de motorista, mudança de horário ou cancelamento?
- Como é definido o valor da viagem: por quilômetro, tempo, tabela fixa ou negociação?
- A viagem pode ter mais de um passageiro?

## 5. Cadastros necessários

**Objetivo:** Identificar os dados que o sistema deverá armazenar sobre clientes, motoristas e veículos.

- Quais informações são necessárias sobre o cliente?
- O CPF do cliente será obrigatório ou opcional?
- Quais informações são necessárias sobre o motorista?
- O motorista terá acesso individual ao sistema, com login e senha?
- Quais informações sobre o veículo devem ser cadastradas?
- Um veículo pode ser utilizado por mais de um motorista?
- Um motorista pode utilizar mais de um veículo?
- Como será feita a busca por clientes, motoristas e veículos: por nome, telefone ou placa?
- Quais dados serão obrigatórios no cadastro?
- Quais dados podem ser opcionais?

## 6. Ordens de serviço

**Objetivo:** Definir o conteúdo, o fluxo e os status das ordens de serviço.

- O que a empresa entende por ordem de serviço?
- Toda viagem deverá gerar uma ordem de serviço?
- Quais informações a ordem de serviço deve conter?
- Quem poderá criar, editar, atribuir e cancelar uma ordem de serviço?
- Quais são os possíveis status de uma ordem de serviço: aguardando, em andamento, concluída ou cancelada?
- Como o gestor acompanhará as ordens de serviço em andamento?
- A ordem de serviço será enviada ao motorista pelo WhatsApp?
- O motorista poderá alterar informações da ordem de serviço durante a viagem?
- Será necessário anexar fotos, comprovantes ou observações à ordem de serviço?

## 7. Gestão de motoristas e veículos

**Objetivo:** Entender como serão controlados motoristas, frota e disponibilidade.

- Como será feito o controle da disponibilidade dos motoristas?
- O motorista poderá informar quando está disponível, ocupado ou indisponível?
- Como será organizada a fila de atendimento?
- O gestor poderá atribuir manualmente uma viagem a um motorista?
- Existe necessidade de distribuição automática das viagens?
- Como será feito o controle da frota?
- Cada veículo terá um histórico de viagens, manutenções ou abastecimentos?
- Os veículos serão utilizados apenas para trabalho ou também para fins pessoais?

## 8. Gestão financeira

**Objetivo:** Definir como serão registrados valores, descontos, vouchers e faturamento.

- Como é calculado o valor de uma viagem?
- O preço é definido por quilômetro rodado, tempo de viagem, tabela fixa ou outro critério?
- Quais formas de pagamento serão aceitas?
- O sistema precisará processar pagamentos ou apenas registrar a forma de pagamento utilizada?
- Como funcionam os vouchers e promoções?
- Quem cria os vouchers: a empresa, parceiros ou terceiros?
- O voucher terá código, valor fixo, percentual de desconto, validade ou limite de uso?
- Como será calculado o ganho do motorista?
- O sistema deverá separar o faturamento bruto, os descontos e o valor líquido?
- Quais relatórios financeiros serão necessários: diário, semanal, mensal ou personalizado?

## 9. Relatórios e indicadores

**Objetivo:** Identificar as informações que o gestor precisará acompanhar.

- Quais informações você gostaria de visualizar na tela inicial do sistema?
- Quais relatórios são mais importantes hoje?
- O gestor precisa acompanhar o faturamento por motorista?
- O gestor precisa acompanhar o faturamento por veículo?
- Será necessário consultar a quantidade de viagens realizadas por período?
- Será necessário acompanhar quilometragem percorrida, descontos, vouchers e cancelamentos?
- Os relatórios deverão ser exportados para PDF ou planilha?
- Quem poderá acessar os relatórios financeiros?

## 10. Integração com WhatsApp

**Objetivo:** Definir como o WhatsApp será utilizado no sistema.

- O WhatsApp será usado apenas para receber informações ou também para enviar confirmações ao motorista?
- Quais informações o motorista deverá enviar pelo WhatsApp?
- O motorista preferirá enviar mensagens livres ou responder a perguntas guiadas do sistema?
- O sistema deverá enviar avisos de nova ordem de serviço, alteração de viagem ou cancelamento?
- O cliente receberá alguma mensagem automática?
- Será necessário enviar comprovantes, recibos ou resumos de viagem pelo WhatsApp?
- Quem poderá registrar viagens pelo WhatsApp: apenas o motorista ou também o gestor?

## 11. Integração com Google Maps

**Objetivo:** Definir o uso de mapas, rotas e cálculo de distância.

- O sistema deverá permitir a busca de endereços pelo Google Maps?
- Será necessário calcular a distância entre origem e destino?
- O valor da viagem será estimado com base na distância calculada?
- O motorista precisará visualizar a rota no mapa?
- Será necessário acompanhar a localização do veículo em tempo real?
- O sistema deverá registrar a quilometragem percorrida automaticamente ou o motorista informará manualmente?
- A integração com o Google Maps será obrigatória já na primeira versão?

## 12. Perfis de acesso

**Objetivo:** Definir quem utilizará o sistema e quais permissões cada perfil terá.

- Quem utilizará o sistema: gestor, motorista, atendente ou outra função?
- O gestor poderá visualizar todas as viagens e informações financeiras?
- O motorista poderá visualizar apenas as próprias viagens?
- O motorista poderá cadastrar clientes e veículos?
- Será necessário um perfil de administrador para configurar o sistema?
- O sistema será utilizado por motoristas autônomos, sem vínculo com a empresa?
- Cada usuário terá acesso individual com login e senha?

## 13. Interface e dispositivos

**Objetivo:** Definir as preferências de uso e os requisitos de acessibilidade.

- O sistema será usado principalmente pelo celular ou pelo computador?
- Quais dispositivos serão utilizados: Android, iPhone ou computador?
- A interface deverá ser simples, com poucos botões e poucos campos?
- O sistema deverá funcionar em navegadores modernos?
- Existem preferências de cores, logotipo ou identidade visual?
- Há necessidade de funcionar offline ou com internet instável?

## 14. Documentos e obrigações

**Objetivo:** Identificar necessidades de comprovantes, recibos e documentos fiscais.

- O sistema deverá emitir recibo de viagem?
- O recibo será enviado ao cliente por WhatsApp, e-mail ou PDF?
- Será necessário emitir nota fiscal?
- Quais dados deverão constar no recibo?
- Será necessário guardar histórico de documentos emitidos?
- Existem regras legais, fiscais ou de privacidade que o sistema deve considerar?

## 15. Regras de negócio e exceções

**Objetivo:** Levantar situações especiais que podem afetar o funcionamento do sistema.

- O que acontece quando o cliente não comparece no local combinado?
- Como serão registrados cancelamentos feitos pelo cliente ou pelo motorista?
- Há cobrança de taxa de cancelamento?
- Um motorista pode recusar uma viagem?
- Como será feita a troca de motorista durante uma viagem?
- Será necessário registrar bagagem, animais de estimação, cadeirinha ou outras necessidades especiais?
- Existe limite de passageiros por veículo?
- Há situações em que a viagem pode ser alterada após o início?

## 16. Prioridades para o MVP

**Objetivo:** Definir o que deve ser desenvolvido primeiro.

- Qual é a funcionalidade mais importante para a primeira versão?
- O registro de viagens pelo WhatsApp é prioritário?
- O acompanhamento de faturamento é mais importante que o controle de vouchers?
- Quais funcionalidades podem ficar para uma segunda etapa?
- Quais recursos são indispensáveis para o sistema começar a ser usado?
- Quais recursos podem ser considerados expansões futuras?

## 17. Encerramento

**Objetivo:** Confirmar entendimentos, esclarecer dúvidas e definir próximos passos.

- Existe alguma necessidade ou regra importante que não foi perguntada?
- Alguma informação mencionada precisa ser corrigida ou complementada?
- Quais decisões podem ser consideradas definitivas neste momento?
- Quais dúvidas ainda precisam ser resolvidas?
- Quem será o responsável por responder às próximas dúvidas?
- Podemos apresentar um protótipo ou uma proposta de modelo de dados na próxima reunião?
