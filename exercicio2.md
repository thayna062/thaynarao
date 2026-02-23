1. O que é o Node.js?
O Node.js é um ambiente de execução JavaScript no lado do servidor (server-side).

Ele permite executar código JavaScript fora do navegador, utilizando o terminal ou servidores.

Ele é considerado um ambiente de execução porque:

Não é uma nova linguagem.
Executa código JavaScript usando um motor (engine).
Fornece APIs próprias para acessar sistema de arquivos, rede, processos, etc.
Ou seja, ele executa JavaScript — não é a linguagem em si.

2. Diferença entre Node.js e JavaScript no navegador
Duas diferenças principais:

1️⃣ Ambiente de execução

No navegador: roda no browser (Chrome, Firefox etc.)
No Node.js: roda no servidor ou terminal
2️⃣ Objetos disponíveis

Navegador: possui window, document, DOM
Node.js: não possui DOM, mas possui fs, http, path
Resumo:

Navegador → manipulação de interface
Node.js → backend e aplicações server-side
3. O que é o V8 Engine?
O V8 é o motor JavaScript criado pelo Google para o navegador Google Chrome.

Ele:

Compila JavaScript para código de máquina
Executa o código de forma extremamente rápida
O Node.js utiliza o V8 para interpretar e executar JavaScript fora do navegador.

4. O que é I/O não bloqueante?
I/O significa Input/Output (entrada e saída de dados).

No Node.js, operações como:

Ler arquivos
Acessar banco de dados
Fazer requisições HTTP
são feitas de forma assíncrona e não bloqueante.

Isso significa que:

O programa não para esperando a resposta.
Ele continua executando outras tarefas.
Isso melhora o desempenho porque:

Permite atender múltiplas requisições ao mesmo tempo.
Evita que o servidor fique parado esperando operações demoradas.
5. O que é o Event Loop?
O Event Loop é o mecanismo responsável por:

Gerenciar operações assíncronas
Executar callbacks quando as tarefas terminam
Funcionamento resumido:

O código é executado.
Operações assíncronas vão para a fila.
Quando terminam, entram na fila de eventos.
O Event Loop verifica a fila e executa os callbacks.
Ele permite que o Node.js seja single-threaded, mas altamente eficiente.

6. O que são módulos no Node.js?
Módulos são arquivos ou bibliotecas reutilizáveis que organizam o código.

Tipos:

🔹 Módulos internos Já vêm com o Node.js. Ex: fs, http, path

🔹 Módulos externos Instalados via npm. Ex: express, axios

🔹 Módulos próprios Criados pelo desenvolvedor. Ex: calculadora.js, usuario.js

Eles permitem organização e reutilização do código.

7. Para que serve o package.json?
O package.json é o arquivo que gerencia o projeto Node.js.

Ele pode conter:

Nome e versão do projeto
Dependências
Scripts (ex: "start": "node app.js")
Autor
Licença
Ele é criado com:

npm init
8. O que é o npm?
O npm é o gerenciador de pacotes do Node.js.

Funções:

Instalar bibliotecas
Gerenciar dependências
Atualizar pacotes
Executar scripts
Exemplo:

npm install express
9. O que é uma API REST?
API REST é uma interface que permite comunicação entre sistemas usando HTTP.

Ela utiliza métodos como:

GET
POST
PUT
DELETE
O Node.js pode ser usado para criar APIs REST utilizando frameworks como o Express.js.

Exemplo:

Criar rotas
Receber requisições
Enviar respostas em JSON
10. Vantagens e desvantagens do Node.js
✅ Vantagens:
Alta performance (V8)
I/O não bloqueante
Mesmo JavaScript no front-end e back-end
Grande ecossistema (npm)
❌ Desvantagens:
Não é ideal para tarefas muito pesadas de CPU
Código assíncrono pode ficar complexo
Dependência excessiva de pacotes externos
