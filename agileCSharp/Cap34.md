# Proxy
- É colocado entre duas classes sem que elas saibam da existência dele;
- Exemplo dado é um Proxy que implementa a interface _Product_, e quando uma _property_ de _Product_ é invocada, ele acessa o banco, procura o produto com o código e retorna aquela propriedade. Portanto, para o cliente, ele não faz ideia que aquele produto não é um produto de fato, pois o Proxy implementa a interface;
- Um proxy se comporta exatamente como o item que está sendo substituído, porém, sua função é atravessar alguma barreira (network, database, file system, etc);
- Normalmente, um proxy é dividido em três partes:
    - Interface
    - Implementação
    - Proxy
- No exemplo de um banco de dados, o proxy carrega os dados, constroi a implementação e delega o trabalho para a implementação. Isso ocorre porque é interessante que a implementação seja o ponto central que contenha a regra de negócio. Dessa maneira, é possível criar diversos proxies para diversas ocasiões e centralizar as regras de negócio;
- Ajuda na inversão de dependências;
- Proxies mudam quando a API externa muda ou quando o aplicativo muda (são os pesadelos, mas estão centralizados);

# Gateway (Data Table Gateway)
- Mais simples do que o Proxy
- Utiliza uma interface para cada entidade do sistema, e.g. UserGateway, OrderGateway, ProductGateway, etc;
- Por conta da existência da interface, é possível intercalar implementações concretas (ex: DbOrderGateway, InMemoryOrderGateway), isso causa uma grande flexibilidade no momento de testar o aplicativo;
