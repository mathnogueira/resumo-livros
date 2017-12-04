# Smells and Heuristics

## Comments

### Inappropriate Information
- Comentários devem conter notas técnicas e sobre o design da aplicação;
- Não deve conter dados do autor, data, etc;

### Obsolete Comment
- Se você encontrar um comentário obsoleto, atualize-o ou delete-o;

### Redundant Comment
- Comentários que não adicionam nenhuma informação ao código;
- "Comments should say things that the code cannot say for itself";

### Poorly Written Comment
- Se você for escrever um comentário, o escreva bem;

### Commented-Out Code
- "Commented-out code is an abomination";
- Delete códigos comentados, o controle de versão está ai pra isso;

## Environment

### Build Requires More than One Step
- Builds tem que ser simples

### Tests require more than one step
- Você deve ser capaz de executar todos os testes em apenas um comando;

## Functions

### Too many arguments
- Funções devem ter poucos argumentos (até 3);

### Output arguments
- Argumentos de saída vão contra o conceito de OO;

### Flag Arguments
- Se existe uma flag, a função faz mais de uma coisa;

### Dead Function
- Funções que não são chamadas devem ser eliminadas;

## General

### Multiple languages in one source file
### Obvious behavior is unimplemented
- Suas funções devem atender as expectativas do desenvolvedor;

### Incorrect behavior at the boundaries
- Funções devem funcionar em todos os casos, inclusive em _corner cases_;

### Overridden Safeties
- Nunca sobraescreva medidas de segurança:
    - Desligar todos os warnings do compilador;
    - Remover testes que falham;

### Duplication
- Toda vez que você vê uma duplicação, ela pode ser eliminada com abstração;

### Code at wrong level of abstraction
- Constantes, variáveis e funções utilitárias devem ser mantidas na implementação, não na classe base;
- Interfaces com métodos que não são utilizados por todas as classes que a implementam;
- "The point is that you cannot lie or fake your way out of a misplaced abstraction";

### Base classes depending on their derivatives
### Too much information
- Módulos bem definidos têm interfaces bem pequenas;
- Esconda seus dados;
- Esconda suas funções utilitárias;
- Interfaces (e classes abstratas) devem ser pequenas;

### Dead code
- Código morto não é atualizado quando o _design_ muda, então ele fica obsoleto rapidamente;
- Ao detectar codigo morto, delete-o;

### Vertical Separation
- Variáveis locais devem ser declaradas o mais proximo de seu uso possível;
- Métodos privados devem estar logo em seguida de sua chamada;

### Inconsistency
- Se você faz algo de uma maneira, faça de maneira similar todos os outros;

### Clutter
- "Variables that aren’t used, functions that are never called, comments that add no information, and so forth";

### Artificial Coupling
- Coloque variáveis, funções e constantes no lugar mais apropriado, não no mais fácil;

### Feature Envy
- Se um método manipula os getters e mutators de outra classe, ela pode ser movida para a outra classe;
- Existem exceções a esta regra (Classe de relatórios acessam outras classes, mas mover os métodos para estas classes não seria correto);

### Selector Arguments
- Mesmo princípio da flag;

### Obscure intent
- Código deve ser bem escrito para mostrar a intenção do código;

### Misplaced responsibility
### Inappropriate Static
### Use explanatory variables
### Function names should say what they do
### Understand the algorithm
### Make logical dependencies physical
### Prefer polymorphism to if/else or switch/case
### Follow standard conventions
### Replace magic numbers with named constants
### Be precise
- Não deixe de fazer as coisas certas por preguiça
    - Usar todos os atributos como `protected` para não se preocupar com visibilidade;
    - Não tratar `locks`;
### Structure over convention
- Definir estruturas é mais rígido do que convenções
    - Uma interface força a implementação de métodos, enquanto um switch/case não;
### Encapsulate Conditionals
- Deixa o código mais legível:
```C#
if (shouldBeDeleted(timer))
```
vs
```C#
if (timer.hasExpired() && !timer.isRecurrent())
```
### Avoid negative conditionals
### Functions should do one thing
### Hidden temporal coupling
- Explicite funções que têm dependencia temporal:
```C#
saturateGradient();
reticulateSplines();
diveForMoog(reason);
```
vs
```C#
Gradient gradient = saturateGradient();
List<Spline> splines = reticulateSplines(gradient);
diveForMoog(splines, reason);
```

### Don't be arbitrary
- Se suas decisões de projeto parecerem arbitrarias, outros irão realizar mudanças nas mesmas;
- Se você mostrar confiança em suas decisões, outros irão utilizá-las no restante do sistema;

### Encapsulate boundary conditions
```C#
if(level + 1 < tags.length)
{
    parts = new Parse(body, tags, level + 1, offset + endTag);
    body = null;
}
```

```C#
int nextLevel = level + 1;
if(nextLevel < tags.length)
{
    parts = new Parse(body, tags, nextLevel, offset + endTag);
    body = null;
}
```

### Functions should descend only one level of abstraction
- Não misture níveis de abstração na mesma função;

### Keep configurable data at high levels
- Funções de baixo nível devem receber a configuração por parâmetro, e não defini-los por meio de condicionais:
```C#
if (arguments.port == 0) // use 80 by default
```
- Coloque a parte configurável em módulos de alto nível;

### Avoid transitive navigation
- Evite train wrecks, pois eles tornam a refatoração muito difícil;

## Names

### Choose descriptive names
- Não utilize o primeiro nome que você encontrou;

### Choose names at the appropriate level of abstraction
- Não escolha nomes que falam sobre a implementação, escolha nomes que refletem o nível de abstração que você está trabalhando;

### Use standard nomenclature where possible
- Utilize nomes que indicam convenções: Decorator, Factory, Visitor, etc;

### Unambiguous names
- Utilize nomes que expressam o que a função faz (`doRename()` vs `renamePage()`);

### Use long names for long scopes
- Escopos pequenos permitem variáveis com nomes pequenos;
- Grandes escopos (classes) merecem nomes mais detalhados;

### Avoid encodings
- Não utilize prefixos;

### Names should describe side-effects
- `getOos()` vs `createOrReturnOos()`;

## Tests

### Insufficient tests
- Você deve criar testes para validar todas as condicionais que podem ser exploradas;

### Use a coverage tool
- Conseguem indicar módulos que necessitam de mais testes;

### Don't skip trivial tests
### An ignored test is a quest about ambiguity
- Se você não sabe escrever o teste por conta do resultado esperado, você deve tirar suas dúvidas sobre os requisitos;

### Test boundary conditions
### Exhaustively test near bugs
- Se você encontrar um bug em uma função, teste mais a função, provavelmente o bug não estava sozinho;

### Patterns of failure are revealing
- Encontre padrões que fazem com que o teste falhe
    - Números negativos;
    - Strings com tamanho maior que X;

### Tests should be fast
- Uma suite de testes que é lenta, não é executada constantemente;