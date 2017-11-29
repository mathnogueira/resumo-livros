# Abstract Server
- Cria uma abstração que será utilizada para realizar a comunicação entre um objeto e outro;
- A relação da interface é mais forte com o cliente (invocador) do que com a classe que irá implementá-la, por esse motivo, a interface deve fazer parte do mesmo pacote físico do que seu cliente;

# Adapter
- Entra em jogo quando não é possível tratar todas as implementações de maneira homogenea;
- Pode ser utilizado para normalizar a API dos diferentes _targets_;
- Deve ser utilizada se o _abstract server_ não for o suficiente para resolver o problema.

# Bridge
- Utilizado para evitar hierarquias exponenciais
- Criação de uma classe abstrata que controla um determinado aspecto independente de plataforma e tem um _link_ para uma abstração que controla os detalhes da plataforma.

## Exemplos

- Modem dedicado vs modem discagem
    - DedModem e DialModem são aspectos independentes do _hardware_, portanto, são representados pela classe abstrata com o link para a abstração da implementação específica do hardware.
    - As implementações de `send()`, `receive()`, `dial()` e `hangup()` são escondidas por uma abstração que é implementada pelos controladores de cada _hardware_.

- Thread Scheduler (from SourceMaking.com)
    - PreemptiveThreadScheduler vs TimeSlicedThread não dependem da plataforma, podem ser implementados de uma forma não dependente da plataforma.