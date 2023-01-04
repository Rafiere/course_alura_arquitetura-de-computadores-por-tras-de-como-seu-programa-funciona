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

# Aula 04 - Como a memória funciona:

# Aula 05 - Como os dados são armazenados:
