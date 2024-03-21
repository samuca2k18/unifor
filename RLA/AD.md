## Lista de questões

### Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis, $a$ e $b$, implemente e teste um algoritmo para trocar os valores atribuídos a elas.
#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[A = 10]
B --> C[B = 8]
C --> D[C = A]
D --> E[A = B]
E --> F[B = C]
F --> G{{ESCREVA, A, B}}
G --> Z([FIM])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo TrocaValores
DECLARE A, B, C: REAIS
ESCREVA A, B
A = 10
B = 8
C = A
A = B
B = C
ESCREVA A, B
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)


| a  | b  | aux | a  | b  | saída 1 | saída 2 | 
| -- | -- | --  | -- | -- | --      | --      | 
| 0  | 1  | 0   | 1  | 0  | a = 1   | b = 0   |
### Questão 2 - Contagem (1 ponto)

Dado um conjunto $n$ de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem $cont$ do número de alunos que foram aprovados no exame. 
Será considerado aprovado o aluno que tirar $nota$ 50 ou maior (no intervalo de 0 a 100).

#### Fluxograma (0.25 ponto)

```mermaid 
flowchart TD
A([INICIO]) --> B{{ESCREVA O NUMERO DE NOTAS}}
B --> C[/N/]
C --> D[I = 0]
D --> E{SE I != N}
E -->|SIM| F{{ESCREVA NOTA DO ALUNO}}
F --> G[/Nota/]
G --> H{SE Nota >= 50}
H -->|SIM| I[Cont =+ 1]
I --> J[I =+ 1]
J --> E
H -->|NÃO| K[I =+ 1]
K --> E
E -->|NÃO| L{{O NUMERO DE ALUNOS APROVADOS FOI, Cont}}
L --> M([FIM])
```


#### Pseudocódigo (0.5 ponto)

```
ALGORITMO ALUNOS_APROVADOS
DECLARE N, I, Cont, Nota : NUMERICO INTEIRO
INCIO
ESCREVA "DIGITE NUMERO DE NOTAS: "
LEIA N
I = 0
Cont = 0
ENQUANTO I != N FAÇA
	ESCREVA "DIGITE NOTA DO ALUNO"
	LEIA Nota
	SE NOTA >= 50
		Cont =+ 1
		I =+ 1
	SENÃO
		I =+ 1
FIM_ENQUANTO
ESCREVA "NUMERO DE ALUNOS APROVADO FOI ", Cont
FIM_ALGORITMO 

```


#### Teste de mesa (0.25 ponto)

| it | n  | i  | cont | i<=n  | nota, i | nota | nota_valida | cont+1 | i+1 | saída        | 
| -- | -- | -- | --   | --    | --      | --   | --          | --     | --  | --           |
| 1  | 3  | 1  |  0   | True  | nota 1  | 60   | True        | 1      | 2   |              |
| 2  | 3  | 2  |  1   | True  | nota 2  | 40   | False       | 1      | 3   |              |
| 3  | 3  | 3  |  1   | True  | nota 3  | 90   | True        | 2      | 4   |              |
| 4  | 3  | 4  |  2   | False |         |      |             |        |     | Aprovados: 2 |
### Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de $n$ números, implemente e teste um algoritmo para calcular a soma desses números. <br>
Aceite apenas $n$ maior ou igual a zero.

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{ESCREVA NUMERO TOTAL DE NUMEROS}}
B --> C[/N/]
C --> D[I = 0]
D --> E{SE I != N }
E -->|SIM| F{{ESCREVA UM NUMERO}}
F --> G[/Num/]
G --> H{SE Num >= 0}
H -->|SIM| I[soma =+ Num]
I --> J[I =+ 1]
J --> E
H -->|NÃO| E
E -->|NÃO| K{{A SOMA TOTAL DOS NUMEROS É, soma}}
K --> Z([FIM])

```

#### Pseudocódigo (0.5 ponto)

```
ALGORITMO SOMA_TOTAL
DECLARE I, N, soma, Num: NUMERICO
INICIO
ESCREVA "DIGITE QUANTOS NUMERO SERA: "
LEIA N
I = 0
soma = 0
ENQUANTO I != N FAÇA
	ESCREVA "DIGITE UM NUMERO"
	LEIA Num
	SE Num >= 0
		soma =+ Num
		I =+ 1
FIM_ENQUANTO
ESCREVA "A SOMA TOTAL DOS NUMEROS É", soma
FIM_ALGORITMO

