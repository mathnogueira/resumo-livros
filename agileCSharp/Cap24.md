# Singleton
- Classe tem um método estático que testa a existência de uma instância e sempre retorna a mesma instância;
- Não é possível mockar o uso de um singleton;
- Melhor usado quando se deseja restringir por meio de derivação.

# Monostate
- O valor é compartilhado entre todas as instâncias;
- O valor é _static_;
- É possível criar objetos de _Mock_;
- Melhor usado quando a singlaridade da classe deve ser transparente para seus usuários ou quando se quer utilizar derivações polimórficas do único objeto.