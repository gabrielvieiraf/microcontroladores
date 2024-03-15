# Números Binários

Qualquer programador de verdade sabe o que são as bagaças dos números binários. Não preciso introduzir o conceito básico de `0 = desligado` e `1 = ligado`. E se você não sabe, sai desse repositório, que embarcado não é pra você. 

 Quando unitário os números binários são chamados de bit. A parada que muitos **animais** não sabem é que podemos usar um conjunto de bits para representar outras paradas que fujam da **lógica tosca** de apenas ligado e desligado.

Por exemplo, na tabela abaixo temos níveis de inteligência e suas encodificações para lógica digital:

| valor  | Encodificação A |  Encodificação B | Encodificação C  | 
|---|---|---|---|
|inteligente| 00  |00   |0001   |   
|medíocre| 01  |10   |0010   |   
|burro| 10  |11   |0100   |  
|dev frontend| 11  | 01   |1000   |    

Para encodificar as paradas, nós temos que saber quantos cenários temos, que nesse caso são 4. Para saber o número mínimo de bits para transformar a lógica da sua caixola para essa carroça que você chama de computrador, temos que fazer uma conta matemática, que é a seguinte:

$ceil(\log_2 n)$

Essa conta ridícula deve ter te assustado, uma vez que vivemos numa geração que não pensa sem um chat GPT do lado. Mas aqui no meu repositório, você vai pensar na base do ódio.

A função representada por `ceil` é basicamente um arredondamento pra cima da parada pq o log pode vir com numero quebrado, e não em como tu fazer 4,1 cenários por exemplo. Leia essa parte até entender essa bagaça, se não entender, pede pro teu chatgpt explicar isso como se estivesse explicando pra um neandertal.

Seguimos e beleza, o `ceil` é apenas pra arredondar. Agora nós temos a parte do log. `n` bascamente é o número de cenários que nós temos para encodificar para a lógica digital, que se você tem dois neurônios na sua cabeça, deve lembrar que a tabela acima tem `4 cenários`. Logo, nossa conta para **o número mínimo de bits necessários para representar nosso cenário** será: 


$ceil(\log_2 4)$

Se você sabe calcular ou sabe operar uma calculadora, deve ter visto que o resultado é `2`.

# Outras bases numéricas
Se você não é um imbecil, deve ter percebido que a base binária é baseada em `2` algarismos, `0` e `1`. Nós normalmente utilizamos a base **decimal** em nosso dia a dia, que é baseada em `10` algarismos. Além dessas duas óbvias, nós temos outras, mas a que será útil por aqui é a hexadecimal, baseada em `16` algarismos. 

Através da matemática conseguimos converter de uma base para a outra, por incrível que pareça o mundo da computação funciona e é lógico. Não sou professorzinho de faculdade pra ficar me aprofundando em conversão de um pra outro, então fica com um exemplo simples ai que ja ta bom demais:


| Decimal  | Binário |  binário para decimal | Hexadecimal  | Hexadecimal para decimal | 
|---|---|---|---|---|
|0| 00  |$0*2^1 + 0*2^0$  |0   |   $0*16^0$
|1| 01  |$0*2^1 + 1*2^0$   |1   |   $1*16^0$
|2| 10  |$1*2^1 + 0*2^0$   |2   |  $2*16^0$
|3| 11  | $1*2^1 + 1*2^0$   |3   |  $3*16^0$


A parada do hexadecimal é que além dos `10` algarismos numéricos, nós temos mais `6` algarismos alfabéticos. Eu fiquei com preguiça de digitar a tabela toda nesse markdown, mas basicamente o hexadecimal vai do `0` ao `F`, como visto abaixo:

`0 1 2 3 4 5 6 7 8 9 A B C D E F`

 > **SE NÃO ENTENDEU ESSA BAGAÇA, VAI ESTUDAR MAIS UM POUCO ANTES DE SEGUIR, POR QUE ISSO É O BÁSICO DO BÁSICO DAQUI PRA FRENTE**



 # Bytes

 Um número binário de $n$ bits pode representar os valores decimais sem sinal de 0 a $2^{(n-1)}$. Um número comum
o tamanho dos dados binários é um grupo de oito bits, o famoso **byte**.

Um byte pode representar o intervalo entre de 0 a 255 (0x00 a 0xFF em hexadecimal). Grupos de bytes são muito utilizados para representar numeros maiores.

> **MOMENTO NERDOLA**
    Potências de dois que são divisíveis por 210 podem ser referidas pelos sufixos Ki (kibi, kilobina ry, 210), Mi (mebi, megabinário, 220) e Gi (gibi, gigabinário, 230). A notação de Ki, Mi e Gi é adotado do padrão IEEE 1541-2002, que foi criado para evitar confusão com os sufixos:


- **k (quilo, 103)**
- **M (mega, 106)**
- **G (giga, 109)**.


>    Assim, o valor de 4.096 pode ser escrito na forma abreviada de 4 Ki (4 * 1 Ki = 22 * 210 = 212 = 4096 = 4,096 k). No entanto, esteja ciente de que a ter minologia deste padrão IEEE ainda não é amplamente utilizada. Os termos kBytes e MBytes são
    comumente usado quando se refere a tamanhos de memória e significa o mesmo que KiBytes e MiBytes
