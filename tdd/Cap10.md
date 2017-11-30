# Testes de integração e TDD

- Utilizados para testar o comportamento do sistema como um todo, executando as unidades em conjunto com suas dependências concretas;
- Classes de comunicação com infraestrutura, caso usem dependências, estas não precisam ser mockadas;
- TDD não faz muito sentido ser aplicado a testes de integração, a não ser que a integração a ser testada é muito complexa;

- Quanto mais completo o teste (unidade -> integração -> sistema), mais sensível e mais caro ele se torna.
