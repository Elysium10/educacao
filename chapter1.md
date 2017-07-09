---
title       : Introdução 
description : Insert the chapter description here
attachments :
--- type:NormalExercise lang:r xp:100 skills:1 key:aad1409c3d
## Comandos básicos do R

*** =instructions
- O editor à direita possui um código de exemplo. Você consegue identificar quais linhas são códigos em R e quais são comentários?
- Adicione uma linha de código que calcule a soma de 6 + 12, e clique no botão ‘Submit Answer’.

*** =hint
Adicione uma linha em R que calcule 6 + 12, exatamente igual ao código de exemplo!

*** =pre_exercise_code
```{r}
# no pec
```

*** =sample_code
```{r}
# Calcule 3 + 4
3 + 4

# Calcule 6 + 12

```
*** =solution
```{r}
# Calcule 3 + 4
3 + 4

# Calcule 6 + 12
6 + 12
```

*** =sct
```{r}
test_output_contains("18", incorrect_msg = "Tenha certeza que você inseriu uma nova linha que some 6 + 12. Não o inicie esta linha com um `#`, senão o código não será  executado!")
success_msg("Parabéns! Veja como o console mostra o resultado do seu código. Agora, que você está familiarizado com a interface do curso, vamos aprender R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:955002b2b7
## Média aritmética

É o valor que mais se aproxima do valor real. Para obtê-la basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas. Por exemplo, numa experiência foram obtidas as seguintes medidas: 4m, 5m, 8m, 9m, 5m. Em R a média aritmética $\bar{x}$ pode ser calculada da seguinte maneira:

<p style="background-color: rgb(102, 255, 255);">É o valor que mais se aproxima do valor real. Para obtê-la basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas. Por exemplo, numa experiência foram obtidas as seguintes medidas: 4m, 5m, 8m, 9m, 5m. Em R a média aritmética $\bar{x}$ pode ser calculada da seguinte maneira:</p>

<div style="font-size: large; font-family: sans-serif">
  <p style="color: #000000; background-color: #ffffff">Text color: black, background-color: white</p>
  <p style="color: #ffffff; background-color: #000000">Text color: white, background-color: black</p>
  <p style="color: #ff0000; background-color: #ffffff">Text color: red, background-color: white</p>
  <p style="color: blue; background-color: #ffffff">Text color: blue, background-color: white</p>
  <p style="color: green; background-color: #ffff42">Text color: green, background-color: yellow</p>
  <p style="color: #ffffff; background-color: #ff0000">Text color: white, background-color: red</p>
</div>

```{r}
x <- c(4, 5, 8, 9, 5)
mean(x)
```
Depois basta teclar enter para obter o resultado.

> #### Efetuando várias medidas -  cálculo de $\bar{x}$

> Calcule a média aritmética das seguintes medidas: 10, 20, 30, 50, 100, 123, 233.

*** =instructions
- Use o mesmo procedimento feito no código acima acima.
- O vetor é c(10, 20, 30, 50, 100, 123, 233). Armazene-o numa variável.

*** =hint
Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x e use o comando mean(x)

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Calcule a média aritmética pedida

mean(x)
```
*** =solution
```{r}
x <- c(10, 20, 30, 50, 100, 123, 233)
mean(x)
```
*** =sct
```{r}
test_output_contains("80.85714", incorrect_msg = "Voce tem certeza que armazenou o vetor c na variavel x?")
success_msg("Parabéns! Agora você sabe calcular a média aritmética usando o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:dd48eb091a
## Erro absoluto (E)

Podemos encontrar o erro aboluto de uma medida usando a seguinte expressão: 

> $$E = {\left |m-\bar{m}  \right |}$$

> onde,

> $E$ - erro absoluto.

> $m$ - valor correto.

> $\bar{m}$ - valor obtido nas medidas.

No R, a fórmula de erro absoluto é escrita assim:

```{r}
E <- abs(m - mean(x))
E
```
Depois basta teclar enter para obter o resultado.

> #### Medindo alturas - cálculo do E

> Suponha que você tenha a tarefa de medir várias vezes a altura de uma porta e obteve as seguintes medidas: 2.17, 2.20, 2.15 e 2.12. Se o valor correto da medida da altura da porta corresponde a 2.10m, calcule o erro absoluto (E).

*** =instructions
- Calcule a média aritmética das medidas ==> mean(x). 
- Subtraia a média encontrada da medida correta ==> m - mean(x). 
- Obtenha o módulo (valor absoluto) dessa diferença ==> abs(m - mean(x)).
*** =hint

Armazene 2.10 na variável m.
Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x e o valor 
da medida correta numa variável m e use o comando mean(x).

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Armazene o valor da medida correta. 
m <- 
# Crie um vetor c com as medidas dadas e o armazene em uma variável x.
x <- 
# Use o comando mean(x) para calcular a média.
mean ()
# Obtenha o módulo (valor absoluto) dessa diferença e armazene a média numa variável.
E <- abs(m - mean(x))
# Mostre o valor de E na tela.
E
```
*** =solution
```{r}
m <- 2.10
x <- c(2.17, 2.20, 2.15, 2.12)
mean(x)
E <- abs(m - mean(x))
E 
```
*** =sct
```{r}
test_output_contains("0.06", incorrect_msg = "Você armazenor corretamente o vetor x <- c(2.17, 2.20, 2.15, 2.12) na variável x?")
success_msg("Parabéns! Agora você sabe calcular o erro absoluto usando o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:24e7dc599e

## Medida da aceleração da gravidade

> #### Valor teórico da aceleração da gravidade

> O valor teórico da aceleração da gravidade (g) é aproximadamente igual a 9,8 m/s<SUP>2</SUP>. Suponha que você efetuou várias medidas da aceleração e achou outro valor que corresponde a 10.2 m/s<SUP>2</SUP>. Determine o erro absoluto (E).

*** =instructions
- Nesse caso, a média aritmética corresponde à medida experimental efetuada de 10.2 m/s<SUP>2</SUP>. 
- Subtraia o valor da medida experimental do valor da medida correta.  
- Obtenha o módulo (valor absoluto) dessa diferença.
*** =hint

Armazene $9.8m/s^2$ na variável g.
Armazene a medida efetuada de $10.2m/s^2$ em uma variável qualquer (gr).

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Armazene o valor da medida correta de 9.8. 
g <- 
# Armazene a medida efetuada de 10.2 em uma variável qualquer (gr).
gr <- 
# Obtenha o módulo (valor absoluto) da diferença entre a medida correta e a medida experimental e armazene-o na variável E.
E <- abs(9.8 - 10.2)
# Mostre o valor do erro na e E na tela, digitando Eteclando Enter.
E
```
*** =solution
```{r}
g <- 9.8
gr <- 10.2
E <- abs(g - gr)
E 
```
*** =sct
```{r}
test_output_contains("0.4", incorrect_msg = "Você armazenou corretamente 9.8 na varável g? e 10.2 na varável gr?")
success_msg("Parabéns! Agora você sabe calcular o erro absoluto usando o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:7f8c3148a8
## Erro relativo

> #### Erro relativo de duas medidas

> Do exemplo anterior, determine o erro relativo entre as medidas dadas.

A expressão para calcular o erro relativo $E_{r}$:

$E_{r} = \frac{\left |g- gr  \right |}{g}$

onde,

$\left |g-gr  \right |$ - módulo da diferença entre os valores das medidas teóricas e experimentais.

Tanto nesse caso como no exemplo anterior, o valor obtido nas medidas experimentais é o mesmo valor da média aritmética.

*** =instructions
- Mesmo procedimento do exercício anterior: a medida experimental corresponde à média aritmética efetuada de $10.2m/s^2$. 
- Subtraia o valor da medida experimental do valor da medida correta.  
- Obtenha o módulo (valor absoluto) dessa diferença e divida pelo valor da medida correta.
*** =hint
Armazene $9.8m/s^2$ na variável g.
Armazene a medida efetuada de $10.2m/s^2$ em uma variável qualquer (gr).
Obtenha o módulo (valor absoluto) dessa diferença e divida pelo valor da medida correta.
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Armazene o valor da medida correta de 9.8. 
g <- 
# Armazene a medida efetuada de 10.2 em uma variável qualquer (gr).
gr <- 
# Obtenha o módulo (valor absoluto) da diferença entre a medida correta e a medida experimental e armazene-o na variável E.
Er <- abs(g - gr)/g
# Mostre o valor do erro relativo, digitando Eteclando Enter.
Er
```
*** =solution
```{r}
g <- 9.8
gr <- 10.2
Er <- abs(g - gr)/g
Er 
```
*** =sct
```{r}
test_output_contains("0.04081", incorrect_msg = "Você armazenou corretamente 9.8 na varável g e 10.2 na varável gr?")
success_msg("Parabéns! Agora você sabe calcular o erro relativo usando o R!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:bc0cf7b809
## Operações aritméticas no ambiente R

Sendo um ambiente de desenvolvimento integrado para cálculos estatísticos e gráficos, o R possui uma grande quantidade de comandos. Veremos alguns comandos básicos. 

```{r}
3 + 6 + 12   # soma   
[1] 6
```
```{r}
2-4-8   # subtração
[1] -10
```
```{r}
5 + 6 * 8  # multiplica e soma 
[1] 53         
```
```{r}
20/2 + 8  # divide e soma  
[1] 18        
```
```{r} 
10*2**2 # potência (**).
[1] 40        
```
ou

```{r}
10*2^2  # potência (^)       
[1] 40
```

```{r}
 2+(4**5)+(sqrt(144)/2) -(4^3)*6 + 2^(2^2) # expressões
[1] 664
```
ou

```{r}
2+4**5+sqrt (144)/2 -4^3*6+2^2^2
[1] 664
```

```{r}
sqrt(32) # raiz quadrada de 32
[1] 5.656854
```
<p style="color: #ff0000; background-color: #ffffff">Comandos para funções trigométricas, expressões algébrica e sequências numéricas Text color: red, background-color: white</p>

```{r}
sin(pi) # seno de pi constante
[1] 1.224606e-16
```
```{r}
sin(3.14159) # seno de pi em radianos
[1] 2.65359e-06
```
```{r}
sqrt(cos(60 * pi/180)) # combinando várias expressões
[1] 0.7071068 
```
```{r}
x <- sin(pi) # atribui a x o sin(pi)
y <- sqrt(100) # atribui a y a raiz de 100
y + x # soma os valores guardados em y e x
[1] 10
```
```{r}
1:10  # cria sequência de 1 até 10 e...
 [1]  1  2  3  4  5  6  7  8  9 10 
```
```{r}
(1:10)^2 # eleva ao quadrado seus números e...
 [1]   1   4   9  16  25  36  49  64  81 100     
```
```{r}
sum((1:10)^2) # somá-los.
[1] 385
```
```{r}
0:6  # cria uma sequência de 0 até 6 e...
[1] 0 1 2 3 4 5 6 
```
```{r}
10^(0:6) # faz 10 elevado a cada número da sequência e... 
[1] 1e+00 1e+01 1e+02 1e+03 1e+04 1e+05 1e+06
```

<p style="color: #ff0000; background-color: #ffffff">Explorando a função log10 Text color: red, background-color: white</p>

Vamos utilizar alguns comandos já visto para resolvermos logaritmos. Na matemática, o logaritmo comum ou decimal de um número é o expoente a que a base deve ser elevado para produzir este número. Por exemplo, o logaritmo de 100 na base 10 é 2, pois 10 ao quadrado é 100. Veja como calcular o log de 100:

$$\sqrt{log(100)}\rightarrow10^{x}=100\rightarrow 10^{x}=10^{2}\rightarrow x =2$$

O log de zero não existe. O log de 1 na base 10 é zero:

$$\sqrt{log(1)} = 0$$

O log de 10 na base 10 equivale a 1:

$$\sqrt{log(10)}\rightarrow10^{x}=10\rightarrow 10^{x}=10^{1}\rightarrow x =1$$

O log de 10000000 na base 10 equivale a quanto? Veja:

$$\sqrt{log(10000000)}\rightarrow10^{x}=10000000\rightarrow 10^{x}=10^{7}\rightarrow x =7$$

Calcule no R quanto vale a seguinte soma de logs:

$$\sqrt{log(1)}+\sqrt{log(10)}+\sqrt{log(100)}+ \sqrt{log(1000)}+\sqrt{log(10000)}+ \sqrt{log(100000)}+\sqrt{log(10000000)}$$

Passo-a-passo:

```{r}
10^(0:7) # fazer 10 elevado a cada número da sequência e... 
 10^(0:7)
[1] 1e+00 1e+01 1e+02 1e+03 1e+04 1e+05 1e+06 1e+07   ## faz 10 elevado a cada número da sequência e...
```

```{r}
log(10^(0:7))   #   determina seus logs na sequência e...
[1]  0.000000  2.302585  4.605170  6.907755  9.210340 11.512925 13.815511 16.118096
```

```{r}
sqrt(log(10^(0:7)))  # suas respectivas raizes e...
[1] 0.000000 1.517427 2.145966 2.628261 3.034854 3.393070 3.716922 4.014735
```

```{r}
sum(sqrt(log(10^(0:7)))) # somá-las
[1] 20.45124
```

*** =instructions
Digite a soma de 10 mais 6 (, digite a multiplicação de 50 vezes 6.
Depois digite 400 dividido por 4 mais 10 e crie uma sequência de números de 10 a 50.

*** =hint
Adicione uma linha em R que crie uma sequência de números de 10 a 50, conforme foi mostrado no código de exemplo!

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Digite a soma de 10 mais 6
10 + 6

# Digite a multiplicação de 50 vezes 6
50*6

# Digite 400 dividido por 4 mais 10
400/4 + 10 

# Crie uma sequência de números de 10 a 50.
```
*** =solution
```{r}
10:50
```
*** =sct
```{r}
test_output_contains("10:50", incorrect_msg = "Coloque dois pontos no meio dos números que vão delimitar a sequência!")
success_msg("Bom trabalho! Neste tópico aprendemos aprendemos a somar, tirar raiz quadrada, criar sequências numéricas, elevar seus respectivos números ao quadrado, determinar seus logs, suas respectivas raízes e somá-las. ")
```