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

```mermaid
flowchart TD
A([Inicio]) --> B{{Digite o custo de fabrica do carro:}}
B --> C[/Cus_fabri/]
C --> D[Cus_consu = Cus_fabri + /Cus_fabri * 0.12\ + /Cus_fabri * 0.45]
D --> E

```
