### QUESTÃO 1
```mermaid 
flowchart TD


A([inicio]) --> B{{Digite o numeros:}}
B --> C[/n1,n2,n3,n4/]
C --> D[Media=/n1+n2+n3+n4\/4]
D --> E{{Media}}
E --> z([Fim])
```

```

1 AGORITMO Media
2 DECLARE N1,N2,N3,N4,Media : int
3 ESCREVA "Digite quatros numeros: "
4 LEIA N1,N2,N3,N4
5 Media = (N1+N2+N3+N4)/4
6 ESCREVA Media
7 FIM_ALGORITMO

```
### QUESÃO 2
```mermaid
flowchart TD

A([Inicio]) --> B{{Digite a temperatura: }}
B --> C[/Cel/]
C --> D[Fah = 9/5 * Cel + 32]
D --> F{{Esta ,Cel, graus e ,Fah, em Fahrenheit}}
F --> G([Fim])
```

```
1 ALGORITMO CONVERSAO_GRAUS
2 DECLARE Cel, Fah : reais
3 ESCREVA "DIGITE A TEMPERATURA EM CELCIUS: "
4 LEIA Cel
5 Fah = (9/5) * Cel + 32 
6 ESCREVA "ESTA", Cel,"GRAUS E ", Fah,"EM FAHRNHEIT" 
7 FIM_ALGORITMO




```
### QUESTÃO 3
```mermaid
flowchart TD

A([inicio]) --> B{{Digite o dado:}}
B --> C[/Pol/]
C --> D[Mili = Pol * 25,4]
D --> E{{Tem ,Mili, de milimetros de chuva}}
E --> F([Fim])
```

```
1 ALGORITMO CHUVA
2 DECLARE Pol ,Mili : reais
3 ESCREVA "DIGITE AS POLEGADAS: "
4 LEIA Pol
5 Mili = Pol * 25.4
6 ESCREVA "TEM ", Mili, "milimetros de chuva" 
7 FIM_ALGORITMO


```

### QUESTÃO 4
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite o custo de fabrica do carro:}}
B --> C[/Cus_fabri/]
C --> D["Cus_consu = Cus_fabri + (Cus_fabri * 0.12) + (Cus_fabri * 0.45)"]
D --> E{{'O custo do carro foi de ', Cus_consu,  'reais'}}
E --> F([Fim])

```

```
1 ALGORITMO PREÇO_CARRO
2 DECLARE Cus_fabri, Cus_consu : reais
3 ESCREVA: "digite o custo de fabrica do carro: "
4 LEIA Cus_fabri
5 Cus_consu = Cus_fabri + (Cus_fabri * 0,12) + (Cus_fabri * 0,45)
6 ESCREVA "O custo do carro foi ", Cus_consu, " reais" 
7 FIM ALGORITMO

```
### QUESTÃO 5
```mermaid 
flowchart TD
A([inicio]) --> B{{Digite um numero}}
B --> C[/num/]
C --> D{{num ** 2}}
D --> E([fim])
```
```
1 ALGORITMO NUMERO_AO_QUADRADO
2 DECLARE num : real
3 ESCREVA "Digite um numero: "
4 LEIA num
5 ESCREVA"Numero ", num," ao quadrado é ",num ** 2
6 FIM_ALGORITMO
```
### QUESTÃO 6
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite quantos hamburgues foram consumidos}}
B --> C[/Ham/]
C --> D{{Digite quantos chesseburgues foram consumidos}}
D --> E[/Cheese/]
E --> F{{Digite quantas fritas foram consumidas}}
F --> G[/Fritas/]
G --> H{{Digite quantos refrigerantes foram consumidos}}
H --> I[/Refri/]
I --> J{{Digite quantos milkshakes foram consumidos}}
J --> K[/Milk/]
K --> L["total = (Ham * 3) + (Cheese * 2.5) + (Fritas * 2.5) + (Refri * 1.5) + (Milk * 3)"]
L --> M{{O preço da conta foi de, total}}
M --> N([Fim])
```

```
1 ALGORITMO CONTA
2 DECLARE Ham,Cheese,Fritas,Milk,Refri,Total: numericos e reais
3 ESCREVA" Digite quantos hambugues, cheeseburgue, fritas, refri e milkshake foram consumidas"
4 LEIA Ham, Cheese, Fritas, Refri, Milk
5 Total = (Ham * 3) + (Cheese * 2.5) + (Fritas * 2.5) + (Refri * 2.5) + (Milk * 3)
6 ESCREVA "A conta deu ", total, " reais
7 FIM_ALGORITMO

```

