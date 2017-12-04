# TDD

- Não escreva _production code_ antes de ter escrito um teste que falha;
- Você não deve escrever mais de um teste que falha ao mesmo tempo;
- Você não deve escrever mais código de produção do que o necessário para o teste passar;

- A qualidade do código dos testes devem ser equivalente ao código de produção;
- Quando o código da suite de testes não é bem estruturado, você pode ter problemas para mantê-los e, devido ao alto custo de manutenção, descartá-los. Isso fará com que o seu software apodreça rapidamente;
- O que torna um teste limpo?
    - Readability
        - Clarity
        - Simplicity
        - Density of expression
- Usar o padrão Build-Operate-Check quando escrever testes;
- Um conceito por teste;

- F.I.R.S.T.
    - Fast: testes devem ser executados rapidamente;
    - Independent: Um teste não deve causar efeitos colaterais em outro;
    - Repeatable: testes devem ser reproduzíveis em outro ambiente
        - Você deve ser capaz de executá-los mesmo sem internet ou qualquer outra coisa, pois isso pode causar desculpas do porquê os testes estão falhando;
    - Self-Validating: testes devem ter uma saída booleana, para que assim você não tenha que ler os resultados e interpretá-los você mesmo;
    - Timely: Testes de unidade devem ser escritos antes do código de produção que os fazem passar;