# Resumão do Carrilho  | 05.07.2022

---- PLANO: Iniciante em programação.
---- CURSO: Arquitetura de computadores: por trás de como seu programa funciona.

## LINGUAGEM COMPILADA x INTERPRETADA

Para que um computador consiga "ler" o código, este precisa de uma espécie de "tradutor", podendo ser um COMPILADOR ou um INTERPRETADOR, para que a máquina entenda
o que está escrito ali, nas diversas linguagens existentes, algumas são compiladas, outras interpretadas.

### COMPILADA

São linguagens em que primeiro ocorre uma tradução COMPLETA do código para a linguagem da máquina para que posteriormente possam ser executados.
O java por exemplo, compila para JVM bytecode, já o C# para CIL bytecode.
Eventuais erros no código serão mostrados antes da execução.

Exemplos: Java, Go, C#.

#### JIT COMPILE

É a chamada compilação just-in-time, conhecida como tradução dinâmica. Executa e compila o código ao mesmo tempo, sendo considerada um meio termo entre as anteriores
apresentando vantagens de ambos e desvantagens também, é considerada uma "otimização" para a compilação em algumas linguagens.

Exemplos: Java (JVM), C# (CLR)

### INTERPRETADA

Nestes casos ocorre a tradução simultanea em conjunto com a execução.
Eventuais erros no código serão mostrados durante a execução.

Exemplos: Python, JavaScript


## COMPONENTES PRINCIPAIS

**Processador (CPU)**: É o responsável por fazer os calculos lógicos e realizar entradas e saidas de dados, é formado por:
- UC: Responsável por controlar e instruir as ações de um computador, acessar dados na memória etc.
- ULA: Executa as instruções do programa ou dados acessados, sejam elas lógicas, aritméticas etc.
- Registradores: Pequenas memórias que armazenam valores que são utilizados no controle e processamento das instruções.

**Memória RAM:** Armazena dados voláteis de acesso rápido que não ficam salvos.

**SSD e HD:** Armazenam os dados de forma permanente para eventuais acessos.

**Dispositivos de entrada e saída:** Os de entrada são utilizados para darmos instruções aos computadores, já os de saídas são para exibir os resultados, sejam eles em aúdio, imagem entre outros. 


## HIERARQUIA DE MEMÓRIA

