# Meaningful Names

- Dê nomes que revelam sua intenção;
- Nomes que precisam de um comentário para revelar sua intenção não são bons nomes;
- Nomes devem ser pronunciaveis;
- Nomes devem ser procuráveis;
- IFactory vs Factory:
    - Porque temos que dizer a nossos usuários que eles estão trabalhando com uma interface?

- Classes devem ser nomeadas com substantivos;
- Métodos devem ter verbos em seu nome;
- Quando existe sobrecarga de construtores, utilize métodos estáticos para facilitar a criação do objeto:
```C#
Complex fulcrumPoint = Complex.FromRealNumber(23.0);
```
mostra mais o intuito do método do que a solução abaixo:
```C#
Complex fulcrumPoint = new Complex(23.0);
```

- Não utilize várias palavras para o mesmo conceito
    - `fetch()` vs `get()` vs `retrieve()`?
- Não utilizar a mesma palavra para duas ações diferentes:
    - Se o nome é o mesmo, as entradas e saídas do método devem ser semanticamente parecidas;
    - Quaisquer mudanças semanticas devem impactar no nome do método;

- Use Solution Domain Names quando aplicáveis (termos de padrões, matemáticos, área de computação, etc);
- Use Problem Domain Names (nomes referentes ao problema a ser resolvido [outorga por exemplo]);
- Não adicione mais contexto a uma variável do que o necessário para o seu entendimento;