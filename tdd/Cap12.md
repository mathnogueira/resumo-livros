# Quando não usar TDD?

- Códigos que lidam com infraestrutura ou camada de visualização;
- Não significa deixar as coisas sem testes automatizados;
- Buscar 100% de cobertura pode ser inútil;
- Métodos simples **talvez** não precisem de testes, porém isso não é uma regra. Alguns métodos simples são cruciais para o aplicativo e podem ser quebrados por alterações futuras.

- É importante ver o teste falhar, pois isso mostra que não existem bugs no teste;
- Refatoração é uma etapa muito importante para o TDD, pois auxilia o desenvolvedor a refinar o _design_ da aplicação;