### QUESTÃO 7
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite o nome do funcionario, numero de carros vendidos e valor total das vendas}}
B --> C[/Nome,Num_carros,Valor_vendas/]
C --> D["total = 500 + (Num_carros * 50) + (Valor_vendas * 0.05)"] 
D --> E{{Salario do funcionario, Nome, é de ,total, reais}}

```

```
1 ALGORITMO SALARIO
2 DECLARE Nome : STRING
3 DECLARE total, Num_carros, Valor_vendas : numerico
4 ESCREVA "Digite o nome, o numero de carros vendidos e o valor total das vendas"
5 LEIA Nome, Num_carros, Valor_vendas
6 total = 500 + (Num_carros * 50 ) + (Valor_vendas * 0.05)
7 ESCREVA "O salario do funcionario", nome," é de ", total," reais"
8 FIM_ALGORITMO
```

### QUESTÃO 8
```mermaid
flowchart TD
A([inicio]) --> B{{Digite o nome do aluno, a nota da prova e a nota qualitativa}}
B --> C[/Nome, N1,N2/]
C --> D["media = ((N1*2) + N2)/3"]
D --> E{{A media do aluno, Nome, é ,media,}}  

```
```
1 ALGORITMO MEDIA
2 DECLARE Nome : STRING
3 DECLARE Media, N1, N2 : NUMERICO
4 ESCREVA" Digite o nome do aluno, nota da prova e a nota qualitativa"
5 LEIA Nome, N1, N2
6 Media = (N1*2 + N2)/3
7 ESCREVA" A media do aluno ", Nome," foi ", media 
8 FIM_ALGORITMO

```

### QUESTÃO 9
```mermaid 
flowchart TD
A([Inicio]) --> B{{Digite o nome do aluno, email e curso do aluno}}
B --> C[/Nome, Email, Curso/]
C --> D{{Digite a matricula e idade do aluno}}
D --> E[/ Matricula e Idade/]
E --> F{{O nome do aluno é, Nome, a sua matricula é, matricula, o curso que faz é, Curso, sua idade é, Idade, e o email é, Email}}
F --> G([Fim])

```
```
1 ALGORTIMO DADOS_DE_ALUNO
2 DECLARE Nome, Email, Curso: STRING
3 DECLARE Matricula, Idade: NUMERICO
4 ESCREVA "Digite seu nome, curso e email"
5 LEIA Nome, Email, Curso
6 ESCREVA "Digite sua matricula e sua idade"
7 LEIA Matricula, Idade
8 ESCREVA "Os dados do aluno Nome: ", Nome," sua matricula: ", Matricula," seu curso: ", Curso," sua idade: ", Idade," e o emai: ", Email  
9 FIM_ALGORITMO
```
### QUESTÃO 10
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite o raio}}
B --> C[/Raio/]
C --> D[Peri = 2 * 3.14 * Raio]
D --> E[Area = 3.14 * Raio ** 2]
E --> F{{A area é de, Area, e o perimetro é de , Peri}}
F --> G([fim]) 
```

```
1 ALGORITMO RAIO
2 DECLARE Raio, Area, Peri : NUMERICO
3 ESCREVA "Digite o raio "
4 LEIA Raio
5 Area = (Raio ** 2) * 3.14
6 Peri = 2 * 3.14 * Raio
7 ESCREVA "A area é ",Area," e o perimetro é ", Peri
8 FIM_ALGORITMO


```

### QUESTÃO 11
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite um numero: }}
B --> C[/N1/]
C --> D{{O numero ao quadrado é, N1 ** 2, o numero ao cubo é, N1 ** 3, a raiz quadrada do numero é, N1 ** 1/2, a raiz cubica do numero é, N1 ** 1/3,}}
D --> E([Fim])
 
```

```
1 ALGORITMO RAIZ_E_EXPOENTE
2 DECLARE N1
3 ESCREVA "Digite um numero: "
4 LEIA N1 
5 ESCREVA "O numero ao quadrado é ", N1 ** 2, " o numero ao cubo é ", N1 ** 3, " a raiz quadrada do numero é ", N1 ** 1/2, " a raiz cubica do numero é ", N1 ** 1/3
6 FIM_ALGORITMO
 ```
### QUESTÃO 12
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite 3 numeros: }}
B --> C[/N1,N2,N3/]
C --> D{N1 < N2 e N1 < N3}
D -->|sim| E{N2 < N3}
E -->|sim| F{{N1,N2,N3}}
F --> Z([Fim])
E -->|nâo| G{{N1,N3,N2}}
G --> Z
D -->|NÃO| H{N2 < N1 E N2 <N3}
H -->|SIM| I{N1 < N3}
I -->|SIM| J{{N2,N1,N3}}
J --> Z
I -->|NÃO| K{{N2,N3,N1}}
K --> Z
H -->|NÃO| L{N1 < N2}
L -->|SIM| M{{N3,N1,N2}}
M --> Z
L -->|NÃO| N{{N3,N2,N1}}
N --> Z
```

