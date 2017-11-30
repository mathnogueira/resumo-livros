# TDD e o encapsulamento

- Classes que sabem demais sobre o comportamento de outras classes não são boas;
- Classes devem controlar seu próprio estado
    - Tell, Don't ask
- Lei de demeter: uma dependência interna de uma classe não pode ser utilizada pelo seu contexto externo. Simplificando: você deve evitar (não é uma regra escrita na pedra):
```C#
    var pagamentosValidos = fatura.Pagamentos.Where(p => p.Valido).ToList();
```

Você deve utilizar:
```C#
    var pagamentosValidos = fatura.GetPagamentosValidos();
```

Isso evita que mudanças na implementação da classe `Fatura` cause problemas em outras classes que fazem acesso direto a suas dependências.

- Componentes não encapsulados criam oportunidades de outros componentes se tornarem sensíveis a sua implementação interna, causando problemas de acoplamento.