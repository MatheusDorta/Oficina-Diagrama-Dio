#Diagrama de Banco de Dados para Oficina
#Descrição
Este repositório contém o diagrama de banco de dados desenvolvido como parte do desafio da Digital Innovation One (DIO) para modelar o sistema de uma oficina mecânica. O diagrama representa a estrutura de entidades e relacionamentos necessários para gerenciar clientes, veículos, ordens de serviço, equipes, mecânicos, serviços e peças.

#Entidades Principais
Cliente
- idCliente (INT) - Identificador único do cliente
- Nome (VARCHAR(45)) - Nome do cliente
- Telefone (INT) - Número de telefone
- E-mail (VARCHAR) - Endereço de e-mail
- CPF (INT) - Número do CPF

#Veículo
- idVeiculo (INT) - Identificador único do veículo
- Placa (VARCHAR(45)) - Placa do veículo
- Modelo (VARCHAR(45)) - Modelo do veículo
- Marca (VARCHAR(45)) - Marca do veículo
- Ano (INT) - Ano de fabricação
- Cliente_idCliente (INT) - Chave estrangeira para o cliente proprietário

#Ordem de Serviço
- idOrdem de Serviço (INT) - Identificador único da ordem
- Data Emissão (INT) - Data de emissão da ordem
- Data de Entrega (INT) - Data prevista de entrega
- Status (VARCHAR(45)) - Status atual da ordem
- Valor Total (VARCHAR(45)) - Valor total do serviço
- Relacionamentos com Veículo e Cliente

#Equipe
- idEquipe (INT) - Identificador único da equipe
- Nome do Funcionario (VARCHAR(45)) - Nome do funcionário
- Relacionamentos com Ordem de Serviço

#Mecânico (Funcionário)
- idMecanico (INT) - Identificador único do mecânico
- Nome (VARCHAR(45)) - Nome do mecânico
- Endereço (VARCHAR(45)) - Endereço do mecânico
- Especialidade (VARCHAR(45)) - Especialidade do mecânico
- Relacionamentos com Equipe e Ordem de Serviço

#Serviços
- idServiços (INT) - Identificador único do serviço
- Descrição (VARCHAR(45)) - Descrição do serviço
- Valor da mão de obra (VARCHAR(45)) - Valor do serviço

#Peças
- idPeças (INT) - Identificador único da peça
- Nome (VARCHAR(45)) - Nome da peça
- Valor Unitario (VARCHAR(45)) - Valor unitário da peça

#Relacionamentos
Cliente (1..*) → Veículo (1) (Um cliente pode ter vários veículos)
Veículo (1..*) → Ordem de Serviço (1) (Um veículo pode ter várias ordens de serviço)
Ordem de Serviço tem relacionamentos muitos-para-muitos com Serviços e Peças através de tabelas associativas

#Como Visualizar
O diagrama está disponível no arquivo oficina.pdf neste repositório. Para visualizar, basta abrir o arquivo em qualquer visualizador de PDF.

#Contribuições
Contribuições para melhorar o diagrama são bem-vindas. Sinta-se à vontade para abrir issues ou enviar pull requests com sugestões de melhorias.
