# Interface Segregation Principle (ISP)

## Sintomas
- Interfaces gordas
- Classes concretas que utilizam partes da interface, mas omitem a implementação de um grupo de métodos da interface;

## Resumo
- Interfaces gordas fazem com que alterações na mesma causem compilação de diversos artefatos e distribuição de itens que não foram alterados;


## Notas
- Interfaces devem conter apenas métodos utilizados por **TODAS** classes abstratas que a utilizam.
- Mesmo que uma função _g_ dependa de duas interfaces, que no momento da execução irão referenciar o mesmo objeto, não utilize a interface global. Segregue-as.