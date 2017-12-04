# Emergence

Quatro regras para ter um bom design na ordem de importancia:

## Execute todos os testes
- Sistemas que não são testáveis, não são verificaveis;
- Se você não consegue verificar a exatidão de um sistema, todo o esforço para desenhá-lo no papél foi em vão;
- Alto acoplamento é difícil de testar;
- Um sistema testável segue os princípios SOLID;
- Tendo um sistema que é verificado a cada iteração, é possível realizar refatorações e melhorá-lo constantemente;=

## Não tenha código duplicado
- Duplicação representa trabalho adicional, risco adicional e complexidade desnecessária;
- Template method pode ser utilizado para resolver a duplicação;

## Expresse o que você quer dizer no código;
- Escolha bons nomes que sejam pronunciáveis;
- Classes e métodos pequenos;
- Utilizar o nome de padrões de projeto para expressar sua intenção;
- Testes de unidade bem escritos;
- "Remember, the most likely next person to read the code will be you.";

## Minimize o número de classes e métodos;
- Alto número e baixo número de classes são problemas;
- Imagine se para toda classe escrita, seja necessário criar uma interface, ou então, que exista a separação de classes (Model) de dados e classes de comportamento (Services)
    - Martin Fowler (https://www.martinfowler.com/bliki/AnemicDomainModel.html)