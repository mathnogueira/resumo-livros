# Functions

- Funções devem ser pequenas;
- A indentação de uma função não deve passar de um ou dois níveis;
- Devem realizar apenas uma tarefa;
- Uma mesma função só deve trabalhar no mesmo nível de abstração:
```C#
// Dois níveis de abstração em uma mesma função
var users = userRepository.fetchUsers();
foreach (var user in users) {
    var userPurchases = session.Query<Purchases>()
        .Where(purchase => purchase.User.Id == user.Id)
        .ToList();
}
```

- Funções devem contar uma história;
- Um nome longo é melhor do que um curto enigmático;
- Parâmetros de saída são confusos:
```C#
public void IncludeSetupPageInfo(StringBuffer pageText) {}
```

Poderia ser feito para que a função retornasse um novo StringBuffer
```C#
public StringBuffer Transform(StringBuffer in) {}
```
- Flags são ruins e indicam que a função faz mais de uma coisa
- Quando alguns argumentos fazem parte de um objeto maior, você pode extraí-los e criar um wrapper. Por exemplo:

```C#
public Geometry MakeCircle(double x, double y, double radius);
public Geometry MakeCircle(Point center, double radius);
```

- Não pode causar efeitos colaterais
    - Cria um acoplamento temporal na função, pois ela pode ser executada normalmente n vezes, mas na (n+1)th vez, ela falhará conta conta do contexto atual da aplicação;

- Funções devem fazer algo ou responder algo, não ambos;
- Exceções são melhores do que códigos de erro;
- Extraia blocos de try/catch em funções próprias;
- Segundo Dijkstra, uma função só pode conter um `return`, não podem existir `breaks`, `continues` ou `gotos`;