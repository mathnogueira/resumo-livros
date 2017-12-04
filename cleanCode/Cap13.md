# Concurrency

- Concorrencia nem sempre aumenta a performance do programa:
    - Troca de contexto do SO;
    - Troca dos dados que estão na cache;
    - TLB é esvaziada (acesso à memória fica mais lento)
- Design da aplicação deve ser alterada;
- Recomendação: Mantenha seu código paralelo separado do restante do código;
- Limite o acesso a dados compartilhados;
- Faça com que cada thread funcione independentemente;
- Utilize bibliotecas que suportam multithreading (java.collections.concurrency);

## Produtor-Consumidor
- Produtor coloca item no buffer;
- Consumir consome o item da lista;

## Writers-Readers
- Devemos encontrar um ponto de equilibrio quando damos prioridade para uma categoria desses serviços, pois podemos encontrar problemas de performance;

## Jantar dos filosofos

## Recomendações
- Evite usar mais de um método `syncronized` em dados compartilhados;
- Métodos `syncronized` devem o mais breve possível;
- Se é necessário que o processo execute e se desligue de forma natural, faça isso o mais rápido possível (no início do projeto), pois é algo muito complicado;
- Escreva testes com multiplas configurações e multiplas cargas, se alguma vez ele falhar, não ignore a falha só porque o teste passou na proxima execução;
- Não ignore falhas como "one-offs";
- Faça seu código não-paralelo funcionar primeiro;
- Não tente solucionar bugs causados por multithread e bugs normais ao mesmo tempo, tenha certeza que seu código funciona com uma thread;
- Faça o seu código Plugável (permita múltiplas configurações):
    - N threads;
    - O código deve ser capaz de iteragir com componentes reais e mockados;
    - Execute o teste com mocks que executam rapidamente e depois lentamente, varie as condições;
    - Configure seus testes para eles executarem diversas vezes;
- Execute o código com mais threads do que processadores para incentivar a troca de contexto em cada processador e poder encontrar alguns problemas;
- Realize testes em diferentes plataformas;
- Faça com que seu código possa forçar as falhar: Utilize `Object.wait()`, `Object.sleep()`, `Object.yield()` e `Object.priority()` para tentar forçar os erros:
    - O uso desses comandos não quebram o código, mas sim evidenciam as falhas no seu código;
    - Adicione esses métodos de forma automática:
        - Crie uma interface `ThreadJiglePoint` e utilize-a para adicionar estes métodos ao código, em produção, utilize uma implementação vazia;