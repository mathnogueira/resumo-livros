# Objects and Data Structures

"There is a reason that we keep our variables private. We don’t want anyone else to depend on them. We want to keep the freedom to change their type or implementation on a whim or an impulse. Why, then, do so many programmers automatically add getters and setters to their objects, exposing their private variables as if they were public?"

- Train crash: Invocar métodos de objetos que foram retornados por outro método de forma encadeada;

- Demeter: não podemos acessar os conteúdos internos de um objeto, porém, se esse objeto for apenas uma estrutura de dados, isso não se aplica;

- Estruturas de dados não têm a necessidade de ter membros privados, já que eles serão acessados via getter, isso só causa retrabalho e não protege nada do objeto;

- Nunca misture objetos e estruturas de dados. Objetos realizam ações e escondem suas partes internas, enquanto estruturas de dados são utilizadas para guardar dados;

- Objetos expõem comportamento (métodos); Estruturas de dados expõem dados e não têm comportamentos significantes.