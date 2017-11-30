# TDD e o acoplamento

- Utilização de _mocks_ para imitar o comportamento de algum componente que será testado por outra _suite_ de testes;
- Classes que têm muitas dependências (explicitas pelo contrutor), geralmente, são chamadas de _God Classes_;
- Dependência de classes concretas é ruim;
- Métodos estáticos não podem ser passados via contrutor, portanto, é importante criar abstrações que trabalhem com os métodos estáticos. Por exemplo, imagine que você tenha que trabalhar com o método `DateTime.Now`. Não é possível construir um `mock` desse método pelo fato dele ser estático, portanto, o mais sensato seria criar uma abstração `IRelogio` que é capaz de obter a hora atual do sistema;