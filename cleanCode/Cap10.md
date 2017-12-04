# Classes

- Ordem das variáveis de uma classe:
    - public static constants;
    - private static variables;
    - private instance variables;
    - public variable (você precisa de uma ótima argumentação para utilizar uma destas);

- Classes devem ser pequenas (ter apenas uma responsabilidade);
- O mais ambiguo o nome de uma classe, o mais fácil é de detectar que ela faz mais de uma coisa;
- Descreva o que a classe faz:
    - Se você utilizar palavras "se", "e", "ou", "mas", isso indica que ela tem mais de uma responsabilidade;
- Se uma classe tem mais de um motivo para mudar, ela está fazendo muita coisa;
- Várias classes são melhores do que poucas classes;
- Se uma classe contém algumas variáveis que são utilizadas somente por uma fração de seus métodos, podemos extrair uma nova classe;
- "When classes lose cohesion, split them";
- Nunca depender de detalhes, sempre de abstrações;
