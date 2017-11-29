# Liskov Substitution Principle (LSP)

## Sintomas
- Quando se troca o subtipo do objeto faz o programa se comportar de maneira incorreta;
- Alteração da classe C que faz uso do objeto do tipo S para verificar seu subtipo para que C consiga executar as ações corretamente;
- Uso de verificação de tipos em tempo de execução;

## Resumo
- Exemplo do quadrado, quando um atributo não é declarado _virtual_, mudanças na classe base são forçadas.
- Se o autor de uma função _f_ fizer suposições sobre o tipo S, e o tipo T não se aplique a esta suposição, a relação S -> T viola o princípio de LSP;
- Olhar as classes para ver se elas são coerentes e válidas não é o suficiente para validar o LSP, pois podem existir módulos, que a função _f_, foram desenvolvidas a partir de algumas suposições que não serão respeitadas pelo relacionamento S -> T;
- **É melhor adiar as violações do LSP até que os sintomas sejam visíveis**;
- Fatoração é melhor do que extensão.

### Design por contrato
- Um módulo T devirado do módulo S não pode supor que suas pré-condições sejam mais fortes do que as exigidas por S;
- O módulo T deve obedecer a todas as pós-condições do módulo T;

## Desafios

- Prever algumas suposições que podem ser feitas pelos usuários da classe;
- Não infectar o projeto com complexidade desnecessária;
- Saber quando aceitar uma falha é mais lucrativo do que buscar a perfeição (**MUITO RARO**);

## Notas

- "Podemos afirmar que, se todas as classes em um conjunto de classes aceitam uma responsabilidade comum, elas devem herdar essa responsabilidade de uma superclasse comum.";
- "Uma derivada que faz menos do que sua base normalmente não é substituível por essa base e, portanto, viola o LSP";
- O termo É-Um é amplo demais para ser usado como definição de um subtipo. Devemos verificar se o subtipo é substituível.