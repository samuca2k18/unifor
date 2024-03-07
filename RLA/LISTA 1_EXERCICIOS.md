# UNIFOR
**Disciplina:** Raciocínio Logico Algorítmico
**Orientador:** Ricardo
## Lista de exercícios
### Questão 1
```mermaid
flowchart TD

A([Inicio]) --> B{{As notas:}}
B --> C[/Nota1,Nota2/]
C --> D{/Nota1+Nota2\ /2 >= 7}	
D --> |Não| E{{aluno reprovado}}
E --> Z([Fim])
D --> |Sim| F{{aluno aprovado}}
F --> Z

```

```
1 Algoritmo Aprovado_Reprovado
2 Declare nota1, nota 2, numerico
3 ESCREVA "digite as notas"
4 Leia nota1, nota2
5 SE (nota1+nota2)/2 >= 7
6 	ENTÃO ESCREVA "aluno aprovado"
7 SENÂO
8 	ESCREVA "aluno reprovado"
```


### Questão 2
```mermaid
flowchart TD

A([Inicio]) --> B{{Digite seu salario}}
B --> C[/Salario/]
C --> D{Salario < 501}	
D --> |Sim| E[Salario = Salario * 1,2]
D --> |Não| F[Salario = Salario * 1,1]
E --> G{{Seu salario novo é, Salario}}
G --> H([Fim])
F --> G


```

```
1 Algoritmo Novo_Salario
2 Declare salario, numerico
3 ESCREVA "digite seu salario: "
4 Leia salario
5 SE salario < 501
6 	ENTÂO salario = salario * 1,2
7 SENÂO
8 	salario = salario * 1,1
9 ESCREVA "Seu novo salario é", salario

```

### Questão 3
Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um numero é par ou impar -- numero inteiro e positivo par ou impar--

### FLUXOGRAMA
```mermaid
flowchart TD
A([Inicio]) --> B{{Digite um numero:}}
B --> C[/Num/]
C --> D{numero >= 0}	
D --> |Não| E{{O numero deve ser positivo}}
E --> Z([Fim])
D -->|Sim| F[Num = Num % 2]
F --> G{Se Num == 0} 
G --> |Não| H{{O numero é impar}}
G --> |Sim| I{{O numero é par}}
H --> Z
I --> Z

```

```
1	ALGORITIMO verificar_par_impar
2	DECLARE Num, resto numerico
3	ESCREVA "Digite um numero: "
4	Leia Num
5		SE numero > 0 ENTÃO
6		resto = num % 2
7		SE resto == 0 
8			ESCREVA "numero par"
9		SENAO
10			ESCREVA "numero impar"
11	SENÂO 
12		ESCREVA "numero deve ser positivo"
13	FIM_ALGORITMO

```

### Questão 4

```mermaid
flowchart TD

A([Inicio]) --> B{{Digite sua idade}}
B --> C[/Idade/]
C --> D{Idade < 18}	
D --> |Não| E{{Você não pode tirar CNH faltam, 18 - Idade, anos }}
D --> |Sim| F{{Você pode tirar CNH}}
E --> G([Fim])
F --> G


```

```
1 Algoritmo CNH
2 Declare Idade, numerico
3 ESCREVA "digite sua idade: "
4 Leia idade
5 SE idade < 18
6 	ENTÂO Escreva "Voce não pode tirar CNH falta", 18 - idade, "anos"
7 SENÂO
8 	Escreva "Voce pode tirar CNH"





```
