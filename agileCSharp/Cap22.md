# Template Method

- Faz uso de herança;
- Cria um _template_ com funções abstratas que devem ser implementadas por seus filhos;
- Uma classe filha do template sempre utilizará a implementação da classe pai;
- Rígido.

# Strategy

- Faz uso de delegação;
- Utiliza a inversão de dependencia;
- Uma mesma _strategy_ pode ser utilizado por diversos componentes, ela não está presa em um componente.