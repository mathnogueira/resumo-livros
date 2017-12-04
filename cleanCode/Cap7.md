# Error Handling

- Se o tratamento de erros ofusca a lógica do código, ela está sendo feita de forma errada;

- Checked Exceptions violam o OCP, pois se muda o tipo da exceção, todos os níveis de chamada intermediárias ao catch e o throw terão de ser modificadas;

- Não retorne códigos de erro;
- Não retorne Null, utilize uma exceção ou NullObject.