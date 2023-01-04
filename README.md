# Aula 01 - Como o computador lê o seu código:

Quando escrevemos um código, normalmente utilizamos uma linguagem de alto nível. Uma linguagem de alto nível é uma linguagem que o ser humano possui uma maior facilidade de entender.

O computador não entende as linguagens de alto nível, assim, ele entende apenas o código de máquina, que é uma linguagem muito restrita e que consegue fazer algumas poucas operações, como somar, guardar e comparar valores.

O Assembly, normalmente, é considerado como uma linguagem de baixo nível.

O computador utiliza apenas o código binário, que é composto por "0" e "1".

A sequência é a seguinte:

Código-Fonte -> Tradutor -> Código de Máquina

O tradutor do computador serve para ler o código-fonte e traduzir o código-fonte em um código de máquina.

Um código-fonte pode ser traduzido em um código de máquina de duas principais formas, são elas:

Código-fonte -> Código de máquina -> Executar (Linguagens Compiladas)

Código-fonte -> Traduz uma parte do código -> Executa -> Repete o processo (Linguagens Interpretadas)

Uma linguagem compilada, normalmente, é muito mais rápida do que uma linguagem interpretada.

Exemplos de Linguagens Compiladas: C, Rust, Go
Exemplos de Linguagens Interpretadas: JavaScript, Python, PHP, Ruby

Exemplos de Linguagens Híbridas:

O JIT (Just in Time) Compilation consiste realizarmos a compilação na hora certa, só compilando as funções que estão sendo executadas. A V8 da Google e o NodeJS utiliza o JIT, por exemplo. Dessa forma, conseguimos compilar e interpretar o código na hora certa.

O Java é uma linguagem compilada e interpretada. Ela funciona da seguinte forma:

Código-fonte -> Compilador -> Bytecode (.class) -> Interpretador (JVM) -> Execução

# Aula 02 - Como o computador executa um programa:

Uma memória não volátil é uma memória que guarda a informação mesmo se perdermos a energia. Alguns tipos de memórias não voláteis são o HD (Hard Disk) e o SSD, que é formado por chips eletrônicos.

A memória RAM guarda os dados que estamos trabalhando no momento. Quanto mais memória RAM, conseguimos, por exemplo, abrir várias abas de um jogo ao mesmo tempo.

Quando o computador é desligado, os dados da RAM são apagados.

Uma memória RAM é uma tabela com bytes, onde cada índice armazena um byte.

O termo "RAM" significa "Random Access Memory", assim, não importa o endereço que a informação for escrita, levaremos sempre o mesmo tempo para acessá-lo.

O processador, ou CPU, é responsável por receber as instruções da memória RAM e executá-las. Ela é dividida em algumas partes:

Unidade de Controle (UC): Receberá os dados da memória RAM e tenta entender o que a instrução significa, enviando o significado dessas instruções para a ULA.

Unidade Lógico Aritmética (ULA): Realiza as operações de soma, multiplicação, comparação e operações lógicas.

Registradores: É um conjunto de posições que conseguimos armazenar valores intermediários para as operações. Ele é responsável pela memória do processador. Ele armazena as instruções atuais, as posições da instrução atual, os valores intermediários e etc. Ele recebe os dados da ULA. Ele é uma memória rápida, mas pequena.

Sequências de Instruções do Processador:

Busca: O processador buscará as instruções que ele deve executar na memória RAM e guarda essa instrução nos registradores.

Decodificar: A instrução é enviada para a Unidade de Controle e ela configura o processador para realizar essa instrução.

Executar: O processador executa a instrução.

O "clock", do processador, é como um "metrônomo". Ele cria um "ritmo" para as ações. A cada "tic" do metrônomo, uma ação é executada no processador, ou seja, a cada "tic", ele busca, decodifica ou executa uma ação.

Um processador possui, em média, 3 bilhões de "tics" por segundo.

## Memória na Prática:

Temos dois programas escritos em JavaScript.

O primeiro programa lê todas as linhas da tabela de uma vez só e executa depois uma ação.

Esse primeiro programa, se ele for ler uma tabela muito grande e puxar ela inteira para a memória, o JavaScript poderá dar um erro de estouro de memória, pois toda a tabela deverá ser armazenada na memória RAM.

O segundo programa lê uma linha da tabela e executa uma ação para cada linha.

Esse programa não correrá o risco de travar igual o primeiro programa, pois a memória RAM não ficará sobrecarregada, pois todos os dados da tabela não serão puxados de uma vez só para a memória RAM do servidor.

# Aula 03 - Como o computador executa vários programas:

Durante muitos anos, apenas a velocidade do clock diferenciava a velocidade dos processadores, assim, quanto mais rápido o clock, mais rápido o processador seria.

Nos processadores modernos, adicionamos mais núcleos aos processadores, assim, quanto mais núcleos, mais "braços" o processador vai ter, e ele vai ser capaz de executar uma maior quantidade de operações, como a busca, a decodificação e a execução ao mesmo tempo.