```
1 ALGORITMO ORDENAÇÃO
2 DECLARE N1, N2, N3: NUMERICO
3 ESCREVA "Digite 3 numeros: "
4 LEIA N1, N2, N3
5 SE N1 < N2 E N1 < 3
6 		ENTÃO SE N2 < N3
7 				ENTÃO ESCREVA "N1,N2,N3"
8 			   SENÃO
9 					  ESCREVA "N1,N3,N2"
10 SENÃO SE N2 < N1 E N2 < N3
11 		ENTÃO SE N1 < N3
12 				ENTÃO ESCREVA "N2,N1,N3"
13			  SENÃO 
14               ESCREVA " N2,N3,N1"
15 SENÃO SE N1 < N2
16 	         ENTÃO ESCREVA " N3,N1,N2"
17 		 SENÃO 
18			 ESCREVA "N3,N2,N1"
19 FIM_ALGORITMO		
```
### QUESTÃO 13
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite sua idade}}
B --> C[/Idade/]
C --> D{Idade > 18}
D -->|Sim|E{{Sua categoria é adulto}}
E --> Z([Fim])
D -->|Não|F{Idade < 18 e Idade > 13}
F -->|Sim|G{{Sua categoria é juvenil B}}
G --> Z
F -->|Não|H{Idade < 14 e Idade > 10}
H -->|Sim|I{{Sua categoria é juvenil A}}
I --> Z
H -->|Não| J{Idade < 11 e Idade > 7}
J -->|Sim| K{{Sua categoria e infantil B}}
K --> Z
J -->|Não| L{{Sua categoria é infantil A}}
L --> Z


```

```
1 	ALGORITMO CATEGORIA
2 	DECLARE Idade : numerico
3 	SE Idade > 18
4 		ENTAO ESCREVA "Sua categoria é adulto"
5 	SENAO SE Idade < 18 e > 13
6 			ENTÃO ESCREVA"Sua categoria é juvenil B"
7 	SENAO SE IDADE < 14 e Idade > 10
8 			ENTÃO ESCREVA"Sua categoria é juvenil A"
9 	SENAO SE Idade < 11 E Idade > 7
10 			ENTÃO ESCREVA"Sua categoria é infantil B"
11 	SENAO 
12 			ESCREVA"Sua categoria é infantil A"
13 	FIM_ALGORITMO
```
### QUESTÃO 14
```mermaid
flowchart TD
A([Início])-->B{{"Digite dois números:"}}
B-->C[\n1,n2\]
C-->D{{"Digite o operador (+, -, *, /):"}}
D-->E[\operador\]
E-->F{operador==+}
F--NAO-->G{operador==-}
G--NAO-->H{operador==*}
H--NAO-->I{operador==/}
I-->J{n2 =! 0}
J--NAO-->K{{"divisão por zero"}}
J--SIM-->L[resultado <-- n1 / n2]
F--SIM-->M[resultado <-- n1 + n2]
G--SIM-->N[resultado <-- n1 - n2]
H--SIM-->O[resultado <-- n1 * n2]
L-->P{{resultado}}
M-->P{{resultado}}
N-->P{{resultado}}
O-->P{{resultado}}
P-->Q([Fim])
K-->Q([Fim])
```
### Pseudocódigo
```
	ALGORITMO calculadora_simples
	DECLARE n1, n2, resultado: float
	DECLARE operador, +, -, *, / : operadores
		INICIO
			ESCREVA "Digite dois números e uma operação:"
			LEIA n1, n2, operador
			SE operador ← + ENTAO
				resultado == n1 + n2
			FIM_SE
			SE operador ← - ENTAO
				resultado == n1 - n2
			FIM_SE
			SE operador ← * ENTAO
				resultado == n1 * n2
			FIM_SE
			ENQUANTO operador ← / e n2 = 0 FAÇA
				ESCREVA "ERRO: divisão por zero"
			FIM_ENQUANTO
			SE operador ← / e n2 =! 0 ENTAO
				resultado == n1 / n2
			FIM_SE
			LEIA resultado
			ESCREVA resultado
		FIM
```