```

#### Teste de mesa (0.25 ponto)

| it | n  | n >= 0 | soma | i  | i <= n | num | soma =+ num  | saída                   |
| -- | -- | --     | --   | -- | --     | --  | --           | --                      |
|    | -3 | False  |      |    |        |     |              | O valor deve ser ...    |
| 1  | 0  | True   | 0    | 1  | False  |     |              | A soma dos números é 0  |
| 1  | 3  | True   | 0    | 1  | True   | 5   | 0 + 5 = 5    |                         |
| 2  | 3  | True   | 5    | 2  | True   | 10  | 5 + 10 = 15  |                         |
| 3  | 3  | True   | 15   | 3  | True   | 20  | 15 + 20 = 35 |                         |
| 4  | 3  | True   | 35   | 4  | False  |     |              | A soma dos números é 35 |


### Questão 4 - Cálculo de uma série (1 ponto)

Dado um conjunto de $n$ termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

$$ S = \frac{1}{2} + \frac{3}{4} + \frac{5}{6} + \frac{7}{8} + \dots $$

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{ESCREVA O NUMERO DE TERMOS}}
B --> C[/N/]
C --> D[I = 0]
D --> E{SE I != N}
E -->|SIM| F["soma = (1 + I * 2)/(2 + I * 2)"]
F --> G[S =+ soma]
G --> H[I =+ 1]
H --> E
E -->|NÃO| I{{SOMA TOTAL DOS ELEMENTOS É, S}}
I --> Z([FIM])
```


#### Pseudocódigo (0.5 ponto)

```
ALGORITMO SOMA_DE_N_ELEMENTOS
DECLARE I, N, soma, S: NUMERICO INTEIRO
INCIO
ESCREVA" Digite quantos termos serâo: "
LEIA N
I = 0
soma = 1/2
ENQUANTO I != N FAÇA
	soma = (1 + I * 2)/(2 + I * 2)
	S =+ soma
	I =+ 1
FIM_ENQUANTO
ESCREVA "SOMA TOTAL DOS ELEMENTOS É ", S
FIM_ALGORITMO

```

#### Teste de mesa (0.25 ponto)

| it | n  | S  | i | numerador | denominador | termo | S += termo     | saída                  |
| -- | -- | -- |-- | --        | --          | --    | --             | --                     |
|    | 0  | 0  |   |           |             |       |                |                        |
| 1  | 4  | 0  | 0 | 2*0+1 = 1 | 2*0+2 = 2   | 1/2   | 0+1/2 = 1/2    |                        |
| 2  | 4  | 0  | 1 | 2*1+1 = 1 | 2*1+2 = 2   | 3/4   | 1/2+3/4 = 1.25 |                        |
| 3  | 4  | 0  | 2 | 2*2+1 = 1 | 2*2+2 = 2   | 5/6   | 0+1/2 = 2.08   |                        |
| 4  | 4  | 0  | 3 | 2*3+1 = 1 | 2*3+2 = 2   | 7/8   | 0+1/2 = 2.96   | Soma da série S é 2.96 |


### Questão 5 - Cálculo fatorial (2 pontos)

Dado um número $n$, implemente e teste um algoritmo para calcular o fatorial de $n$ (escrito como $n!$), onde $n ≥ 0$.

#### Fluxograma (0.5 ponto)


```mermaid 
flowchart TD
A([INICIO]) --> B{{ESCREVA QUAL NUMERO SERA FATORIAL: }}
B --> C[/N/]
C --> D[I = 0]
D --> E{SE N >= 0}
E -->|NÃO| B
E -->|SIM| F{SE I != N}
 F -->|SIM| G[total *= I]
 G --> H[I += 1]
 H --> F
 F -->|NÃO| I{{O TOTAL DEU, total}}
 I --> Z([FIM])

```
#### Pseudocódigo (1.0 ponto)

```
ALGORITMO NUMERO_FATORIAL
DECLARE N, I, TOTAL: NUMERICO INTEIRO
INCIO
I = 0
REPITA
	ESCREVA "ESCOLHA UM NUMERO POSITIVO: "
	LEIA N
ATE_QUE N >= 0
ENQUANTO I != 0 FAÇA
	TOTAL *= I
	I += 1
FIM_ENQUANTO
ESCREVA "TOTAL DEU ", TOTAL
FIM_ALGORITMO
```
#### Teste de mesa (0.5 ponto)
| n  | fator | i  | fator = fator * i | saída               |
| -- | --    | -- | --                | --                  |
| 3  | 1     | 1  | 1*1 = 1           |                     |
| 3  | 1     | 2  | 1*2 = 2           |                     |
| 3  | 2     | 3  | 2*3 = 6           | O fatorial de 3 é 6 |


### Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os $n$ primeiros termos da sequência de Fibonacci, onde $n ≥ 1$. <br>
Os primeiros termos são: $0, 1, 1, 2, 3, 5, 8, 13, \dots$ <br>
Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.

#### Fluxograma (0.5 ponto)


```mermaid
flowchart TD
A([INICIO]) --> B{{ESCREVA TOTAL DE SEQUENCIA:}}
B --> C[/N/]
C --> D[I = 0]
D --> E[soma = 0]
E --> F[num_anterior = 0]
F --> Z{{num_anterior}}
Z --> G[num_atual = 1]
G --> H{SE I != N}
H -->|SIM| I[soma = num_atual + num_anterior]
I --> J[num_anterior = num_atual]
J --> K[num_atual = soma]
K --> L[I += 1]
L --> M{{ESCREVA,soma}}
M --> H
H -->|NÃO| N([FIM])  

```

#### Pseudocódigo (1.0 ponto)

```
ALGORITMO_FIBONACCI
DECLARE I, N, num_anterior, num_atual, soma: numerico inteiro
INICIO
ESCREVA "digite o numero de termos: "
LEIA N
num_anterior = 0
num_atual = 1
i = 0
ESCREVA num_anterior
ENQUANTO I != N FAÇA
	soma = num_atual + num_anterior
	num_anterior = num_atual
	num_atual = soma
	i += 1
	ESCREVA soma
FIM_ENQUANTO
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| it | n  | a  | b  | i  | saída | termo_atual = a + b | a = b | b = termo_atual |
| -- | -- | -- | -- | -- | --    | --                  | --    | --              |
| 1  | 5  | 0  | 1  | 1  | 0     | 0 + 1 = 1           | 1     | 1               |
| 2  | 5  | 1  | 1  | 2  | 1     | 1 + 1 = 2           | 1     | 2               |
| 3  | 5  | 1  | 2  | 3  | 1     | 1 + 2 = 3           | 2     | 3               |
| 4  | 5  | 2  | 3  | 4  | 2     | 2 + 3 = 5           | 3     | 5               |
| 4  | 5  | 3  | 5  | 5  | 3     | 3 + 5 = 8           | 5     | 8               |
### Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Implemente e teste um algoritmo para inverter a ordem dos dígitos de um número inteiro positivo de dois dígitos.

#### Fluxograma (0.5 ponto)


```mermaid
flowchart TD
A([INICIO]) --> B{{ESCREVA UM NUMERO COM 2 DIGITOS:}}
B --> C[/N/]
C --> D{N >= 10 E N < 100}
D -->|NÃO|B
D -->|SIM| E[ultimo_digito = N % 10]
E --> F["num_invertido = (ultimo_digito * 10) + (N // 10)"]
F --> G{{O NUMERO INVERTIDO É, num_invertido}}
G --> Z([FIM])
```


#### Pseudocódigo (1.0 ponto)

```
ALGORITMO_INVERSÃO_DE_NUMERO
DECLARE N, ultimo_digito, num_invertido: numerico inteiro
INICIO
REPITA
	ESCREVA "DIGITE UM NUMERO COM 2 DIGITOS: "
	LEIA N
ATE_QUE N >= 10 E N < 100
ultimo_digito = N % 10
num_invertido = (ultimo digito * 10) + (N // 10)
ESCREVA "O NUMERO INVERTIDO DE ", N, "É ",num_invertido
FIM_ALGORITMO
```
#### Teste de mesa (0.5 ponto)

| it | num | num_inv | num > 0 | digito | num = num // 10 | num_inv = (num_inv * 10) + digito | Saída                       |
| -- | --  | --      | --     | --      | --              | --                                | --                          |
|    | -1  | 0       | False  |         |                 |                                   | O número deve ser positivo! |
| 1  | 0   | 0       | False  |         |                 |                                   | Número invertido:: 0        |
| 1  | 42  | 0       | True   | 2       | 4               | 2                                 |                             |
| 2  | 4   | 2       | True   | 4       | 0               | 24                                |                             |
| 3  | 0   | 24      | False  |         |                 |                                   | Número invertido:: 24       |
