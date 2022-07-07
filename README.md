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

**Memória Cache L1, L2, L3:** São as memórias mais rápidas de um computador, ficam localizadas na CPU e possuem a maior velocidade, porém o menor armazenamento de dados.

**Memória RAM:** Possuem memória de acesso rápidas com um pouco mais de capacidade.

**SSD e HD:** Possuem grandes capacidades de armazenamento, porém a memória de acesso deles é lenta.

**CLOUD:** Possuem atualmente as maiores capacidades de armazenamento, porém a velocidade deles de transferência de dados é a menor de todas.

## PASS BY VALUE X PASS BY REFERENCE

**O que é?** Quando uma função de um código é chamada, , ela pode passar por valor ou referência.

**Pass by Value:** A grosso modo, o valor do parâmetro da função é recebido e "copiado" para outra variável e então a cópia é utilizada. Não há efeitos no valor original

**Pass by Reference:** Neste caso, o valor do endereço de memória é passado para a função, a mesma recebe o valor "original" do parâmetro, portanto, todas as modificações afetam o valor original.


# Resumão do Carrilho  | 05.07.2022

---- PLANO: Iniciante em programação.
---- CURSO: Jogos clássicos parte 1: Pong com Javascript

## Primeiro Projeto com Scratch

Este foi o primeiro projeto feito na minha vida de um joguinho de pong, foi utilizado a ferramenta Scratch para realizar o jogo com sons, modelo de bolinha e raquetes.

Ao realizar o projeto, notei duas coisas interessantes, a primeira delas foi o comportamento mecânico da raquete do oponente. Para solucionar este problema, na parte final, resolvi implementar uma variável como mostra a imagem a seguir, para que ele a cada 0.2 segundos deslize a raquete em uma posição váriavel de acompanhamento da posição y da bolinha entre 30 e -30, criando assim um comportamento mais "natural".

![alt text](C:\Go\src\github.com\karilho\resumaodocarrilho\erro1projetoscratch.png)

A segunda observação, foi em relação aos bugs que estavam ocorrendo, sendo eles o ponto duplo e as vezes a bolinha ficar agarrada tanto encima quanto embaixo, ocasionando problemas de pontuação infinita, confesso que para este problema específicamente não consegui achar uma solução que realmente resolvesse sem criar novos modelos. Então eu resolvi pesquisar e buscar ideias de soluções alternativas e, uma delas que encontrei, foi criar dois novos atores chamados de Borda1 e Borda2 e colocar na função da bolinha que toda vez que fosse contabilizado um ponto, ele devolvesse a bolinha pro centro após 1.5 segundos, resolvendo assim ambos os problemas citados.

![alt text](C:\Go\src\github.com\karilho\resumaodocarrilho\erro2projetoscratch.png)

