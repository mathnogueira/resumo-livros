# Visitor

- Aplica alterações nas classes sem que a classe tenha de ser alterada;
- Cria um visitor que recebe uma entidade como parâmetro no método Visit(T item)
    - Essa função irá manipular o item do tipo T para realizar a ação;
- Adiciona-se um visitor a uma entidade pelo método Accept(Visitor v);
- Faz com que o visitor se preocupe com a implementação das novas funcionalidades, sem que as classes tenham que sofrer grandes alterações;
- Não é muito escalável, pois o Visitor necessita de um método `Visit(T)` para cada T na hierarquia a ser visitada, portanto, se novos tipos são adicionados à hierarquia com frequência, o Visitor terá de ter modificado e conterá muitos métodos.

# Acyclic visitor
- Resolve o problema de escalabilidade do Visitor
- Esconde a dependencia entre o _target_ e o _visitor_ utilizando interfaces
    - O método `Accept(Visitor)` deverá verificar se a instância recebida é do tipo esperado, se for, invoca o método `Visitor.Accept(this);`;
- Isso faz com que seja mais simples adicionar derivadas visitadas e fazer compilações incrementais
    - Com o custo de deixar a solução mais complexa;
- Se um item da hierarquia não pode ser visitado (limitações como por exemplo, o `ErnieModem` não pode ser configurado para o UNIX), o `Visitor` concreto não precisa implementar a interface `ErnieModemVisitor`.

- Só deve ser utilizado se a hierarquia visitada é volátil e é alterada constantemente, senão, o aumento da complexidade e perda de desempenho não valem a pena;

## Usos de Visitors

- Geração de relatórios
    - A estrutura de dados aceita um visitor, que é responsável por criar o relatório a partir da estrutura;
    - Separa a estrutura de dados e as classes de geração de relatório
        - A estrutura de dados não precisa ser alterada se um novo relatório é adicionado
- Pode ser aplicado para analisar estruturas de dados de diversas formas;


# Decorator

- Altera o funcionamento de uma classe em tempo de execução;
- Funciona como um _wrapper_ da classe para que quando uma ação seja executada, alguma alteração seja feita e assim a real ação seja delegada para a implementação correta.

# Extension Object

- Existem objetos de extensão que são identificados por seu nome;
- Na construção de um objeto, este explicita quais extensões estão acessíveis para aquele tipo de dado;
- Extensões são adicionadas à classe em tempo de execução, sem a necessidade de explicitá-las no código por meio de composição direta ou herança;
- As extensões fazem o "trabalho sujo" sem que a classe alvo tenha que sofrer alterações.