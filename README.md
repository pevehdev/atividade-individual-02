# Módulo 2 – Sistema RESILIADATA
## Objetivo
O objetivo do projeto é realizar a modelagem (conceitaul e lógico) de um banco de dados da empresa Resilia. 

A Atividade consistem em 4 perguntas sendo:
```
1 - Quais são as entidades necessárias?
```
Empresa_Parceira: Representa as empresas parceiras.

Tecnologia: Representa as tecnologias disponíveis.

Colaborador: Representa os colaboradores que trabalham para as empresas parceiras.

Tecnologia_Utilizada: Representa a relação entre as empresas parceiras e as tecnologias que elas utilizam.

Colaborador_Tecnologia: Representa a relação entre os colaboradores e as tecnologias que eles utilizam
```
2 - Quais são os principais campos e seus respectivos tipos?
```
## Principais Campos e Tipos de Dados:

Empresa_Parceira:
id_empresa (INT): Chave primária autoincrementada.

nome (VARCHAR): Nome da empresa.

telefone (VARCHAR): Número de telefone da empresa.

email (VARCHAR): Endereço de e-mail da empresa.

data_inicio (DATE): Data de início da parceria.

Tecnologia:
id_tecnologia (INT): Chave primária autoincrementada.

nome (VARCHAR): Nome da tecnologia.

descricao (VARCHAR): Descrição da tecnologia (opcional).

area (VARCHAR): Área de aplicação da tecnologia.

Colaborador:
id_colaborador (INT): Chave primária autoincrementada.

nome (VARCHAR): Nome do colaborador.

email (VARCHAR): Endereço de e-mail do colaborador.

cargo (VARCHAR): Cargo do colaborador na empresa.

id_empresa (INT): Chave estrangeira referenciando a tabela Empresa_Parceira.

Tecnologia_Utilizada:

id_empresa (INT): Chave estrangeira referenciando a tabela Empresa_Parceira.

id_tecnologia (INT): Chave estrangeira referenciando a tabela Tecnologia.

Colaborador_Tecnologia:

id_colaborador (INT): Chave estrangeira referenciando a tabela Colaborador.

id_tecnologia (INT): Chave estrangeira referenciando a tabela Tecnologia.

```
3 - Relacionamentos entre as Entidades:
```
Empresa_Parceira e Colaborador: Relacionamento de 1 para N, indicando que uma empresa pode ter vários colaboradores e um colaborador trabalha para apenas uma empresa.

Empresa_Parceira e Tecnologia_Utilizada: Relacionamento de 1 para N, indicando que uma empresa pode utilizar várias tecnologias e uma tecnologia pode ser utilizada por várias empresas.

Tecnologia e Tecnologia_Utilizada: Relacionamento de 1 para N, indicando que uma tecnologia pode ser utilizada por várias empresas e uma empresa pode utilizar várias tecnologias.

Colaborador e Colaborador_Tecnologia: Relacionamento de 1 para N, indicando que um colaborador pode ter habilidades em várias tecnologias e uma tecnologia pode ser dominada por vários colaboradores.
```
4 - Simule 2 registros para cada entidade.
```
## Adicionar registros para Empresa_Parceira

INSERT INTO Empresa_Parceira (nome, telefone, email, data_inicio) VALUES 
('Empresa A', '123456789', 'empresa_a@example.com', '2023-01-01'),
('Empresa B', '987654321', 'empresa_b@example.com', '2022-05-10');

Adicionar registros para Tecnologia
INSERT INTO Tecnologia (nome, descricao, area) VALUES 
('Java', 'Linguagem de programação', 'Desenvolvimento de software'),
('Python', 'Linguagem de programação', 'Ciência de dados');

Adicionar registros para Colaborador
INSERT INTO Colaborador (nome, email, cargo, id_empresa) VALUES 
('João', 'joao@example.com', 'Desenvolvedor', 1),
('Maria', 'maria@example.com', 'Analista de Dados', 2);

Adicionar registros para Tecnologia_Utilizada
INSERT INTO Tecnologia_Utilizada (id_empresa, id_tecnologia) VALUES 
(1, 1),
(2, 2);

Adicionar registros para Colaborador_Tecnologia
INSERT INTO Colaborador_Tecnologia (id_colaborador, id_tecnologia) VALUES 
(1, 1),
(2, 2);
