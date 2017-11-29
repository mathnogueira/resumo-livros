# Observer

- Utilizado para que um objeto seja notificado quando uma determinada ação seja executada
- Faz com que classes não gastem processamento desnecessário (dentro de um loop para saber se pode executar uma determinada tarefa);
- A classe observadora não precisa conhecer os detalhes para saber se ela deve executar uma tarefa.
- Cuidado com observers, o uso excessivo fazem sistemas serem difíceis de serem endendidos e rastreados

## Modelos

- Pull
    - O método `Update()` do Observer é chamado sem nenhum parâmetro e ela é responsável por realizar a atualização (utilizado quando a resposta para a pergunta "O que mudou?" é obvia);

- Push
    - O método `Update()` do Observer é chamado com uma dica (`Hint`) para informar qual foi o tipo de atualização realizada.

- O modelo é escolhido dependendo da complexidade do objeto que está sendo observado.

## Notas

- Está de acordo com o OCP (você pode adicionar novos observers sem alterar o Subject).