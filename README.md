# Programação Assíncrona

Programação assíncrona permite executar tarefas sem bloquear a execução do código principal. Isso é útil para operações demoradas, como requisições HTTP ou leitura de arquivos, permitindo que o programa continue rodando enquanto espera o resultado.

No <b>Angular</b>, a programação assíncrona é essencial para lidar com chamadas a APIs, timers, eventos de usuário e fluxos de dados dinâmicos.

### 1. Promises

Uma <b>Promise</b> representa um valor que pode estar disponível <b>agora, no futuro, ou nunca.</b>
Ela tem três estados:

- <b>Pending (pendente)</b> – ainda não finalizou
- <b>Resolved (resolvida)</b> – operação concluída com sucesso
- <b>Rejected (rejeitada)</b> – houve um erro

### Exemplo de Promise em TypeScript

     function buscarDados(): Promise<string> {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          const sucesso = true;
          if (sucesso) resolve("Dados carregados!");
          else reject("Erro ao buscar dados.");
         }, 2000);
      });
    }

      // Usando a Promise com .then() e .catch()
        buscarDados()
         .then((dados) => console.log(dados))
         .catch((erro) => console.error(erro));


     // Usando a Promise com .then() e .catch()
       buscarDados()
         .then((dados) => console.log(dados))
         .catch((erro) => console.error(erro));
