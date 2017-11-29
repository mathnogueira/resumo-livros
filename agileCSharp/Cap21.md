# Command

## Características
- Mantém uma ação isolada dentro de uma classe;

## Vantagens
- Desacoplamento físico
    - O comando fica isolado dentro de uma classe e pode ser executado por diversos clientes.
- Desacoplamento temporal
    - O comando não precisa ser executado logo após sua criação;
    - Pode ser agendado para ser executado;
- Possibilidade de manter o contexto da ação isolada no objeto
    - Facilita a implementação de desfazer a ação

# Active Object

# Características
- Utilizado para prover tarefas multithread;
- Fila de _Commands_ que são executados em sequência;
- Um _Command_ pode ser colocado ao final da fila após sua execução (_SleepCommand_ por exemplo).