Os dispositivos de entrada e de saída são utilizados para enviarmos inputs (entrada) e recebermos um output do coputador (saída).

Os drivers são utilizados para abstrairmos várias particularidades dos dispositivos de entrada e saída, assim, não importa a implementação de um teclado, por exemplo, através do driver, que é uma camada de compatibilidade, o teclado conseguirá se comunicar com o computador.

## Monitor:

A imagem de um monitor é representada por pixels. Cada pixel pode ter três cores, que são o "vermelho", o "verde" e o "azul". Os pixels, normalmente, são atualizados da esquerda para a direita.

A placa de vídeo possui o objetivo de atualizar rapidamente os pixels na tela, assim, elas são otimizadas para realizar esses cálculos de atualização de pixels com um maior desempenho.

## Teclado:

Quando apertamos uma tecla, emitimos um sinal para o computador que uma determinada tecla foi executada. Ele envia apenas a posição do caractere que foi executada.

## Execução de Várias Tarefas ao Mesmo Tempo:

O computador executa dezenas de programas ao mesmo tempo, assim, para o computador conseguir executar música e mexer o mouse simultaneamente, ele move um pouquinho o mouse e toca um pouco de música, e, como essas operações são executadas muito rapidamente, ele executa um pouquinho para cada programa.

Cada programa deverá ser executado por um determinado tempo, assim, o SO cria uma fila, e, nessa fila, cada programa é executado durante o tempo que está definido na fila. A prioridade do mouse, por exemplo, é maior do que a de outros programas, por isso que ele precisa ser executado muito rapidamente.

# Aula 04 - Como a memória funciona:

## Cache:

A memória DRAM é uma memória RAM mais barata, mas também mais lenta. A memória SRAM é muito mais rápida do que a DRAM, mas ela é mais cara.

O processador possui uma memória SRAM, assim, ela armazena os dados que estão sendo mais utilizados no momento, assim, ao invés do processador buscar um dado na memória RAM, ele colocará esse dado que está sendo mais utilizado na memória cache.

Existem vários níveis de cache.

O cache L1 é muito colado na CPU, e o cache L2 é um pouco maior do que o L1, e ele está colado no L2. Cada core possui um cache L1 e L2. O cache L3 é um cache que é muito maior e um pouco mais lento, mas ele é compartilhado por todos os cores da CPU.

## Hierarquia de Memória:

Abaixo, temos o nome, a velocidade e a quantidade de armazenamento de cada memória.

1. Registrador - 1 Ciclo de Clock ~ 500 Bytes
2. Cache L1 - 700GB/s - 64 KB
3. Cache L2 - 200GB/s - 500 KB
4. Cache L3 - 150GB/s - 4 MB
5. RAM - 10GB/s - 8 GB
6. SSD - 2GB/s - 500GB
7. HD - 200MB/s - 4 TB
8. Cloud - 2MB/s - PB ou EB

## Princípio da Localidade:

A localidade temporal consiste em sempre utilizarmos a mesma porção da memória.

A localidade espacial significa que, se estamos acessando um dado em um local, provavelmente acessaremos o vizinho dessa instrução de forma posterior.

Isso ocorre pois os programas, na maioria das vezes, são escritos de forma sequencial.

## Processador 32 ou 64 bits:

É o tamanho de informação que pode ser processada pela CPU em um ciclo de clock. Um processador de 64 bits possui mais performance, pois ele processa muitos dados de uma vez. Um processador de 64 bits também possui uma maior quantidade de memória. Um processador de 32 bits consegue representar apenas valores de 2^32, ou seja, não conseguimos representar mais do que 4GB de memória RAM. Um processador de 64 bits, pelo contrário, consegue suportar mais ou menos 16 bilhões de GB de RAM.

Um Windows de 32 bits deverá enviar instruções de 32 bits. Um processador de 64 bits consegue suportar instruções de 32 bits, mas ele funcionará de forma mais otimizada com um computador de 64 bits.

# Aula 05 - Como os dados são armazenados:

Quando executamos um código, os valores são armazenados na memória.

Os caracteres são armazenados de acordo com valores, e esses valores são armazenados na memória.

O ASCII é um padrão que codifica os caracteres utilizando 7 bits.

O Unicode trata de letras, caracteres, e os símbolos respectivos dele. Ele é uma evolução do ASCII, com suporte a um maior número de caracteres.

O UTF-8 não possui um número fixo de bytes para cada caractere, assim, cada caractere tem um determinado tamanho. Cerca de 95% da web utiliza o UTF-8.

Um ponteiro é um valor que aponta para outro valor na memória.

A passagem por referência consiste em copiarmos o endereço de memória de uma lista, assim, duas variáveis poderão apontar pro mesmo endereço da memória.

A passagem por valor consiste em copiarmos o valor de uma lista e atribuirmos para outra lista, sendo que essa outra lista estará em outro endereço de memória.
