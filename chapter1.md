--- 
title_meta  : Capítulo 1
title       : Introdução
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:aad1409c3d
## Comandos básicos do R

> A linguagem R

<p align="justify">R é uma linguagem de programação que pode ser utilizada em diversas áreas da ciência, pesquisas científicas, estatística e análise de dados. Devido a sua facilidade de manuseio, pode ser usada por alunos, trabalhadores, técnicos, professores e pesquisadores. Nesse ambiente os usuários podem limpar, analisar, visualizar e apresentar dados. O R é gratuito para download, pois está licenciado nos termos da licença GNU General Public. O R pode ser utilizado em todas as plataformas  Windows, Linux e Mac e seus comandos podem ser encontrados nesse link:</p>   

Comandos do R](https://stat.ethz.ch/R-manual/R-devel/library/base/html/00Index.html)

> Demonstrando o poder do R - seu primeiro programa

<p align="justify">Com apenas uma linha de código, você poderá escrever seu primeiro programa em R que gerará um gráfico de barras oriundo de uma tabela carregada com 5000 números aleatórios em uma distribuição normal com a frequência de cada um dos números. Foi atribuído a média desses números para 250 e o seu desvio padrão para 50. O comando floor remove o ponto decimal. Estes comandos é apenas para mostrar o poder da linguagem R, não se preocupe ainda em aprendê-los. Quando puder, execute o comando na sua plataforma R:</p> 

```{r}
barplot(table(floor(rnorm(5000, 250, 50))), xlab="Numeros aleatorios", ylab="Frequencias")
```

*** =instructions

- O editor à direita possui um código de exemplo. As linhas de comentários dos códigos são identificados pelo símbolo #.

- Adicione uma linha de código que calcule a multiplicação de 100*12/10 e clique no botão 'Submit Answer'.

*** =hint

- Digite 100*12/10 no editor à direita e clique no botão 'Submit Answer'.

- O símbolo "*" indica uma multiplicação.

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Calcule (escreva na linha abaixo) 100*12/10

```

*** =solution
```{r}
100*12/10
```
*** =sct

```{r}
test_output_contains("100*12/10", incorrect_msg = "Escreva corretamente a linha de código. Veja as dicas.")
success_msg("Bom trabalho! Veja como o console mostra as operações aritméticas. Agora que você está familiarizado com a interface do curso, vamos aprender mais sobre o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:955002b2b7
## Média aritmética

> <p align="justify">A média aritmética ($\bar{X}$) é o valor que mais se aproxima do valor real de uma medida. Para obtê-la, basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas. Simbolicamente, temos</p>

$$\bar{X} = \displaystyle \frac{X _{1}+X _{2}+X _{3}...+ X _{n}}{n},$$

ou, de uma maneira mais compacta:

$$\bar{X} =  {1 \over n} \sum_{i = 1}^n{X _i}.$$

> Fórmula para a média aritmética no R

```{r}
> mean(x)
```
> Motivação

* <p align="justify">Determine a média aritmética entre os números 10, 20 e 30.</p>

$$\bar{X} = \displaystyle \frac{10+20+30}{3}=20.$$

> Determinando a média aritmética no R:

<p align="justify">Por exemplo, numa experiência foram obtidas as seguintes medidas: 4, 5, 8, 9, 5. Em R, a média aritmética $\bar{X}$ pode ser calculada da seguinte maneira:</p>

```{r}
# Atribuir à variável x um vetor c:
x <- c(4, 5, 8, 9, 5)
# Determinar a média:
mean(x)

[1] 6.2
```

> <p align="justify">A seguir, mais exemplos de como é calculada a média aritmética no R, analise-os e exercite-os no seu ambiente R:</p>

```{r}
# Atribuir à variável a um vetor c:
a <- c(14, 20, 30, 50, 60, 56, 9, 5)
# Determinar a média:
mean(a)

[1] 30.5
```

```{r}
# Atribuir à variável x um vetor c:
x <- c(10, 20, 30)
# Determinarr a média:
mean(x)

[1] 20
```

```{r}
# Atribuir à variável a um vetor c:
a <- c(14, 6)
# Determinar a média:
mean(a)

[1] 10
```

* <p align="justify"> Nos comandos acima pudemos observar que um vetor representado pela letra c, formado pelas medidas dadas, foi armazenado em uma variável x (ou outra letra). Por meio do comando mean(x) é obtido a média das medidas - por exemplo, o comando mean(x) vai somar os números 4 + 5 + 8 + 9 + 5, dividir o resultado por 5 e mostrá-lo na tela, assim que teclarmos em 'Submit Answer', no editor do ambiente R.</p>

> Dever de casa - Faça no seu ambiente R:

<p align="justify">- Na escola, um estudante fez todas as provas de Matemática dos bimestres. Sendo que no 1º bimestre sua média correspondeu a 5.5, no 2º bimestre a 7.5, no 3º a 9.0 e no 4º a 5.0. Qual foi a média final do aluno? Resposta: 6.75.</p>

<p align="justify">- Um funcionário ganhou 1800 reais nos primeiros 3 meses. Nos últimos 3 meses ele ganhou 2000 reais. Qual foi sua média salarial em um semestre (6 meses)? Resposta 1900 reais.</p>


<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">ATIVIDADE</font></p>

<p align="justify"> Calcule a média aritmética das seguintes medidas: 10, 20, 30, 50, 100, 123, 233.</p>

*** =instructions

- O vetor que armazena os dados é representado por c(10, 20, 30, 50, 100, 123, 233). Armazene-o numa variável x.

*** =hint

- Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x. Após isso, tecle em 'Submit Answer'.

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Atribuir à variável x um vetor c:
x <- 
# Determinar a média: 
mean(x)
```
*** =solution
```{r}
# Atribuir à variável x um vetor c:
x <- c(10, 20, 30, 50, 100, 123, 233)
# Determinar a média:
mean(x)
```
*** =sct
```{r}
test_output_contains("80.85714", incorrect_msg = "Voce tem certeza que armazenou o vetor c na variavel x?")
success_msg("Bom trabalho! Agora você sabe calcular a média aritmética usando o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:dd48eb091a
## Média harmônica

> <p align="justify">A média harmônica ($\bar{X} _{H}$)  entre números reais e positivos é definida como o quociente entre a quantidade (n) de números pela soma dos inversos desses números. A média harmônica também é definida como sendo o inverso da média aritmética do inverso destes números. Simbolicamente, temos</p>

$$\bar{X} _{H}  = \displaystyle \frac{n}{\frac{1}{X _{1}}+\frac{1}{X _{2}}+ \frac{1}{X _{3}}+...+\frac{1}{X _{n}}},$$

ou, de uma maneira mais compacta:

$$\bar{X} _{H} = \displaystyle \frac{n} { \displaystyle \sum _{i=1}^{n} \left(\frac{1}{X _{i}} \right)} =  \left (\frac{1}{n}\sum _{i=1}^{n}\frac{1}{X _{i}}  \right )^{-1}.$$

> Fórmula para a média harmônica no R

```{r}
> 1/mean(1/x)
```
Exemplos de como é calculada a média harmônica no R:

```{r}
# Atribui-se à variável x o vetor c:
x <- c(3, 8, 5, 10.5)
# O inverso da média do inverso dos números contidos na variável x:
1/mean(1/x)
[1] 5.308057
```
ou

```{r}
x <- c(3, 8, 5, 10.5)
(1/4*sum(1/x))^(-1)
[1] 5.308057
```
> Aplicação 1

* <p align="justify">Um móvel se desloca até uma certa cidade com uma velocidade média (${V} _{m}$) de 18km/h. Depois retorna pelo mesmo percurso com uma velocidade média de 72km/h. Determine a velocidade média do percurso completo (ida e volta).</p>

<p align="justify">Utilizaremos a expressão que calcula a média harmônica:

$$\bar{X} _{H} = {V} _{m} = \displaystyle \frac{n}{\frac{1}{V1}+\frac{1}{V2}} \cdot$$

Substituindo as quantidades (temos dois valores de velocidades, n = 2) e os valores das velocidades na expressão acima e obteremos

$$\bar{X} _{H} = {V} _{m} = \displaystyle \frac{2} { \displaystyle \frac{1}{18} +\frac{1}{72}}=\displaystyle \frac{2} {\displaystyle\frac{5}{72}}=\displaystyle\frac{144}{5}=28.8~km/h \cdot $$

Logo abaixo, temos o código deste exercício de aplicação. No seu ambiente R, exercite-o: </p>

```{r}
# Atribui-se à variável x o vetor c:
x <- c(18,72)
# O inverso da média do inverso dos números contidos na variável x:
1/mean(1/x)
[1] 28.8
```
ou

```{r}
x <- c(18,72)
(1/2*sum(1/x))^(-1)
[1] 28.8
```

> Aplicação 2 

* <p align="justify">Uma motocicleta percorreu a distância entre duas cidades, com velocidade média de 60km/h e fez a viagem de regresso com velocidade média de 40km/h. Determine qual foi a velocidade média do percurso total, de ida e volta.</p>

$$\bar{X} _{H} = {V} _{m} = \displaystyle \frac{2} { \displaystyle \frac{1}{60} +\frac{1}{40}}=\displaystyle \frac{2} {\displaystyle\frac{5}{120}}=\displaystyle\frac{240}{5}=48~km/h \cdot $$

> Dever de casa

<p align="justify">Logo abaixo, temos o código deste exercício de aplicação para ser analisado e exercitado no seu ambiente R. É proveitoso exercitar sobre a média harmônica entre outros números quaisquer.</p>

```{r}
x <- c(60,40)
1/mean(1/x)
[1] 48
```
ou

```{r}
x <- c(60,40)
(1/2*sum(1/x))^(-1)
[1] 48
```

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">ATIVIDADE</font></p>

> Encontre a média harmônica entre 2, 5 e 10.

*** =instructions

* <p align="justify">Aplique os comandos estudados neste tópico para encontrar a média entre os números 2, 5, 10;</p>

* <p align="justify">Um auxílio para comparar cálculos de média harmônica pode ser encontrado neste link:</p> 

[Cálculo de média harmônica.](http://www.gyplan.com.br/pt/harmonic_mean_pt.html)</p>

*** =hint

- Atribua à variável x um vetor contendo os três números.

- O vetor deve começar com c. Assim: c(2,5,10).

- Observação: a solução matemática é 

$$H = \displaystyle \frac{3} { \displaystyle \frac{1}{2} +\frac{1}{5} + \frac{1}{10}}$$
$$= \displaystyle \frac{3} {\displaystyle {\frac{8}{10}}}=\displaystyle\frac{30}{8}=3.75.$$

*** =pre_exercise_code

```{r}

# no pec

```
*** =sample_code
```{r}
# Complete a linha abaixo com o vetor c
x <- 
(1/3*sum(1/x))^(-1)
```
*** =solution
```{r}
# Complete a linha abaixo com o vetor c
x <- c(2,5,10)
(1/3*sum(1/x))^(-1)
```
*** =sct
```{r}
test_output_contains("3.75", incorrect_msg = "Os números devem estar separados com vírgula e antecedidos pela letra c. Após isso, tecle em 'Submit Answer'.")
success_msg("Bom trabalho! Você adquiriu noções sobre média harmônica aplicada na Física em velocidades médias e em números.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:18b6a4eeb5
## Média geométrica

<p align="justify">Para determinar a média geométrica ($\bar{X} _{G}$) basta multiplicar todos os elementos dados no problema e extrair a raiz de índice n (número de elementos) deste produto. Simbolicamente, temos</p>

$$\bar{X} _{G} = \sqrt[n]{X _{1}.X _{2}.X _{3}.X _{4} \cdots a _n},$$

ou de uma maneira mais compacta:

$$\bar{X} _{G} = \left(\prod _{i=1}^{n}x _{i}\right)^{1/n}.$$
 
> Fórmula para a média geométrica no R

```{r}
> prod(x)^(1/n)
```
> Motivação

* Determine a média geométrica entre os números 2, 8, 32.

$$\bar{X} _{G} =\sqrt[3]{2.8.32}=\sqrt[3]{512}=\sqrt[3]{8^{3}}=8.$$

> Determinando a média geométrica no R:

```{r}
# Atribui-se à variável x o vetor c:
x <- c(2, 8, 32)
# Número de elementos n:
n <- 3
# Multiplicar os elementos e extrair a raiz cúbica:
prod(x)^(1/n)

[1] 8
```
> Determine a média geométrica entre os números 5, 7, 10, 15 e 21.

```{r}
x <- c(5, 7, 10, 15, 21)
n <- 5
prod(x)^(1/n)

[1] 10.19708
```

> Aplicação  

<p align="justify">A média geométrica é muito útil em situações que envolvem aumentos sucessivos. Suponhamos que uma classe 
de trabalhadores terá um aumento salarial de 5%, 10% e 15% em meses sucessivos. Determine a média geométrica dos aumentos.</p>

<p align="justify">Para acumular um aumento de 5%, 10% e 15% sobre o valor de um salário, a suas taxas percentuais devem ser transformadas em taxas unitárias:</p>

* 5% = 1.05 
* 10% = 1.10 
* 15% = 1.15


<p align="justify">Portanto, devemos determinar a média geométrica de 1.05, 1.10 e 1.15. Resolvendo no R, temos</p>

```{r}
# Atribui-se à variável x o vetor c:
x <- c(1.05, 1.10, 1.15)
# Número de elementos n:
n <- 3
# Multiplicar os elementos e extrair a raiz cúbica:
prod(x)^(1/n)

[1] 1.099242
```

<p align="justify">Observação: O fator 1.099242 equivale a uma taxa média aproximada de 10.99% de todos os aumentos sucessivos, ou seja, se for aplicado três vezes consecutivas a taxa aproximada de 10.99%, no final teremos o mesmo resultado que se tivéssemos aplicado os percentuais 5%, 10% e 15%.</p>

> Dever de casa

<p align="justify">- Analise e exercite, no seu ambiente R, sobre as médias geométricas dos números dados nos códigos abaixo:</p>

```{r}
# Atribui-se à variável x o vetor c:
x <- c(10, 20)
# Número de elementos n:
n <- 2
# Multiplicar os elementos e extrair a raiz cúbica:
prod(x)^(1/n)

[1] 14.14214
```

```{r}
x <- c(6.7, 2.2, 5)
n <- 3
prod(x)^(1/n)

[1] 4.192655
```

```{r}
x <- c(2, 4, 6, 8)
n <- 4
prod(x)^(1/n)

[1] 4.426728
```
<p align="justify">- Use os comandos do R neste problema: o $3º$ elemento de uma Progressão Geométrica (PG) é 3402 e o $1º$ é 378. Calcule o $2º$ termo desta PG. A resposta é 1134.</p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">ATIVIDADE</font></p>

> <p align="justify">Uma loja de software investiu em aplicações financeiras que lhe renderam 20% no primeiro ano e 30% no segundo ano. Qual o foi o rendimento médio deste investimento?</p>

*** =instructions

<p align="justify">- Para o cálculo do rendimento de 20% e 30% sobre o valor de um investimento inicial, estas taxas percentuais devem ser transformadas em taxas unitárias, ou seja, 20% = 1.2 e 30% = 1.3.<p align="justify"> 

<p align="justify">- Aplicar os comandos do R para achar as médias geométricas entre 1.2 e 1.3.</p>

<p align="justify">- Um auxílio para comparar cálculos de média geométrica pode ser encontrado neste link:</p> 

[Cálculo de média geométrica.](http://www.gyplan.com.br/pt/geometric_mean_pt.html)</p>

*** =hint

- Atribua à variável x um vetor contendo os três números. O vetor deve começar com c. Assim: c(1.2,1.3).

- O número de elementos (n) é igual a 2. 

*** =pre_exercise_code

```{r}

# no pec

```
*** =sample_code
```{r}
# Complete a linha abaixo com o vetor c:
x <- 
# Número de elementos n:
n <- 
# Multiplicar os elementos e extrair a raiz quadrada:
prod(x)^(1/n)
```
*** =solution
```{r}
# Complete a linha abaixo com o vetor c:
x <- c(1.2, 1.3)
# Complete a linha abaixo com o número de elementos:
n <- 2
# Multiplicar os elementos e extrair a raiz quadrada:
prod(x)^(1/n)
```
*** =sct
```{r}
test_output_contains("1.249", incorrect_msg = "Os números devem estar separados por vírgulas e antecedidos pela letra c. O n equivale a 2.")
success_msg("Bom trabalho! Você adquiriu noções sobre média geométrica aplicada em economia e em números.")
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
E <- abs(g - gr)
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
iiiiii

--- type:NormalExercise lang:r xp:100 skills:1 key:bc0cf7b809
## Operações aritméticas no ambiente R

Sendo um ambiente de desenvolvimento integrado para cálculos estatísticos e gráficos, o R possui uma grande quantidade de comandos. 

> Veja alguns comandos básicos: 

```{r}
# soma
3 + 6 + 12

[1] 6
```
```{r}
# subtração
2-4-8 

[1] -10
```
```{r}
# multiplica e soma
5 + 6 * 8

[1] 53         
```
```{r}
# divide e soma  
20/2 + 8

[1] 18        
```
```{r}
# potência (**)
10*2**2

[1] 40        
```
ou

```{r}
# potência (^)  
10*2^2

[1] 40
```

```{r}

2+(4**5)+(sqrt(144)/2) -(4^3)*6 + 2^(2^2)

[1] 664
```
ou

```{r}
# expressões
2+4**5+sqrt (144)/2 -4^3*6+2^2^2

[1] 664
```

```{r}
# raiz quadrada de 32
sqrt(32) 

[1] 5.656854
```
> Comandos para funções trigométricas, expressões algébrica e sequências numéricas

```{r}
# seno de pi constante
sin(pi)

[1] 1.224606e-16
```
```{r}
# seno de pi em radianos
sin(3.14159)

[1] 2.65359e-06
```
```{r}
# combinando várias expressões
sqrt(cos(60 * pi/180)) 

[1] 0.7071068 
```
```{r}
# atribui a x o sin(pi)
x <- sin(pi) 
# atribui a y a raiz de 100
y <- sqrt(100) 
# soma os valores guardados em y e x
y + x 

[1] 10
```
```{r}
# cria sequência de 1 até 10
1:10

 [1]  1  2  3  4  5  6  7  8  9 10 
```
```{r}
# eleva ao quadrado seus números
(1:10)^2 

 [1]   1   4   9  16  25  36  49  64  81 100     
```
```{r}
# somá-los
sum((1:10)^2)

[1] 385
```
```{r}
# cria uma sequência de 0 até 6
0:6

[1] 0 1 2 3 4 5 6 
```
```{r}
# faz 10 elevado a cada número da sequência
10^(0:6)

[1] 1e+00 1e+01 1e+02 1e+03 1e+04 1e+05 1e+06
```
> Explorando a função log10

Vamos utilizar alguns comandos já visto para resolvermos logaritmos. Na matemática, o logaritmo comum ou decimal de um número é o expoente a que a base deve ser elevado para produzir este número. Por exemplo, o logaritmo de 100 na base 10 é 2, pois 10 ao quadrado é 100. Veja como calcular o log de 100:

$$\sqrt{log(100)}\rightarrow10^{x}=100\rightarrow 10^{x}=10^{2}\rightarrow x =2$$

O log de zero não existe. O log de 1 na base 10 é zero:

$$\sqrt{log(1)} = 0$$

O log de 10 na base 10 equivale a 1:

$$\sqrt{log(10)}\rightarrow10^{x}=10\rightarrow 10^{x}=10^{1}\rightarrow x =1$$

O log de 10000000 na base 10 equivale a quanto? Veja:

$$\sqrt{log(10000000)}\rightarrow10^{x}=10000000\rightarrow 10^{x}=10^{7}\rightarrow x =7$$

> Calcule no R quanto vale a seguinte soma de logs:

$$\sqrt{log(1)}+\sqrt{log(10)}+\sqrt{log(100)}+...+\sqrt{log(10000000)}$$

> Passo-a-passo:

```{r}
# Fazer 10 elevado a cada número da sequência
10^(0:7)

[1] 1e+00 1e+01 1e+02 1e+03 1e+04 1e+05 1e+06 1e+07   
```

```{r}
# Determinar seus logs na sequência
log(10^(0:7))

[1]  0.000000  2.302585  4.605170  6.907755  9.210340 11.512925 13.815511 16.118096
```

```{r}
# Determinar suas respectivas raízes
sqrt(log(10^(0:7)))

[1] 0.000000 1.517427 2.145966 2.628261 3.034854 3.393070 3.716922 4.014735
```

```{r}
# Somá-las
sum(sqrt(log(10^(0:7))))

[1] 20.45124
```

*** =instructions

* Digite a soma de 10 mais 6 e a multiplicação de 50 vezes 6 (já feito).

* Depois digite 400 dividido por 4 mais 10 e crie uma sequência de números de 10 a 50 (já feito).

* Digite expressão para a soma das raízes dos logs dos números da sequência 1,  2,  4,  8 e 16.

*** =hint

- A expressão é semelhante a que foi mostrada nesse tópico! Crie a sequência com 2 elevado a 0:5.

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

# Dada a sequência 1,  2,  4,  8 e 16, determine na linha abaixo uma expressão para a soma das raízes dos logs desses números.

```
*** =solution
```{r}
sum(sqrt(log(2^(0:5))))
```
*** =sct
```{r}
test_output_contains("sum(sqrt(log(2^(0:5))))", incorrect_msg = "Os números da sequência são 1,  2,  4,  8 e 16. Crie essa sequência elevando dois a 0:5, como visto no tópico.")
success_msg("Bom trabalho! Neste tópico aprendemos aprendemos a somar, tirar raiz quadrada, criar sequências numéricas, elevar seus respectivos números ao quadrado, determinar seus logs, suas respectivas raízes e somá-las. ")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:6026cdef55
## Criando uma função no R

> Equação horária do MRUV

- Na Física temos o conhecido Movimento Retilíneo Uniformemente Variado(MRUV), onde a velocidade de um móvel varia igualmente em intervalos de tempos iguais, ou seja, sua acelaração é constante. A equação horária desse tipo de movimento equivale a uma equação do 2º grau, onde a condição para que o móvel passe pela origem da trajetória é determinada quando o espaço final (S) percorrido for igual a zero.

> Exemplos de equações horárias de movimentos de móveis:

$$S = 6 - 5t + 1t^{2}$$
com coeficientes: a = 1, b = -5, c = 6. Raízes: 2 e 3.
$$S = 30 + 20t - 5t^{2}$$
com coeficientes:  a = -5,  b = 20,  c = 30. Raízes: -1.162278 e 5.162278.
$$S = 6 + 8t + 4t^{2}$$  
com coeficientes:  a = -4,  b = 8,  c = 6. Raízes:  complexas. 
$$S = -2 - 3t + 5t^{2}$$ 
com coeficientes:  a = -5,  b = 3,  c = 2. Raízes:  -0.4 e 1.
$$S = -20 - t + t^{2}$$  
com coeficientes:  a = -1,  b = -1,  c = -20. Raízes:  -4 e 5.
$$S = -4 - 3t + t^{2}$$
com coeficientes:  a = -1,  b = -3,  c = -4. Raízes: -1 e 4. 
$$S = 7 - 8t + t^{2}$$
com coeficientes:  a = -1,  b = -8,  c = 7. Raízes: 1 e 7.

> Criando a função passo-a-passo

- É necessário criarmos uma função para o cálculo do instante (ou instantes) em que o móvel passa pela origem da trajetória. 

- No caso dessa função, vamos chamar estes instantes de tempo1 e tempo2 que correspondem às raízes da equação. 

- O nome da função será "raízes". Atribua a ele o comando function( ). A função precisará de informações ou argumentos: coloque nos parênteses os coeficientes separados por vírgula (a, b, c). 

- A partir daí delimite por chaves os comandos necessários para a funçãos. O return() é um comando não obrigatório, mas que é bastante comum no final das funções. Não o usaremos aqui. 

- Depois de tudo pronto, execute a função digitando-a pelo nome com os argumentos dentro dos parênteses (a, b, c). Assim:

```{r}
coefic <- function(a,b,c){
    delta <- b^2 - 4*a*c
    if(delta<0){
        cat("Essa equação de movimento não possui raízes reais - são raízes complexas")
    } else{
        raiz1 <- (-b - sqrt(delta))/(2*a)
        raiz2 <- (-b + sqrt(delta))/(2*a)
        cat("as raízes são reais:", raiz1, "e", raiz2)
    }
}
```
- Depois basta digitar, por exemplo, os coeficientes das raízes: coefic (1, -5, 6) e teclar "Enter". Em seguida aparecerá na tela as duas raízes que são os intantes na Física. Na prática o tempo sempre é positivo, por isso, qualquer raiz negativa (complexa) será desconsiderada. Você pode executar esse procedimento para todas as equações dadas no tópico. Veja exemplo:

```{r}
> coefic (1, -5, 6)
as raízes são 2 e 3 
```
*** =instructions

* Aplique a condição para que o móvel passe pela origem da trajetória, quando $S = 0$. Crie uma função que determine e mostre as raízes na tela;

* Escolha um nome (coeficientes) para a função. Atribua a ele o comando function( ). Dentro dos parênteses do comando function digite os argumentos separados por vírgula (a, b, c). A partir daí delimite por chaves os comandos necessários para a função;

* Execute a função digitando-a pelo nome, conforme mostrado no exemplo anterior. Use a seguinte equação:
$$S = -4 - 3t + t^{2}.$$

* A resposta do problema é que, de acordo com a equação, o móvel passa pela origem da trajetória no instante (raiz) 4 segundos. 

*** =hint

- O nome dado à função foi: coeficientes.

- Digite o nome da função com seus coeficientes entre parênteses.

*** =pre_exercise_code
```{r}

# no pec

```

*** =sample_code
```{r}

coeficientes <- function(a,b,c){
    delta <- b^2 - 4*a*c
    if(delta<0){
        cat("Essa equação de movimento não possui raízes reais - são raízes complexas. Tente outra")
    } else{
        tempo1 <- (-b - sqrt(delta))/(2*a)
        tempo2 <- (-b + sqrt(delta))/(2*a)
        cat("as raízes (instantes) são", tempo1, "e", tempo2)
    }
}
# Digite na linha abaixo o nome da função (coeficientes) com os seus respectivos coeficientes e tecle Enter.

```

*** =solution
```{r}

coeficientes <- function(a,b,c){
    delta <- b^2 - 4*a*c
    if(delta<0){
        cat("Essa equação de movimento não possui raízes reais - são raízes complexas. Tente outra")
    } else{
        tempo1 <- (-b - sqrt(delta))/(2*a)
        tempo2 <- (-b + sqrt(delta))/(2*a)
        cat("as raízes (instantes) são", tempo1, "e", tempo2)
    }
}
coeficientes (1, -3, -4)
```

*** =sct
```{r}

test_output_contains("coeficientes (1, -3, -4)", incorrect_msg = "O nome da função é coeficientes. Digite o nome da função com os seus respectivos coeficientes e tecle Enter.")
success_msg("Bom trabalho! Você adquiriu noções sobre a equação horária do MRUV e desenvolveu uma função para determinar o instante (raiz) ou instantes (raízes) em que um móvel passa pela origem (0) da trajetória.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:3fde33b8e4
## Escalas termométricas

> Escala termométrica Kelvin

<p align="justify">A escala Kelvin foi construída baseado em pesquisas que apontam que o zero absoluto é a menor temperatura (0K) encontrada na natureza e corresponde na escala Celsius a -273,15°C, por isso é chamada de escala absoluta de temperatura. Possui um ponto de gelo equivalente a aproximadamente 273,15K e um ponto de ebulição equivalente a aproximadamente 373,15K. O Kelvin é a unidade de medida de base do Sistema Internacional de Unidades (SI) para a grandeza temperatura. A expressão para transformar unidades de medidas de temperaturas Celsius para Kelvin é dada por:</p>

$$TK= TC + 273.15$$

> Escala termométrica Celsius

<p align="justify">O grau Celsius ou Centígrado é uma unidade de medida de temperatura oriundo da escala termométrica Celsius. Nesta, o ponto de gelo corresponde a 0°C e o ponto de vapor corresponde a 100°C. A expressão para transformar unidades de medidas de temperaturas Kelvins em Celsius é dada por:</p></p> 

$$TC = TK - 273.15$$

> Escala termométrica Fahrenheit

<p align="justify">O grau Fahrenheit é uma unidade de medida de temperatura oriundo da escala termométrica Fahrenheit, onde o ponto de gelo corresponde a 32°F  e o ponto de vapor corresponde a 212°F. O zero absoluto é definido como igual a -459,67°F. A expressão para transformar unidades de medidas de temperaturas Fahrenheit em Celsius é dada por:</p>

$$TC = (TF - 32)/1.8$$

> Criando mais funções

<p align="justify">Baseado nas fórmulas de conversões de escalas termométricas, podemos criar algumas funções no R. 

Função que transforma graus Kelvins em graus Celsius:</p>

```{r}
KemC <- function(Kelvin,Celsius){# <== Cria a função KemC 
	# Fórmula de conversão:
    Celsius <- Kelvin-273.15
	# Retorna o resultado calculado:
    return(Celsius)
}
```
> No seu ambiente R, transforme 300K em Celsius. 

<p align="justify"> Basta digitar, no ambiente R, o nome da função seguida com o dado entre parênteses e teremos como resposta 26.85°C. Veja:</p>

```{r}
KemC(300)
[1] 26.85
}
```
> Função que transforma graus Celsius em graus Kelvins

* No seu ambiente R, transforme 10K em Celsius.

```{r}
CemK <- function(Celsius,Kelvin){# <== Cria a função CemK 
	# Fórmula de conversão:
    Kelvin <- Celsius + 273.15
	# Retorna o resultado calculado:
    return(Kelvin)
}
```

> Função que transforma graus Fahrenheit em Kelvins

- No seu ambiente R, transforme 32°F em Celsius.

```{r}
FemK <- function(Fahrenheit,Kelvin){# <== Cria a função FemK 
	# Fórmula de conversão:
	Kelvin <- (Fahrenheit + 459.67)/1.8
	# Retorna o resultado calculado:
    return(Kelvin)
}
```

> Função que transforma graus Kelvins em Fahrenheit

- No seu ambiente R, transforme 100K em Fahrenheit.

```{r}
KemF <- function(Kelvin,Fahrenheit){# <== Cria a função KemF 
	# Fórmula de conversão:
	Fahrenheit <- (Kelvin*1.8)-459.67)
	# Retorna o resultado calculado:
    return(Fahrenheit)
}
```

> Função que transforma graus Fahrenheit em Celsius

- No seu ambiente R, transforme 40°F em Fahrenheit.

```{r}
FemC <- function(Fahrenheit,Celsius){# <== Cria a função FemC 
	# Fórmula de conversão:
	Celsius <- (F - 32)/1.8
	# Retorna o resultado calculado:
    return(Celsius)
}
```

### Atividade

> Tente criar uma função que transforma graus Celsius em Fahrenheit

- No nosso ambiente R, transformaremos 100°C em Fahrenheit.

*** =instructions

* Estude e analise a função;

* Digite a função seguida de 100 e clique no botão 'Submit Answer';
 
* Um auxílio sobre resultados de transformações de graus em escalas termométricas pode ser encontrado neste link: 
[conversor de temperaturas.](https://www.google.com.br/#q=transformar+graus)

*** =hint

- O nome dado à função deve ser digitado seguido com o número a ser transformado.

- O nome da função está à esquerda do comando "function".

*** =pre_exercise_code
```{r}

# no pec

```

*** =sample_code
```{r}
CemF <- function(Celsius,Fahrenheit){# <== Cria a função CemF 
    # Fórmula de conversão:
    Fahrenheit <- (1.8*Celsius + 32)
    # Retorna o resultado calculado:
    return(Fahrenheit)
}
# Na linha abaixo, escreva o comando de conversão de 100°C em Fahrenheit:

```

*** =solution
```{r}
CemF <- function(Celsius,Fahrenheit){# <== Cria a função CemF 
    # Fórmula de conversão:
    Fahrenheit <- (1.8*Celsius + 32)
    # Retorna o resultado calculado:
    return(Fahrenheit)
}
# Na linha abaixo, escreva o comando de conversão de 100°C em Fahrenheit:
CemF(100)
```

*** =sct
```{r}
test_output_contains("CemF(100)", incorrect_msg = "O nome da função deve ser seguida com o dado que é o 100. Digite o dado entre parênteses e tecle 'Submit Answer'.")
success_msg("Bom trabalho! Você adquiriu mais noções sobre como criar uma função e aprendeu um pouco sobre Termologia e escalas termométricas.")
```