# Rascunho do Modelo de Dados — PostgreSQL

## 1. Objetivo

Este documento organiza a estrutura inicialmente proposta pela equipe, com tipos de dados compatíveis com PostgreSQL.

Os atributos e relacionamentos do rascunho foram preservados. As regras de obrigatoriedade, unicidade e cardinalidade ainda deverão ser definidas.

## 2. Cliente

Nome da tabela: `cliente`.

| Atributo | Tipo de dado PostgreSQL | Chave | Descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador do cliente, gerado automaticamente. |
| nome | VARCHAR(100) | — | Nome do cliente. |
| telefone | VARCHAR(15) | — | Telefone do cliente. |
| num_documento | VARCHAR(50) | — | Número do documento do cliente. |
| tipo_documento | VARCHAR(10) | — | Tipo do documento do cliente. |

## 3. Veículo

Nome da tabela: `veiculo`.

| Atributo | Tipo de dado PostgreSQL | Chave | Descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador do veículo, gerado automaticamente. |
| placa | VARCHAR(17) | — | Placa do veículo. |
| cor | VARCHAR(10) | — | Cor do veículo. |
| modelo | VARCHAR(100) | — | Modelo do veículo. |
| ano | VARCHAR(4) | — | Ano do veículo. |

## 4. Motorista

Nome da tabela: `motorista`.

| Atributo | Tipo de dado PostgreSQL | Chave | Descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador do motorista, gerado automaticamente. |
| nome | VARCHAR(100) | — | Nome do motorista. |
| telefone | VARCHAR(15) | — | Telefone do motorista. |
| num_documento | VARCHAR(50) | — | Número do documento do motorista. |
| tipo_documento | VARCHAR(10) | — | Tipo do documento do motorista. |

## 5. Ordem de Serviço

Nome da tabela: `ordem_servico`.

| Atributo | Tipo de dado PostgreSQL | Chave | Referência / descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador da ordem de serviço, gerado automaticamente. |
| id_cliente | INTEGER | FK | Referência a `cliente.id`. |
| id_motorista | INTEGER | FK | Referência a `motorista.id`. |
| id_veiculo | INTEGER | FK | Referência a `veiculo.id`. |
| data | TIMESTAMP | — | Data e horário associados à ordem de serviço; significado a detalhar. |
| valor_corrida | NUMERIC(12,2) | — | Valor da corrida, com até dez dígitos inteiros e duas casas decimais. |

## 6. Viagem

Nome da tabela: `viagem`.

| Atributo | Tipo de dado PostgreSQL | Chave | Referência / descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador da viagem, gerado automaticamente. |
| id_os | INTEGER | FK | Referência a `ordem_servico.id`. |
| origem | VARCHAR(100) | — | Local de origem da viagem. |
| destino | VARCHAR(100) | — | Local de destino da viagem. |
| inicio_viagem | TIMESTAMP | — | Data e horário de início da viagem. |
| fim_viagem | TIMESTAMP | — | Data e horário de encerramento da viagem. |
| status_viagem | VARCHAR(15) | — | Situação da viagem. |

## 7. Disponibilidade

Nome da tabela: `disponibilidade`.

| Atributo | Tipo de dado PostgreSQL | Chave | Referência / descrição |
|---|---|---|---|
| id | INTEGER GENERATED ALWAYS AS IDENTITY | PK | Identificador do registro de disponibilidade, gerado automaticamente. |
| id_motorista | INTEGER | FK | Referência a `motorista.id`. |
| id_veiculo | INTEGER | FK | Referência a `veiculo.id`. |

## 8. Relacionamentos Indicados

| Tabela de origem | Chave estrangeira | Tabela e coluna referenciadas |
|---|---|---|
| ordem_servico | id_cliente | cliente.id |
| ordem_servico | id_motorista | motorista.id |
| ordem_servico | id_veiculo | veiculo.id |
| viagem | id_os | ordem_servico.id |
| disponibilidade | id_motorista | motorista.id |
| disponibilidade | id_veiculo | veiculo.id |

## 9. Padronização dos Tipos

| Descrição do rascunho | Definição adotada |
|---|---|
| Inteiro com autoincremento | INTEGER GENERATED ALWAYS AS IDENTITY |
| Chave estrangeira para identificador inteiro | INTEGER |
| Modelo com tamanho 100, sem tipo informado | VARCHAR(100) |
| DATETIME | TIMESTAMP |
| MOEDA | NUMERIC(12,2) |

### Observações

- A declaração `GENERATED ALWAYS AS IDENTITY` gera o identificador automaticamente. A restrição `PRIMARY KEY` deverá ser declarada separadamente no SQL.
- Os campos de chave estrangeira deverão receber suas respectivas restrições `FOREIGN KEY` no script de criação.
- `TIMESTAMP` representa data e horário sem informação de fuso horário.
- Caso seja necessário registrar instantes considerando diferentes fusos, deverá ser avaliado o uso de `TIMESTAMP WITH TIME ZONE`, também chamado `TIMESTAMPTZ`.
- `NUMERIC(12,2)` armazena valores decimais exatos, mas não identifica a moeda utilizada. Uma operação com diferentes moedas exigirá uma definição adicional.
- O atributo `ano` foi mantido como `VARCHAR(4)` para preservar o rascunho original.
- Os tamanhos dos campos de texto foram preservados e ainda poderão ser revistos.

## 10. Definições Pendentes

- Obrigatoriedade ou possibilidade de valor nulo em cada atributo.
- Restrições de unicidade.
- Cardinalidades e participação obrigatória ou opcional nos relacionamentos.
- Significado específico do atributo `data` em `ordem_servico`.
- Valores permitidos para `status_viagem`.
- Significado operacional da entidade `disponibilidade`.
- Regras de atualização e exclusão dos registros relacionados.
- Necessidade de utilizar fusos horários.
- Formato de armazenamento dos telefones.
- Inclusão dos demais dados identificados no levantamento, como modalidade da viagem, distância, descontos, vouchers e forma de pagamento.

## 11. Legenda

- PK: chave primária.
- FK: chave estrangeira.
- —: nenhuma
