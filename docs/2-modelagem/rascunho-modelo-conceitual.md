Entidade cliente: id como chave primária inteiro autoincrement, nome varchar(100), telefone varchar(15), num_documento varchar(50), tipo_documento varchar(10)
Veículo: id como chave primaria inteiro autoincrement, placa varchar(17), cor varchar(10), modelo (100), ano varchar(4).
Motorista: id como chave primária inteiro autoincrement, nome varchar(100), telefone varchar(15), num_documento varchar(50), tipo_documento varchar(10)
ordem de serviço: id como chave primária inteiro autoincrement, id_cliente chave estrangeria, id_motorista chave estrangeira, id_veiculo chave estrangeira, data datetime, valor_corrida MOEDA
viagem:  id como chave primaria inteiro autoincrement, id_os chave estrangeira, origem varchar(100), destino varchar(100), inicio_viagem datetime, fim_viagem datetime, status_viagem varchar(15)
disponibilidade: id como chave primaria inteiro autoincrement, id_motorista chave estrangeira, id_veiculo chave estrangeira

gere essa prévia em mermaid, não altere e nem faça sugestões. só represente o que escrevi agora no mermaid.