# Boundaries

- Boundaries são pontos do sistema em que são necessárias integrações com outros sistemas ou subsistemas;
- Learning tests: testes usados para tentar entender o funcionamento de uma 3rd party library;
- Learning tests podem ser mantidos para verificar se uma nova versão da lib trocou o comportamento de algum componente
    - Incentiva o uso de novas versões da lib;

- Para abstrair Boundaries, podemos criar a interface que nós gostariamos de usar, e criar uma implementação falsa em cima dessa API. Quando a API correta for finalizada, podemos criar um `Adapter` que implementa nossa interface e realiza a conexão entre nossa aplicação e a interface real;
- Quando trabalhamos com coisas que são fora de nosso controle, devemos ter o mínimo de referências a esta coisa;
