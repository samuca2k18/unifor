# UNIFOR
**Disciplina:** Raciocínio Logico Algorítmico
**Orientador:** Ricardo
## Lista de exercícios

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
