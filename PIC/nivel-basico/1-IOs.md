# Desvendando TRIS, LAT e PORT: Um Guia Técnico para Entradas e Saídas do PIC


Introdução:

Os microcontroladores PIC oferecem recursos poderosos de entrada e saída (I/O) que permitem interagir com o mundo exterior. Para controlar dispositivos externos e ler informações do ambiente, é essencial entender os conceitos de TRIS, LAT e PORT. Este guia detalhado irá desvendar esses segredos e equipá-lo com as ferramentas para dominar as entradas e saídas do PIC.

1. TRIS: Definindo a Direção do Fluxo de Dados

O registrador TRIS (TRISter) controla a direção do fluxo de dados em cada pino do PIC. Ele pode ser configurado em dois estados:

Entrada (1): O pino se torna uma entrada, permitindo que sinais externos sejam lidos pelo microcontrolador.
Saída (0): O pino se torna uma saída, permitindo que o microcontrolador envie sinais para dispositivos externos.
A configuração do TRIS é realizada através de bits individuais, onde cada bit corresponde a um pino específico. Definindo um bit como '1', o pino se torna uma entrada. Definindo como '0', o pino se torna uma saída.

2. LAT: Armazenando o Valor de Saída Atual

O registrador LAT (LATCH) armazena o valor que está sendo aplicado na saída de cada pino. Mesmo que o valor do TRIS seja alterado, o valor no LAT é preservado. Isso garante que a saída do pino permaneça consistente, mesmo durante transições entre entrada e saída.

Ao escrever um valor no LAT, o valor correspondente é aplicado na saída do pino. Por exemplo, escrevendo '1' no LAT de um pino configurado como saída, o pino assume um nível lógico alto (5V).

3. PORT: Lendo o Estado Atual do Pinos

O registrador PORT (PORTA) permite ler o estado atual do nível lógico em cada pino, independente de sua configuração como entrada ou saída. O valor do PORT reflete o estado real do pino, independentemente do valor armazenado no LAT.

Lendo o valor de um bit no PORT, obtemos o nível lógico atual do pino correspondente. Se o bit for '1', o pino está em nível alto (5V). Se o bit for '0', o pino está em nível baixo (0V).

4. Leitura Digital: Obteção do Nível Lógico de Entrada

A leitura digital consiste em obter o nível lógico atual de um pino configurado como entrada. Essa operação é realizada através da função read_pin(pino), que retorna um valor booleano:

True se o pino estiver em nível alto (5V)
False se o pino estiver em nível baixo (0V)
A função read_pin() utiliza o valor do PORT para determinar o nível lógico do pino especificado.

5. Escrita Digital: Definindo o Nível Lógico de Saída

A escrita digital consiste em definir o nível lógico que será aplicado na saída de um pino configurado como saída. Essa operação é realizada através das funções output_high(pino) e output_low(pino), que definem o pino como nível alto (5V) ou baixo (0V), respectivamente.

As funções output_high() e output_low() modificam o valor do LAT no pino especificado, alterando assim o nível lógico da sua saída.

6. Conjuntos de I/O: Agrupando Pinos para Manipulação Simultanea

Os microcontroladores PIC organizam seus pinos em conjuntos de I/O chamados portas, como PORTA, PORTB, PORTC e assim por diante. Cada porta possui um conjunto de bits (pinos) que podem ser configurados e manipulados individualmente ou em conjunto.

A utilização de portas facilita a manipulação simultânea de grupos de pinos, simplificando o código e otimizando o desempenho.

7. Recapitulando os Conceitos Chave

TRIS: Define a direção do fluxo de dados em cada pino (entrada ou saída).
LAT: Armazena o valor que está sendo aplicado na saída de cada pino.
PORT: Permite ler o estado atual do nível lógico em cada pino.
Leitura Digital: Obtém o nível lógico atual de um pino configurado como entrada.
Escrita Digital: Define o nível lógico que será aplicado na saída de um pino configurado como saída.
Conjuntos de I/O: Agrupam pinos em portas para manipulação simultânea.
