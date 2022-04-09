# POC SQS

[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



## Sobre o projeto

Projeto desenvolvido para validar, de forma simples e prática, a teoria aprendida com o curso de AWS SQS da plataforma Alura. 
Foi desenvolvida uma aplicação utilizando **Node.js** que simula o envio e recebimento de mensagens em uma fila da **AWS SQS**. A mensagem consiste em 
informações de uma transação bancária fictícia, contendo número das contas do remetente e do destinatário e também o valor
a ser transferido. O processamento da mensagem se dá com a confirmação do envio desse valor. 

Também foi definido o envio de uma 
"mensagem envenenada", ou seja, uma mensagem no formato XML que o consumidor não consegue processar, pois só é capaz de ler 
mensagens no formato JSON. Após 3 tentativas de processamento da mensagem envenenada, ela é redirecionada para a fila morta (sql).
Por fim, também há o processador de mensagens na fila morta que a exclui ao fim do processo.

No projeto há as seguintes funcionalidades:
- send-message 
- send-poison-message
- receive-messages
- receive-dlq-messages

Além disso, foi feita a simulação de producer e consumer de uma fila FIFO (first-in-first-out):
- send-fifo-message
- receive-fifo-messages

## Tecnologias utilizadas
- Node.js
- AWS SDK

## Autor

LinkedIn: https://www.linkedin.com/in/emanuele-rangel-7b50971b8/

e-mail: emanuele.rangel52@gmail.com
