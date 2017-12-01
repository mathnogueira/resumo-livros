# Comments

- Não comente código ruim, reescreva-o;
- Comentários podem mentir;
- O melhor comentário é aquele que você encontrou uma forma de não escrever;
- Comentários indicam fracasso em escrever código claro o suficiente;
- Podem ser utilizados para descrever porções de códigos que não podem ser alterados (3rd party software, standard library, etc);
- Podem indicar consequências de executar alguma função ou módulo de uma determinada forma (exemplo: teste que manipula o filesystem e demora vários minutos para executar);
- Todo: podem ser adicionados ao código, porém, devem ser relacionados a tarefas que devem ser realizadas no futuro e não podem ser realizadas agora. Isso não é uma desculpa para deixar código ruim com um comentário TODO: melhorar.

## Comentários ruins

- Comentar o funcionamento de alguma solução ruim. Gaste o tempo para reescrever a solução;
- Comentários que mentem;
- Comentários obrigatorios (Javadoc por exemplo)
- Não devemos utilizar um comentário quando podemos utilizar uma função ou variável:
```C#
// does the module from the global list <mod> depend on the
// subsystem we are part of?
if (smodule.getDependSubsystems().contains(subSysMod.getSubSystem()))
```
- Marcadores de posição:
```C#
// ========================= Methods ====================== 
```
- Indicadores de fechamento de bloco;
- Indicadores de alterações: (Alterado por Matheus em 21/11/2017 15:45);
- Código comentado;
- Comentários com muita informação;
- Javadoc em funções não públicas;
