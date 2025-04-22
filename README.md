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

## Exemplo de Consultas (Queries)

## Listar todos os pedidos com o nome do remédio, farmácia, farmacêutico e motoboy:
sql
Copiar
Editar
SELECT
  p.idpedido,
  r.nome AS remedio,
  f.nome AS farmaceutico,
  fa.nome AS farmacia,
  m.nome AS motoboy,
  p.descricao
FROM pedido p
JOIN remedios r ON p.idremedio = r.idremedios
JOIN farmaceutico f ON p.idfarmaceutico = f.idfarmaceutico
JOIN farmacia fa ON p.idfarmacia = fa.idfarmacia
JOIN motoboy m ON p.idmotoboy = m.idmotoboy;

## Pedidos de um remédio específico (ex: Ibuprofeno):
sql
Copiar
Editar
SELECT p.idpedido, f.nome AS farmaceutico, m.nome AS motoboy
FROM pedido p
JOIN remedios r ON p.idremedio = r.idremedios
JOIN farmaceutico f ON p.idfarmaceutico = f.idfarmaceutico
JOIN motoboy m ON p.idmotoboy = m.idmotoboy
WHERE r.nome = 'Ibuprofeno';

## Farmácias com mais de 100 unidades em estoque:
sql
Copiar
Editar
SELECT fa.nome AS farmacia, r.nome AS remedio, r.quantidade
FROM farmacia fa
JOIN remedios r ON fa.idremedios = r.idremedios
WHERE r.quantidade > 100;

## Observações
Os dados foram inseridos para simulação e testes de queries.

O projeto pode ser expandido com funcionalidades como controle de login, entrega em tempo real e visualização de estoque por cidade.

Relacionamentos foram implementados com FOREIGN KEY.

## Autoria
Projeto desenvolvido por Maria Clara, estudante de Ciência da Computação.
E-mail: mariacrangel04@gmail.com
GitHub: https://github.com/MariRangel04
