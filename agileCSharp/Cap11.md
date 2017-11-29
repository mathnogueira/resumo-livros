# Dependency Inversion Principle (DIP)

## Sintomas
- Módulos de alto nível dependem de classes concretas ao invez de interfaces ou classes abstratas;
- Um projeto OO deve ter suas dependências invertidas;

## Notas
-  "Módulos de alto nível não devem depender de módulos de baixo nível. Ambos devem depender de abstrações."
- " As abstrações não devem depender de detalhes. Os detalhes devem depender das abstrações."
- As interfaces abstratas são definidas no nível hierarquico que ela será empregada (Figura 11-2)
- Nenhuma variável deve conter uma referência para uma classe concreta;
- Nenhuma classe deve derivar de uma classe concreta;
-  Nenhum método deve sobrescrever um método implementado de qualquer uma de suas classes base.