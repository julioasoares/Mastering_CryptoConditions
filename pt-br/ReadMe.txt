Como escrever Contrados CryptoConditions baseados em utxo para KMD chains 
Por jl777

Esta não é a única metodológia de smart contracts que pode ser construída sobre OP_CHECJKCRYPTOCONDITION, é apenas a primeira. Todos os créditos por fazer funcionar OP_CHECJKCRYPTOCONDITION no codebase da Komodo vão para @libscott. Eu estou apenas <i>hooking</i> no código criado por ele e tentei tornar um pouco mais fácil para a criação de novos contratos.

Provavelmente deve haver um termo de marketing elegante para se usar, mas por hora vou chamar simplesmente de "contrato CC" para abreviar. Sabendo já que isto não é 100% preciso tecnicamente uma vez que o aspecto <i>CryptoConditions</i> não é na verdade seu atributo principal. No entanto os contratos KMD foram de fato criados para tornar mais acessível as CryptoConditions que foram integradas ao codebase.

Uma vez que rodam código C/C++ nativo, contratos CC são <i>turing complete</i> e isso quer dizer que qualquer contrato possível de ser feito em outras plataformas poderá ser criado via contrato CC. 

Contratos baseados em utxo são um pouco mais difíceis para se começar a escrever do que contratos baseados em saldos. No entanto eles são muito mais seguros uma vez que se apoiam no sistema utxo existente do bitcoin. Isso faz com que seja muito mais difícil de se encontrat bugs que emitam um <i>zilhão</i> de moedas por um pequeno erro de programação, já que a operação de todo e qualquer contrato CC também precisa obedecer o protocolo utxo bitcoin existente.

Este documento será fortemente baseado em exemplos de forma que vai usar muito os contratos CC de referência existentes. Após compreender este documento, você deverá estar numa boa posição para começar a criar um novo contrato CC para ser integrado ao komodod ou para diretamente criar <i>dapps</i> baseadas em RPC. 

Capítulo 0 - Noções Básicas do Protocolo Bitcoin
Capítulo 1 - OP_CHECKCRYPTOCONDITION
Capítulo 2 - Noções Básicas de contrato CC
Capítulo 3 - CC vins e vouts
Capítulo 4 - Extensões RPC CC
Capítulo 5 - Validação CC
Capítulo 6 - Exemplo de torneira (faucet)
Capítulo 7 - Exemplo de recompensas (rewards)
Capítulo 8 - Exemplo de ativos (assets)
Capítulo 9 - Exemplo de jogo de dados (dice)
Capítulo 10 - Exemplo de loteria (lotto)
Capítulo 11 - Example de canais (channels)
Capítulo 12 - Possibilidades ilimitadas
Capítulo 13 - Diversas linguagens
Capítulo 14 - Ligações em tempo de execução
Capítulo 15 - dapps basedas em RPC