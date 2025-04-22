## Sistema de Gerenciamento de Pedidos de Farmácia
Este projeto tem como objetivo a criação de um banco de dados relacional para gerenciar farmácias, medicamentos, pedidos, clientes, farmacêuticos e motoboys. Ele pode ser utilizado como base para um sistema de entrega de medicamentos por meio de farmácias regionais.

## Estrutura do Projeto
O banco de dados é composto por 8 tabelas principais:

uf: Estados brasileiros

cidade: Cidades com vínculo a uma UF

remedios: Cadastro de medicamentos

farmaceutico: Farmacêuticos vinculados a cidades

cliente: Clientes que realizam pedidos

farmacia: Farmácias que armazenam remédios

motoboy: Responsáveis pela entrega dos pedidos

pedido: Tabela de pedidos que relaciona remédio, farmácia, farmacêutico e motoboy

## Tecnologias Utilizadas
MySQL 8+

Workbench ou DBeaver (recomendado para visualização)

SQL puro para criação e inserção de dados

## Como usar
Clone ou copie este script.

Execute o arquivo .sql em seu ambiente MySQL.

O script criará o schema 03_dump, com todas as tabelas e dados de exemplo prontos para consulta.

## Observações
Os dados foram inseridos para simulação e testes de queries.

O projeto pode ser expandido com funcionalidades como controle de login, entrega em tempo real e visualização de estoque por cidade.

Relacionamentos foram implementados com FOREIGN KEY.

## Autoria
![maria1](https://github.com/user-attachments/assets/701c0e11-4968-404f-b5ea-a7c58b88f2b5)

Projeto desenvolvido por Maria Clara, estudante de Ciência da Computação. <p/>
E-mail: mariacrangel04@gmail.com <p/>
GitHub: https://github.com/MariRangel04
