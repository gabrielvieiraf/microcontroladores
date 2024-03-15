# Aritmética Binária e Hexadecimal

Assim como na base decimal, na base hexa e binaria nós também precisamos fazer algumas continhas:

## Adição binária e hexadecimal
**Na adição binária**, começamos pelo dígito mais à direita (bit menos significativo) e movemos para a esquerda, assim como na adição decimal. As regras são as seguintes:

- 0 + 0 resulta em 0, sem transporte.
- 0 + 1 ou 1 + 0 resulta em 1, sem transporte.
- 1 + 1 resulta em 0, com um transporte de 1 para o próximo dígito mais significativo.

Exemplos:

Decimal:

$1 + 2 = 3$

$0001 + 0010 = 0011$   

Decimal:

$7     +  13  = 28$

binário:

$0111 + 1101 = 10100$


**A adição hexadecimal** funciona de maneira semelhante, mas em vez de dois dígitos (0 e 1), temos dezesseis dígitos (0-9 e A-F). Se a soma de dois dígitos for 16 ou mais, subtraímos 16 do resultado e levamos 1 para o próximo dígito mais significativo.

Por exemplo, se tivermos que adicionar 9 e A, a soma seria 19 em decimal, mas em hexadecimal, subtraímos 16 para obter 3 e levamos 1 para o próximo dígito. Portanto, 9 (hexadecimal) + A (hexadecimal) = 13 (decimal) ou 3 (hexadecimal) com um transporte de 1.

Exemplos:


Decimal:

$10 + 1 = 11$

Hexadecimal:

$A + 1 = B$


Decimal:
$175+255 = 430$


Hexadecimal:
$AF + FF = 1AE$

Obs:
>Adição é a parte mais suave da aritmética digital, então foca em fazer esses calculos ou pelomenos entendê-los perfeitamente antes de seguir.