![hierarquiacorreto](https://user-images.githubusercontent.com/106081805/177786106-3f7d62e6-0f2a-4828-9af6-622a8d305983.png)


**Registradores:** São as memórias mais rápidas de um computador, ficam localizadas na CPU e possuem o menor armazemento de dados. 

**Memória Cache L1, L2, L3:** São as memórias que também ficam localizadas na CPU e possuem altíssima velocidade, porém baixíssimo armazenamento de dados.

**Memória RAM:** Possuem memória de acesso rápidas com um pouco mais de capacidade.

**SSD e HD:** Possuem grandes capacidades de armazenamento, porém a memória de acesso deles é lenta.

**CLOUD:** Possuem atualmente as maiores capacidades de armazenamento, porém a velocidade deles de transferência de dados é a menor de todas.

-- Créditos ao colega do Movimento Codar Paulo Ferreira por complementar este raciocínio.

## PASS BY VALUE X PASS BY REFERENCE

**O que é?** Quando uma função de um código é chamada, , ela pode passar por valor ou referência.

**Pass by Value:** A grosso modo, o valor do parâmetro da função é recebido e "copiado" para outra variável e então a cópia é utilizada. Não há efeitos no valor original

**Pass by Reference:** Neste caso, o valor do endereço de memória é passado para a função, a mesma recebe o valor "original" do parâmetro, portanto, todas as modificações afetam o valor original.


# Resumão do Carrilho  | 07.07.2022

---- PLANO: Iniciante em programação.
---- CURSO: Jogos clássicos parte 1: Pong com Javascript

## Primeiro Jogo de Pong feito com Scratch

Este foi o primeiro projeto feito na minha vida de um joguinho de pong, foi utilizado a ferramenta Scratch para realizar o jogo com sons, modelo de bolinha e raquetes.

Ao realizar o projeto, notei duas coisas interessantes, a primeira delas foi o comportamento mecânico da raquete do oponente. Para solucionar este problema, na parte final, resolvi implementar uma variável como mostra a imagem a seguir, para que ele a cada 0.2 segundos deslize a raquete em uma posição váriavel de acompanhamento da posição y da bolinha entre 30 e -30, criando assim um comportamento mais "natural".

![erro1projetoscratch](https://user-images.githubusercontent.com/106081805/177782247-175c1207-8914-4af7-829f-51e3521f4f09.png)


A segunda observação, foi em relação aos bugs que estavam ocorrendo, sendo eles o ponto duplo e as vezes a bolinha ficar agarrada tanto encima quanto embaixo, ocasionando problemas de pontuação infinita, confesso que para este problema específicamente não consegui achar uma solução que realmente resolvesse sem criar novos modelos. Então eu resolvi pesquisar e buscar ideias de soluções alternativas e, uma delas que encontrei, foi criar dois novos atores chamados de Borda1 e Borda2 e colocar na função da bolinha que toda vez que fosse contabilizado um ponto, ele devolvesse a bolinha pro centro após 1.5 segundos, resolvendo assim ambos os problemas citados.

![erro2projetoscratch](https://user-images.githubusercontent.com/106081805/177782679-cf5dc5ca-c7c2-4003-85b7-c2188f6bec7f.png)

Segue o resultado: https://scratch.mit.edu/projects/712096504/

## Segundo jogo de Pong feito com P5 Web editor em JavaScript

Este foi o mesmo projeto que o anterior basicamente, porém foi escrito em JavaScript.

Durante a realização do projeto não encontrei muitas dificuldades, a única que foi encontrada era novamente a bolinha agarrando na raquete, porém, utilizei a própria solução proposta no curso para resolve-la. 

Segue o resultado: https://editor.p5js.org/lucascarrilho26/sketches/3f5rifyrj


# Resumão do Carrilho  | 10.07.2022

---- PLANO: Iniciante em programação.
---- CURSO: Jogos clássicos parte 2: laços e listas com JavaScript.

## Terceiro jogo de Pong feito com P5 Web editor em JavaScript

Este foi o segundo jogo feito com o P5 web editor feito em JavaScript, é um jogo baseado no antigo Freeway.

Durante a realização deste projeto, eu acabei tendo a ideia a princípio de modifica-lo com um tema diferente, como, por exemplo, as meninas superpoderosas. Porém, quando comecei a fazer as modificações, acabei
tendo outra ideia, que foi customizar o som de forma diferente. Quando o "ator" colidia com um dos obstáculos, a colisão deveria emitir um som específico para cada colisão, diferente do projeto que a colisão era padrão.

Portanto, eu tive que aprender a colocar cada som específico para cada colisão, ai que veio maior parte do meu estudo neste projeto: Aprendi a utilizar OBJETOS em JavaScript, ou seja, aprendi a acessar objetos dentro de listas, algo que para mim foi algo bem difícil, pois nunca havia visto este tipo de estudo. 

Dito isso, utilizei a lista pra criar os "vilões" declarando-os com o const, que diferente do let pois no primeiro caso você não consegue altera-lo, seria como se fosse um pass by value, impedindo que ele seja modificado. Então, após cria-los, eu usei o comando vilao[i].som.play(), para acessar cada som específicamente quando o if(colisao) passar naquele índice específico, criando assim um som customizado para cada colisão.  <Offtopic: Para aprender isso me custou 3 horas, mas o conhecimento é eterno, foi difícil mas consegui, quase soltei foguete quando deu certo!!>

Outra observação necessária: Eu criei 6 personalidades apesar de utilizar somente 3 (repeti cada uma delas 1x), pois, um dos bugs que encontrei, era que o indíce estava acessando até o 6, porém não haviam declarações até o 6, por isso consegue resolve-lo utilizando o console.log(i) para entender melhor o que estava acontecendo ali.

Por fim, o resultado foi este: https://editor.p5js.org/lucascarrilho26/sketches/uzZ7Ar3DJ

Outra coisa também que foi feita, foi utilizar setas para direita e esquerda e modificar a velocidade de cada um dos inimigos.
