# Estado

- Cada estado do AFD é representado por uma classe, que aplica as ações cabíveis para cada possível ação (transição);
- Faz parte do conjunto do padrão STRATEGY;
- Diferente do STRATEGY, as classes que representam um estado têm uma referência ao contexto da aplicação
    - No exemplo da roleta, os estados de RoletaTravada e RoletaDestravada têm a referência para o objeto Roleta, o qual contém as ações que devem ser executadas na transição entre estados.
- Muito massante, as vezes é melhor ter algum gerador de código para gerar o código da máquina de estados.