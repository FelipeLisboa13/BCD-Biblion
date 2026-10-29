 # Sistema de Biblioteca -  Banco de Dados

Sistema de Organização de dados para Biblioteca 

Instituição: Escola SENAI Suíço-Brasileira

Professor: Átila

Disciplina: Banco de Dados

Autores: Felipe Lisboa e Miguel Holanda

Turma: SEDUC 1 

Data: 29/10/2026

## Sobre o projeto
O Biblion é um projeto de banco de dados para organizar as informações e a rotina de uma biblioteca. A proposta surgiu a partir da situação de Samiro, que herdou uma biblioteca com milhares de livros e utilizava apenas um caderno para controlar o acervo.

Esse controle manual causava problemas: livros emprestados não eram devolvidos, títulos podiam ser comprados em duplicidade, autores e editoras eram registrados de maneiras diferentes e era difícil saber se um livro estava disponível.

O objetivo do projeto é centralizar os dados da biblioteca em um banco de dados relacional, facilitando o cadastro, a localização dos exemplares e o acompanhamento dos empréstimos.
Objetivos do sistema
- Cadastrar livros, autores, editoras, categorias e clientes sem repetir desnecessariamente as mesmas informações.
- Registrar a localização física de cada exemplar, como corredor, estante e prateleira.
- Diferenciar a obra bibliográfica de cada cópia física disponível na biblioteca.
- Manter um histórico dos empréstimos, com informações sobre quem retirou os itens e quando.
- Consultar a disponibilidade dos exemplares, os atrasos e o histórico de leitura.
- Organizar os dados com tabelas relacionadas e identificadores consistentes.
## Como o projeto foi pensado
1. Identificar os problemas do controle manual e as informações necessárias para administrar a biblioteca.
2. Identificar as entidades principais, como livros, autores, editoras, categorias, clientes e empréstimos.
3. Diferenciar a obra do exemplar físico e registrar a localização de cada exemplar.
4. Prever tabelas associativas, como livro_autor e item_emprestimo, para representar relacionamentos entre múltiplos registros.
5. Organizar a modelagem com chaves primárias e estrangeiras e aplicar normalização para reduzir duplicações.
6. Criar e testar a estrutura usando SQL e dados de exemplo.

 ## Escopo Operacional

 1-Cadastro e Organização do Acervo

Cadastro e gerenciamento de livros, autores, editoras e categorias, permitindo organizar as informações do acervo e evitar registros duplicados.

 2- Gestão de Exemplares e Localização

Controle individual dos exemplares físicos de cada livro, com registro de sua localização na biblioteca, incluindo corredor, estante e prateleira, facilitando a localização das obras.

 3-Gestão de Clientes e Leitores

Cadastro centralizado dos clientes da biblioteca, armazenando informações pessoais e permitindo identificar os leitores associados aos empréstimos.

 4-Empréstimos e Devoluções

Registro e controle dos empréstimos de livros, incluindo os clientes responsáveis, os exemplares emprestados, as datas de retirada e devolução e o acompanhamento de possíveis atrasos.

 5-Consultas e Relatórios

Realização de consultas ao banco de dados para verificar a disponibilidade de livros, localizar exemplares, consultar o histórico de empréstimos e identificar informações importantes para a administração da biblioteca.

## Resultados das Querys

1-Resultado #1 — Select de livros e autores

<img width="828" height="151" alt="image" src="https://github.com/user-attachments/assets/de1c81e2-2408-45ce-afa2-f915b85239d3" />


2-Resultado #2 - Busca pelo id

<img width="994" height="128" alt="image" src="https://github.com/user-attachments/assets/80d229ee-d954-47d0-9e9e-49916c77d2ca" />

3-Resultado #3 - Busca por exemplares disponivel

<img width="980" height="144" alt="image" src="https://github.com/user-attachments/assets/edba0d8c-e768-4775-b0ad-1b6a8a42d13a" />

4-Resultado #4 - Busca por clientes pela data de cadastro

<img width="946" height="137" alt="image" src="https://github.com/user-attachments/assets/255f8629-dc5d-45c5-a711-4f058c3f44fd" />

5-Resultado #5 - Busca por Nomes de livros que começa Com a Letra O

<img width="984" height="124" alt="image" src="https://github.com/user-attachments/assets/5c9ace4a-6de2-4e61-9296-a93ba018d8b8" />

6-Resultado #6 - Junta tabelas para fazer um relatório mais preciso 

<img width="717" height="179" alt="image" src="https://github.com/user-attachments/assets/87a0c49a-77f8-4489-a8ee-9aff3620de75" />

 # Modelagem do Banco de Dados

O banco de dados Biblion foi desenvolvido utilizando o modelo relacional, com tabelas relacionadas por chaves primárias e estrangeiras. A modelagem busca organizar as informações da biblioteca, reduzir a duplicação de dados e manter a integridade das informações.

 ## Principais entidades

- **Livros:** armazena os dados das obras, como título, sinopse, data de publicação, categoria e editora.
- **Autores:** registra os autores das obras.
- **Editoras:** armazena as informações das editoras.
- **Categorias:** organiza os livros por categoria.
- **Exemplares:** controla cada cópia física dos livros, incluindo código e status.
- **Localizações:** registra onde cada exemplar está guardado, como corredor, estante e prateleira.
- **Clientes:** armazena os dados dos leitores cadastrados.
- **Empréstimos:** registra as retiradas e devoluções dos exemplares.
- **Livro_Autor:** relaciona livros e autores, permitindo que uma obra tenha mais de um autor.
- **Item_Emprestimo:** relaciona os empréstimos aos exemplares emprestados.

 ## Relacionamentos

A modelagem utiliza relacionamentos entre as tabelas para conectar as informações. Um livro pode possuir vários exemplares e estar relacionado a vários autores. Cada exemplar possui uma localização registrada, enquanto os empréstimos permitem acompanhar os leitores, os exemplares retirados e as datas de retirada e devolução.

As chaves primárias identificam os registros de cada tabela, enquanto as chaves estrangeiras estabelecem os relacionamentos entre elas.

 # Diagrama Entidade-Relacionamento (DER)

 <img width="1309" height="676" alt="image" src="https://github.com/user-attachments/assets/84a0954d-6e8c-4ab2-8e69-38fb6fbdd5d7" />


 #                                      SENAI Suíço-Brasileira | Banco de Dados Relacional
