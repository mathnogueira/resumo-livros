# Factory

## Motivações:
- Evitar a dependência de classes concretas;
- Facilidade de trocar a implementação concreta sem alterar todos os arquivos que dependem delas;
- O uso da _keyword_ _new_ é ruim no código, pois indica uma violação no DIP

# Modos de seleção de instância
- Existem diversos métodos para selecionar qual implementação a fábrica deve criar:
    - Métodos separados (`makeA()`, `makeB()`, etc)
    - Parâmetro do tipo `enum` para selecionar a implementação
    - Parâmetro dinâmico (`string` por exemplo)