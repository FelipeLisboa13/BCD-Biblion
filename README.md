# BCD-Biblion

BIBLION - RESUMO

ORIGEM DO PROBLEMA
  Samiro herdou uma biblioteca com milhares de livros e um caderno de anotações como único controle. Livros                emprestados não voltavam, títulos eram comprados em duplicidade, autores e editoras apareciam escritos de formas diferentes e, para saber se um livro estava disponível, era preciso procurar na estante.

O QUE ERA NECESSÁRIO
- Cadastro único de livros, autores, editoras e categorias, sem duplicidade.
- Saber onde cada exemplar está (corredor, estante, prateleira).
- Distinguir o livro (a obra) do exemplar (a cópia física).
- Histórico de empréstimos: quem pegou, quando e o que levou.
- Respostas rápidas sobre disponibilidade, atrasos e leituras.
- Dados consistentes, cada informação em um só lugar.

COMO FOI FEITO
1. Entendemos a dor do Samiro e listamos o que ele precisava saber.
2. Identificamos as entidades: livro, autor, editora, cliente e empréstimo.
3. Separamos obra e cópia: exemplar controla cada unidade e localizacao diz onde ela está.
4. Resolvemos os relacionamentos N:N com as tabelas livro_autor e item_emprestimo.
5. Normalizamos e definimos chaves primárias e estrangeiras.
6. Criamos e testamos o banco em SQL com dados de exemplo.
