# Systems

- Lazy instantiation pode ser ruim, pois a instanciação é feita hard-coded;
- Fábricas
- Injeção de dependências
- Não iremos acertar de primeira no sistema, porém, devemos os evoluir para atender as novas necessidades;
- Os módulos devem ser separados (SRP);
- Sua arquitetura não deve definir influenciar a maneira que seu código é escrito, você deve separar seus objetos das responsabilidades da arquitetura:
    - Ex: seus modelos não devem estender uma classe para que ele seja persistente;
- Sua arquitetura não deve ser pensada toda logo no início, pois isso inibe a adaptação para mudanças;
- Padrões (EJB2 por exemplo) devem ser usados somente se eles trouxerem benefícios;
- "An invasive architecture overwhelms the domain logic and impacts agility"