--- 
title_meta  : Capítulo 3
title       : Elementos do movimento oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:92a2d6e6a2
## Posição do projétil
<style type="text/css">
.letras{
width:300px;line-height:1.5;position:relative; text-align:justify;font-family:Calibri;font-size:16px;line-height:1.5em;border:#7FFF00 2px none;
padding:5px;border-radius:5px;-moz-border-radius:5px; -webkit-border-radius:5px;background:#DDD text-shadow:1px 1px #fff;
box-shadow:0 0 0 6px #33a0c2;
}
</style>
<p align="justify"> A equação que fornece a posição do projétil no instante t, segundo o eixo horizontal (X), é dada por </p>

$$X= v _{ix}.t$$

<p align="justify"> e a equação que fornece a posição do projétil no instante t, segundo o eixo vertical (Y), é dada por </p>
 
$$Y = v _{ix}.t- \displaystyle \frac{g.t^{2}}{2}\cdot$$

<p align="justify">Para determinar uma posição qualquer do projétil, basta obter os valores de X e Y.</p> 

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a posição do projétil em 2 segundos e 4 segundos. Considere $g = 9,8~m/s^{2}$, a $v _{ix} = 43.30~m/s$ e a $v _{iy} = 25~m/s$ foram determinados anteriormente.</p>

> <p align="justify"> Posição do projétil para t = 2s</p> 

$$X= v _{ix}.t = 43,30.2 = 86,6~m.$$

e

$$Y = v _{iy}.t- \displaystyle \frac{g.t^{2}}{2} = 25.2 - \displaystyle \frac{9,8.2^{2}}{2}$$ 
$$= 50 - 19,6 = 30,4~m.$$

> <p align="justify"> Cálculo da posição para t = 4s</p>

$$X= v _{ix}.t = 43,30.4 = 173,2~m.$$

e

$$Y = v _{iy}.t- \displaystyle \frac{g.t^{2}}{2} = 25.4 - \displaystyle \frac{9,8.4^{2}}{2}$$ 
$$= 100 - 78,4 = 21,6~m.$$

> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal e vertical de v e a velocidade resultante - todos no tempo de 2 segundos:</p>

```{r}
# Acel. gravidade:
g <- 9.8
# Instante dado:
t <- 2
# vix:
vix <- 43.30127
# viy:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# vx uniforme igual vix:
vx <- vix
# vy:
vy <- viy - g * t 
# vr:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("X = ",  X, "e Y = ", Y)
cat("vx = ", vx, "e vy = ", vy)
cat("vr = ", vr)

X =  86.60254 e Y =  30.4
vx =  43.30127 e vy =  5.4
vr =  43.63668
```
> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal vx, a componente vertical vy e a velocidade resultante vr - todos no tempo de altura máxima:</p>

```{r}
# Acel. gravidade:
g <- 9.8
# Instante na hmax:
t <- 2.5510204081632653061224489795918
# vix:
vix <- 43.30127
# viy:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# vx igual vix:
vx <- vix
# vy:
vy <- viy - g * t 
# vr:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("X = ",  X, "e Y = ", Y)
cat("vx = ", vx, "e vy = ", vy)
cat("vr = ", vr)

X =  110.4624 e Y =  31.88776
vx =  43.30127 e vy =  0
vr =  43.30127
```
<p align="justify">Observe que o valor de X na altura máxima equivale a 110,4624 m, a metade do alcance (A = 220,9248m).O valor de Y, para esse tempo exato, equivale à altura máxima (31,88776m). Note que a componente da velocidade na horizontal (vx = vix), em um dado tempo, não varia.</p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>

<p align="justify"> Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine, além da posição do projétil em 4 segundos, as suas componentes horizontal e sua velocidade resultante. Considere $g = 9,8~m/s^{2}$, a $v _{ix} = 43.30~m/s$ e a $v _{iy} = 25~m/s$ foram determinados em tópicos anteriores.</p>

<center><div class="letras">
Obs.: Neste exercício você observará que, após o tempo da altura máxima de 2,5510...m, no caso 4s, o projétil estará caindo e, no eixo X, o projétil já estará depois da metade do alcance (110,4624), no caso, 173,2051m. Na queda do projétil, a componente vertical da velocidade vy estará negativa e o vetor resultante vr será sempre positivo.</div></center>

*** =instructions
<p align="justify"> - Use os comandos em R, estudados neste capítulo, para calcular a posição do projétil no tempo de 4s. Escreva a equação da posição do projétil no eixo X.</p>

*** =hint
<p align="justify"> - O valor da posição do projétil, no eixo X, é obtido pela seguinte expressão:</p>
$$X= v _{ix}.t.$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 4
# Componente vix:
vix <- 43.30127
# Componente viy:
viy <- 25
# Escreva a posição em X
X <- 
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# Componente vx:
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("vx:", vx, "e vy:", vy)
cat("vr no tempo dado é", vr)
# Mostrar posição Y
Y
# Mostrar posição X
X
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 4
# Componente vix:
vix <- 43.30127
# Componente viy:
viy <- 25
# Escreva a posição em X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# Componente vx:
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("vx:", vx, "e vy:", vy)
cat("vr no tempo dado é", vr)
# Mostrar posição Y
Y
# Mostrar posição X
X
```
*** =sct
```{r}
test_output_contains ("173.2051", incorrect_msg = "Escreva a expressão que calcula o valor da posição de um projétil no eixo X. Não esqueça que o símbolo para multiplicar é o asterisco. Veja nas dicas essa expressão.")
success_msg ("Bom trabalho! Você aprendeu a determinar o valor da posição (X, Y) de um projétil em um determinado tempo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:da26d811b1
## Atividade - Posição do projétil

<style type="text/css">
.letras{
width:300px;line-height:1.5;position:relative; text-align:justify;font-family:Calibri;font-size:16px;line-height:1.5em;border:#7FFF00 2px none;
padding:5px;border-radius:5px;-moz-border-radius:5px; -webkit-border-radius:5px;background:#DDD text-shadow:1px 1px #fff;
box-shadow:0 0 0 6px #33a0c2;
}
</style>
<style type="text/css">
.exerc{
background-color:#33a0c2; font-weight: bold; font-size:20px; color:#ffffff; text-align:center;
}
</style>
> <p align="justify"> Quando o alcance é quatro vezes maior que a altura máxima</p>

 * <p align="justify"> Um projétil é lançado a partir do solo com uma velocidade inicial igual a 100 m/s, formando um ângulo de tiro de 45°. Quando o ângulo de lançamento é equivalente a 45° o alcance (A) é máximo. Mostre no R que o valor desse alcance é quatro vezes maior que o valor da altura máxima (hmáx). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>

```{r}
# Acel.gravidade:
g <- 9.8
# vi:
vi <- 100
# Ângulo graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# vix:
vix <- vi * cos(teta)
# viy:
viy <- vi * sin(teta) 
# Tempo subida:
thmax <- viy/g
# tempo total:
ttot = 2 * thmax
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# alcance
A = vix * ttot
cat("A altura máxima é", hmax)
cat("O alcance é", A)
cat(A, "é 4 vezes", hmax)
```
> Compare sua resposta:

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A altura máxima é 255.102; <br>  O alcance é 1020.408; <br>  1020.408 é 4 vezes 255.102.</font></p>
<center><div class="exerc">EXERCÍCIO PROPOSTO</div></center>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a posição do projeto no tempo de 2 segundos. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Use os comandos em R, estudados neste capítulo, para calcular a posição do projétil no tempo de 2s. Você escreverá apenas a equação da posição do projétil no eixo X.</p>

*** =hint
<p align="justify"> O valor da posição do projétil, no eixo X, é obtido pela seguinte expressão:</p>
$$X= v _{ix}.t.$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Acel. gravidade:
g <- 9.8
# Instante dado:
t <- 2
# vi:
vi <- 200
# Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# Componente viy:
viy <- vi * sin(teta)
# vx uniforme igual vix:
# Escreva eq. posição em X
X <- 
# Equação posição em Y
Y <- viy * t - (g * t ^ 2)/2 
# Mostrar Y
Y
# Mostrar X
X
```
*** =solution
```{r}
# Acel. gravidade:
g <- 9.8
# Instante dado:
t <- 2
# vi:
vi <- 200
# Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# Componente viy:
viy <- vi * sin(teta)
# vx uniforme igual vix:
# Escreva eq. posição em X
X <- vix * t
# Equação posição em Y
Y <- viy * t - (g * t ^ 2)/2 
# Mostrar Y
Y
# Mostrar X
X
```
*** =sct
```{r}
test_output_contains ("200", incorrect_msg = "Escreva a expressão que calcula o valor da posição de um projétil no eixo X. Não esqueça que o símbolo para multiplicar é o asterisco. Veja nas dicas essa expressão.")
success_msg ("Bom trabalho! Você aprendeu mais sobre como determinar o valor da posição (X, Y) de um projétil em um determinado tempo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:289ca73696
## Direção do projétil
<style type="text/css">
.exerc{
background-color:#33a0c2; font-weight: bold; font-size:20px; color:#ffffff; text-align:center;
}
</style>
<p align="justify"> O ângulo de lançamento do projétil foi chamado de $\theta$. A direção do projétil em um dado instante t será chamado de ângulo $\alpha$, que será determinado pelo cálculo da tangente entre a componente da velocidade na vertical e a componente da velocidade na horizontal. A expressão que calcula a tangente desse ângulo é dada por:</p>

$$tg~ \alpha  = \displaystyle \frac{v _{y}}{v _{x}}$$

<p align="justify"> onde, $\alpha$ corresponde ao ângulo formado entre a componente horizontal e a direção da velocidade resultante num dado instante, $v _{y}$ corresponde à componente da velocidade segundo a vertical e $v _{x}$ corresponde à componente da velocidade segundo a horizontal.</p>

<p align="justify">Da expressão acima podemos encontar o valor do ângulo $\alpha$:</p> 

$$\alpha = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo com uma velocidade inicial igual a 50 m/s. Seu ângulo de lançamento equivale a 30°. Determine a direção do projétil ao atingir o solo. Considere $g = 9,8~m/s^{2}$. A $v _{x} = 43,30127~m/s$ e a $v _{y} = -25~m/s$ foram determinados anteriormente.</p>

> Determinando a tangente do ângulo

$$tg~ \alpha  = \displaystyle \frac{v _{y}}{v _{x}}= \frac{-25}{43,30127}\cong-0,57735.$$

<p align="justify">Link para auxílio no cálculo da tangente (use números com vírgula):</p>

[Calculadora on-line da tangente.](https://www.calculadoraconversor.com/tangente/)

> Determinando o ângulo

$$ \alpha  = arc~tg~(-0,5773503) = -30°.$$

> <p align="justify">-30° é o ângulo formado, em relação à horizontal, no momento em que o projétil chega ao chão.</p>

<p align="justify">Link para auxílio no cálculo do arco tangente (use números com vírgula):</p>

[Calculadora on-line de arco tangente.](https://www.calculadoraconversor.com/arcotangente/)

> <p align="justify">Comandos no R para determinar a direção do projétil, em relação à horizontal, ao atingir o solo:</p>

<p align="justify">No R, o comando "atan(núm)" retorna a tangente inversa (arco tangente) de um número. O ângulo retornado é fornecido em radianos no intervalo -pi/2 a pi/2. Para expressar o arco tangente em graus é necessário  multiplicar o resultado por 180/pi ou dividí-lo por pi/180. Exemplo: queremos saber qual é o ângulo cuja tangente é igual a 1. Colocamos o 1 indexado no comando atan e o atribuímos a uma variável qualquer, assim:</p> 

```{r}
x <- atan(1) *  180/pi
x

45
```
ou assim:

```{r}
y <- atan(1) /(pi/180)
y

45
```
<p align="justify">45° é o ângulo procurado.</p>

<p align="justify">No problema inicial os comandos no R podem ficar nesse formato:</p>

```{r}
# vx e vy já calculados:
vx <-  43.30127
vy <- -25
# Atribuir valor vy/vx:
tang <- vy/vx
# Atribuir valor arco tg
angulo <- atan(tang)
# Atribuir valor angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar tang
tang
# Mostrar graus
graus

tang
-0.5773503
graus
-30
```
<p align="justify">Portanto, o ângulo cuja tangente é igual a -0,57735031 equivale a -30°.</p>
<center><div class="exerc">EXERCÍCIO PROPOSTO</div></center>
* <p align="justify"> Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Determine o ângulo (direção) formado, em relação à horizontal, no momento em que o projétil chega ao solo. Considere $g = 9,8~m/s^{2}$. A $v _{x} = 25 m/s$ e a $v _{y} = -53~m/s$ já foram determinados anteriormente.</p>
*** =instructions
<p align="justify"> - Você irá escrever a expressão que calcula a direção ou ângulo formado em relação à horizontal, no momento em que o projétil chega ao chão, atribuindo-a a uma variável.</p>

*** =hint
<p align="justify"> A direção ou ângulo formado em relação à horizontal, no momento em que o projétil chega ao chão, pode ser obtido pela seguinte expressão:</p> 
$$\theta = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# vx:
vx <- 25
# vy:
vy <- -53
# Escreva vy/vx numa variável:
tang <- 
# Atribuir valor arco tg
angulo <- atan(tang)
# Atribuir valor angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar graus
graus
```
*** =solution
```{r}
# vx:
vx <- 25
# vy:
vy <- -53
# Escreva vy/vx numa variável:
tang <- vy/vx
# Atribuir valor arco tg
angulo <- atan(tang)
# Atribuir valor angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar graus
graus
```
*** =sct
```{r}
test_output_contains ("-64.74684", incorrect_msg = "Escreva a expressão que atribua a uma variável (tang) a divisão entre as componentes vertical e horizontal da velocidade do projétil quando o mesmo alcança o tempo de trajeto.")
success_msg ("Bom trabalho! Você aprendeu a determinar a direção de um projétil quando o mesmo alcança o solo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:06f6447360
## Atividade - Direção do projétil
<style type="text/css">
.exerc{
background-color:#33a0c2; font-weight: bold; font-size:20px; color:#ffffff; text-align:center;
}
</style>
<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Determine: a) A altura máxima desenvolvida pelo projétil; b) O tempo gasto para chegar na altura máxima; c) O alcance desenvolvido pelo projétil; d) A velocidade da componente vertical, a velocidade resultante e a direção do projétil ao alcançar o solo; e) A posição do projétil no tempo de 5 segundos. Compare sua resposta logo abaixo.</p>

```{r}
# Acel. gravidade:
g <- 9.8
# vi:
vi <- 50
# Ângulo em graus:
angulo <- 60
# Graus em rad:
teta <- (pi/180) * angulo
# vix:
vix <- vi * cos(teta)
# viy:
viy <- vi * sin(teta)
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo de subida:
thmax <- viy/g
# tempo trajeto:
ttot = 2 * thmax
# alcance:
A = vix * ttot
# Tempo dado:
t = 5
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2
# vx = vix:
vx <- vix
# vy:
vy <- viy - g * ttot 
# vr:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Atribuir vy/vx a:
tang <- vy/vx
# Atribuir arc tg a:
angulo <- atan(tang)
# Atribuir angulo/(pi/180) a:
graus <- angulo/(pi/180)
cat("a) A hmax é", hmax)
cat("b) O thmax é", thmax)
cat("c) O alcance é", A)
cat("d) vy:", vy, "vr:", vr, "direção:", graus)
cat("e) A posição em 5s é", X, "e", Y)
```
> Compare sua resposta 

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  a) A hmax é 95.66327;<br>  b) O thmax é 4.418497;<br>  c) O alcance é 220.9248;<br>  d) vy: -43.30127, vr: 50, direção: -60; <br>  e) A posição em 5s é 125 e 94.00635.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes vx, vy e a direção do projétil ao chegar no solo. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Calcule a direção do projétil no tempo de trajeto. Você irá atribuir vy/vx a uma variável, escrevendo no código.</p>

*** =hint
<p align="justify"> A direção ou ângulo formado em relação à horizontal no momento em que o projétil chega ao chão, pode ser obtido pela seguinte expressão:</p> 
$$\theta = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Acel. gravidade:
g <- 9.8
# vi:
vi <- 200
# Ângulo graus:
angulo <- 60
# Graus em rad:
teta <- (pi/180) * angulo
# vix:
vix <- vi * cos(teta)
# viy:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo trajeto:
ttot = 2 * thmax
# vy:
vy <- viy - g * ttot
# Escreva atribuindo vy/vx a:
tang <- 
# Atribuir arc tg a:
angulo <- atan(tang)
# Atribuir angulo/(pi/180) a:
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =solution
```{r}
# Acel. gravidade:
g <- 9.8
# vi:
vi <- 200
# Ângulo graus:
angulo <- 60
# Graus em rad:
teta <- (pi/180) * angulo
# vix:
vix <- vi * cos(teta)
# viy:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo trajeto:
ttot = 2 * thmax
# vy:
vy <- viy - g * ttot
# Escreva atribuindo vy/vx a:
tang <- vy/vx
# Atribuir arc tg a:
angulo <- atan(tang)
# Atribuir angulo/(pi/180) a:
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =sct
```{r}
test_output_contains ("-60", incorrect_msg = "Escreva a expressão que atribua a uma variável (tang) a divisão entre as componentes vertical e horizontal da velocidade do projétil quando o mesmo alcança o tempo de trajeto.")
success_msg ("Bom trabalho! Você aprendeu mais sobre como determinar a direção do projétil quando o mesmo alcança o solo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:dee61a2620
## Explorando dados dos eixos X e Y

<p align="justify"> A equação do MRU que fornece o espaço inicial e final para um móvel num instante t, segundo o eixo horizontal (X), é dada por </p>

$$\Delta X= X - x _{i} =v _{ix}.t \rightarrow X= x _{i} + v _{ix}.t$$

<p align="justify">onde, $\Delta X$ representa a variação do espaço no eixo X; $X$ corresponde ao espaço final; $x _{i}$ representa o espaço inicial (no caso, será na origem do gráfico e igual a zero); $v _{ix}$ é constante e corresponde à componente da velocidade no eixo X e o t representa o tempo dado.</p>

<p align="justify"> Quando $x _{i}=0$, a equação acima torna-se</p> 

$$X= v _{ix}.t.$$

<p align="justify">Para depois plotarmos o gráfico do movimento oblíquo, precisaremos isolar o tempo t na equação acima. Portanto, temos que</p> 

$$t = \displaystyle \frac{X - x_{i}}{v _{ix}}\cdot$$

<p align="justify"> A equação do MRUV que fornece a altura inicial e final para um móvel num instante t, segundo o eixo vertical (Y), é dada por </p>

$$\Delta Y= Y - y _{i} = v _{ix}.t - \displaystyle \frac{g.t^{2}}{2} \rightarrow$$
$$Y =  y _{i} + v _{ix}.t - \displaystyle \frac{g.t^{2}}{2}\cdot$$

<p align="justify">onde, $\Delta Y$ representa a variação da altura (no eixo Y); $Y$ corresponde à altura final; $y _{i}$ corresponde a altura inicial (no caso, será na origem do gráfico e igual a zero); $v _{iy}$ corresponde à componente da velocidade no eixo Y e o t corresponde ao tempo dado.</p> 

<p align="justify"> Quando $y _{i}=0$, a equação acima torna-se</p> 

$$Y= v _{ix}.t - \displaystyle \frac{g.t^{2}}{2}\cdot$$

> Valores do eixo X (Distância horizontal)

* <p align="justify">Um projétil é lançado a  partir do solo com uma velocidade inicial de 50m/s formando com o mesmo um ângulo de 30°. Determine e analise os valores das distâncias (coordenadas X) e as alturas (coordenadas Y) do projétil a cada 2,209248 m de distância horizontal a partir de onde onde foi lançado (de 0 m) até o alcance (A = 220,9248 m). Considere $g = 9,8~m/s^{2}$.</p>

```{r}
# Acel. gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# Velocidade inicial:
vi <- 50
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
#Mostrar o eixo X
X
```

```{r}
# correto
# Acel. gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# Tempo da hmax
thmax <- viy/g
# Tempo trajeto
ttotal <- 2 * thmax
# Alcance
A <- vx * ttotal
# Espaço inicial:
xi <- 0
# Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# O tempo na eq. MRU:
tempo <- (X - xi)/vx
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
#Mostrar valores eixo X
X
#Mostrar valores eixo y
Y
# Mínimo no Y
min(Y)
# Maximo no Y
max(Y)
# Mínimo no X
min(X)
# Maximo no X
max(X)
# Escreva X na hmax
X[c(51)] 
# Escreva Y na hmax
Y[c(51)]
```

<p style="font-family = Arial; font-size: 12px; text-align:left">[1] <font color="##FF0000">0.000000</font>   2.209248   4.418496   6.627744   8.836992  11.046240  13.255488  15.464736  17.673984</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[10]  19.883232  22.092480  24.301728  26.510976  28.720224  30.929472  33.138720  35.347968  37.557216</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[19]  39.766464  41.975712  44.184960  46.394208  48.603456  50.812704  53.021952  55.231200  57.440448</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[28]  59.649696  61.858944  64.068192  66.277440  68.486688  70.695936  72.905184  75.114432  77.323680</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[37]  79.532928  81.742176  83.951424  86.160672  88.369920  90.579168  92.788416  94.997664  97.206912</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[46]  99.416160 101.625408 103.834656 106.043904 108.253152 <font color="##FF0000">110.462400</font> 112.671648 114.880896 117.090144</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[55] 119.299392 121.508640 123.717888 125.927136 128.136384 130.345632 132.554880 134.764128 136.973376</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[64] 139.182624 141.391872 143.601120 145.810368 148.019616 150.228864 152.438112 154.647360 156.856608</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[73] 159.065856 161.275104 163.484352 165.693600 167.902848 170.112096 172.321344 174.530592 176.739840</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[82] 178.949088 181.158336 183.367584 185.576832 187.786080 189.995328 192.204576 194.413824 196.623072</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[91] 198.832320 201.041568 203.250816 205.460064 207.669312 209.878560 212.087808 214.297056 216.506304</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[100] 218.715552 <font color="##FF0000">220.924800</font></p>

<p align="justify"> Observe que o projétil partiu de zero metro (espaço inicial) até um alcance máximo de 220,924800m (espaço final). Programamos para o R executar na sequência de 2,209248m em 2,209248m até chegar no alcance máximo.</p>

> Comandos para explorar os valores de X

<p align="justify"> Muitas informações podem ser extraídas dos valores do eixo horizontal. Veja algumas:</p>

```{r}
# Extrai o valor nº 51 do eixo X
# Metade do alcance 
X[c(51)]
110.4624

# Extrai de X os valores
# de nºs 49, 50, 51
X[c(49, 50, 51)]
106.0439 108.2532 110.4624

# Extrai de X os valores
# de 51 a 53
X[c(51:53)]   
110.4624 112.6716 114.8809

# Maior valor no X:
max(X)
220.9248

# Menor valor no X:
min(X) 
0

# Menor e maior valor X:
range(X) 
0.0000 220.9248

# Soma elementos de X:
sum(X)
11156.7

# Variação entre cada elemento
# (constante)
diff(X)
[1]  2.209248 2.209248... 
[12] 2.209248 2.209248... 

# Média: 
 mean(X) 
110.4624
```
> Valores do eixo Y (Distância vertical)

```{r}
# Acel.gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# # Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# Velocidade inicial:
vi <- 50
vi <- 50
# Ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar o eixo X
X
# Mostrar o eixo Y
Y
```

```{r}
# Correto
# Acel. gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# Tempo da hmax
thmax <- viy/g
# Tempo trajeto
ttotal <- 2 * thmax
# Alcance
A <- vx * ttotal
# Espaço inicial:
xi <- 0
# Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# O tempo na eq. MRU:
tempo <- (X - xi)/vx
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
#Mostrar valores eixo X
X
#Mostrar valores eixo y
Y
# Mínimo no Y
min(Y)
# Maximo no Y
max(Y)
# Mínimo no X
min(X)
# Maximo no X
max(X)
# Escreva X na hmax
X[c(51)] 
# Escreva Y na hmax
Y[c(51)]
```

<p style="font-family = Arial; font-size: 12px; text-align:left">[1]  <font color="##FF0000">0.000000e+00</font> 1.262755e+00 2.499999e+00 3.711734e+00 4.897958e+00 6.058672e+00 7.193876e+00 8.303570e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[9]  9.387753e+00 1.044643e+01 1.147959e+01 1.248724e+01 1.346939e+01 1.442602e+01 1.535714e+01 1.626275e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[17] 1.714285e+01 1.799745e+01 1.882653e+01 1.963010e+01 2.040816e+01 2.116071e+01 2.188775e+01 2.258928e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[25] 2.326530e+01 2.391581e+01 2.454081e+01 2.514030e+01 2.571428e+01 2.626275e+01 2.678571e+01 2.728316e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[33] 2.775510e+01 2.820153e+01 2.862245e+01 2.901785e+01 2.938775e+01 2.973214e+01 3.005102e+01 3.034439e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[41] 3.061224e+01 3.085459e+01 3.107143e+01 3.126275e+01 3.142857e+01 3.156888e+01 3.168367e+01 3.177296e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[49] 3.183673e+01 3.187500e+01 <font color="##FF0000">3.188776e+01</font> 3.187500e+01 3.183674e+01 3.177296e+01 3.168367e+01 3.156888e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[57] 3.142857e+01 3.126276e+01 3.107143e+01 3.085459e+01 3.061225e+01 3.034439e+01 3.005102e+01 2.973215e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[65] 2.938776e+01 2.901786e+01 2.862245e+01 2.820154e+01 2.775511e+01 2.728317e+01 2.678572e+01 2.626276e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[73] 2.571429e+01 2.514032e+01 2.454083e+01 2.391583e+01 2.326532e+01 2.258930e+01 2.188777e+01 2.116073e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[81] 2.040818e+01 1.963012e+01 1.882655e+01 1.799746e+01 1.714287e+01 1.626277e+01 1.535716e+01 1.442604e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[89] 1.346941e+01 1.248726e+01 1.147961e+01 1.044645e+01 9.387776e+00 8.303594e+00 7.193900e+00 6.058697e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[97] 4.897984e+00 3.711760e+00 2.500026e+00 1.262782e+00 <font color="##FF0000">2.765749e-05</font></p>

<p align="justify">De acordo com os dados acima, a altura máxima corresponde a</p> 

$$3,188776e+01m$$ 
$$= 3,188776.10^{1}m$$
$$= 3,188776.10m$$ 
$$= 31,88776m.$$

<p align="justify"> Observe que o projétil partiu de zero metro (altura inicial) até uma altura máxima de 31.88776m (altura final) e depois retorna para a origem, que na simulação tende a zero (2,765749e-05m = 0,00002765749m).</p>

> Comandos para explorar os valores de Y

<p align="justify"> Muitas informações podem ser extraídas dos valores do eixo vertical, inclusive as posições (X, Y). Veja algumas:</p>

```{r}
# Extrai as posições X,Y
> X[c(51)]; Y[c(51)]
110.4624
 31.88776

# Extrai valor nº 51 eixo Y
# Altura máxima
Y[c(51)]
31.88776

# Extrai de Y os valores
# de nºs 49, 50, 51
Y[c(49, 50, 51)]
31.83673 31.87500 31.88776

# Extrai de Y os valores
# de 51 a 53 - começo da descida
Y[c(51:53)]
31.88776 31.87500 31.83674

# Conjunto de posições X,Y
X[c(49, 50, 51, 52)]; Y[c(49, 50, 51, 52)]
106.0439 108.2532 110.4624 112.6716
 31.83673 31.87500 31.88776 31.87500
 
# Posições X,Y de chegada
X[c(99, 100, 101)]; Y[c(99, 100, 101)]
216.5063 218.7156 220.9248
2.500026e+00 1.262782e+00 2.765749e-05

# Maior valor no Y:
max(Y) 
31.88776

# Menor valor no Y:
min(Y) 
0

# Menor e maior valor:
range(Y) 
0.00000 31.88776

# Soma elementos de Y:
sum(Y)
2125.638

# Variação cada elemento
## (Não constante)
diff(Y)
[1]  1.26275483  1.23724464...   
[9]  1.05867329  1.03316309...  

# Média: 
mean(Y) 
21.04592
```
<p align="justify">Observe que o valor de X correspondente na altura máxima equivale a 110,4624 m, a metade do alcance (A = 220,9248m). Observe também o valor de Y que corresponde à altura máxima (31.88776).</p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil com uma velocidade inicial igual a 100 m/s é lançado a partir do solo, formando com o mesmo um ângulo de 45°. Particione o alcance máximo (1020,408m), numa sequência de 1,020408m em 1,020408m, escrevendo um comando que indique a posição do projétil na altura máxima (correspondende à metade do alcance máximo). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>

*** =instructions
<p align="justify"> - Gere os dados dos eixos X e Y e observe o valor da altura máxima no eixo Y.</p>
<p align="justify"> - Escreva um comando que mostre o valor no eixo Y da altura máxima.</p>
*** =hint
<p align="justify"> - Veja quem é o elemento nos valores do eixo Y de número 501.</p> 
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Acel. gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# Tempo da hmax
thmax <- viy/g
# Tempo trajeto
ttotal <- 2 * thmax
# Alcance
A <- vx * ttotal
# Espaço inicial:
xi <- 0
# Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# O tempo na eq. MRU:
tempo <- (X - xi)/vx
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
#Mostrar valores eixo X
X
#Mostrar valores eixo y
Y
# Mínimo no Y
min(Y)
# Maximo no Y
max(Y)
# Mínimo no X
min(X)
# Maximo no X
max(X)
# Escreva X na hmax
X[c(51)] 
# Escreva Y na hmax

```
*** =solution
```{r}
# Acel. gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# Tempo da hmax
thmax <- viy/g
# Tempo trajeto
ttotal <- 2 * thmax
# Alcance
A <- vx * ttotal
# Espaço inicial:
xi <- 0
# Sequência 0 até Alcance variando de 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# O tempo na eq. MRU:
tempo <- (X - xi)/vx
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
#Mostrar valores eixo X
X
#Mostrar valores eixo y
Y
# Mínimo no Y
min(Y)
# Maximo no Y
max(Y)
# Mínimo no X
min(X)
# Maximo no X
max(X)
# Escreva X na hmax
X[c(51)] 
# Escreva Y na hmax
Y[c(51)]
```{r}
*** =sct
```{r}
test_output_contains ("255.102", incorrect_msg = "Escreva a expressão que mostre o valor da altura máxima atingida pelo projétil.")
success_msg ("Bom trabalho! Você aprendeu a analisar os valores dos eixos correspondentes à Altura e ao Alcance máximo de um projétil no movimento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:3f42c2369a
## Atividade - Explorando dados dos eixos X e Y

color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Particione o alcance máximo (3534,798m), numa sequência de 3,534798m em 3,534798m, escrevendo um comando que indique a posição do projétil na altura máxima (correspondende à metade do alcance máximo). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Gere os dados dos eixos X e Y e observe a altura máxima no eixo Y.</p>
<p align="justify"> - Escreva um comando que mostre o valor de Y na altura máxima.</p>
*** =hint
<p align="justify"> - Veja quem é o elemento nos valores do eixo Y de número 501.</p> 
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da O alcance é gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 3534.798, by = 3.534798)
# Velocidade inicial:
vi <- 200
# ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar eixo X
X
# Mostrar eixo Y
Y
# Escreva X na hmax
X[c(501)] 
# Escreva Y na hmax

```
*** =solution
```{r}
# Aceleração da O alcance é gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 3534.798, by = 3.534798)
# Velocidade inicial:
vi <- 200
# ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar eixo X
X
# Mostrar eixo Y
Y
# Escreva X na hmax
X[c(501)] 
# Escreva Y na hmax
Y[c(501)]
```
*** =sct
```{r}
test_output_contains ("1530.612", incorrect_msg = "Escreva a expressão que mostre o valor da altura máxima atingida pelo projétil.")
success_msg ("Bom trabalho! Você aprendeu a analisar os valores dos eixos da Altura e Alcance máximo do movimento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:700f8dfafd
## Explorando dados das componentes

<p align="justify"> A equação do MRU que fornece o espaço inicial e final para um móvel num instante t, segundo o eixo horizontal (X), é dada por </p>

$$\Delta X= X - x _{i} =v _{ix}.t \rightarrow X= x _{i} + v _{ix}.t$$

<p align="justify">onde, $\Delta X$ representa a variação do espaço (no eixo X); $X$ corresponde ao espaço final; $x _{i}$ representa o espaço inicial (no caso, será na origem do gráfico e igual a zero); $v _{ix}$ é constante e corresponde à componente da velocidade no eixo X e o t representa o tempo dado.</p>

<p align="justify"> Quando $x _{i}=0$, a equação acima torna-se</p> 

$$X= v _{ix}.t.$$

<p align="justify">Para plotarmos o gráfico precisaremos isolar o tempo t. Portanto, da primeira equação temos que</p> 

$$t = \frac{X - x_{i}}{v _{ix}}.$$

<p align="justify"> A equação do MRUV que fornece a altura inicial e final para um móvel num instante t, segundo o eixo vertical (Y), é dada por </p>

$$\Delta Y= Y - y _{i} = v _{ix}.t - \displaystyle \frac{g.t^{2}}{2} \rightarrow$$
$$Y =  y _{i} + v _{ix}.t - \displaystyle \frac{g.t^{2}}{2}\cdot$$

<p align="justify">onde, $\Delta Y$ representa a variação da altura (no eixo Y); $Y$ corresponde à altura final; $y _{i}$ corresponde a altura inicial (no caso, será na origem do gráfico e igual a zero); $v _{iy}$ corresponde à componente da velocidade no eixo Y e o t corresponde ao tempo dado.</p> 

<p align="justify"> Quando $y _{i}=0$, a equação acima torna-se</p> 

$$Y= v _{ix}.t - \displaystyle \frac{g.t^{2}}{2}\cdot$$

> Valores da componente vy

```{r}
# Aceleração da gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# Velocidade inicial:
vi <- 50
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar o eixo X
X
# Mostrar o eixo Y
Y
# Mostrar vx
vx
43.30127
# Mostrar vy
vy
```
<p style="font-family = Arial; font-size: 12px; text-align:left">
[1]  <font color="##FF0000">2.500000e+01</font> 2.450000e+01  2.400000e+01  2.350000e+01  2.300000e+01  2.250000e+01  2.200000e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[8]  2.150000e+01  2.100000e+01  2.050000e+01  2.000000e+01  1.950000e+01  1.900000e+01  1.850000e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[15] 1.800000e+01  1.750000e+01  1.700000e+01  1.650000e+01  1.600000e+01  1.550000e+01  1.500000e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[22] 1.450000e+01  1.400000e+01  1.350000e+01  1.300000e+01  1.250000e+01  1.200000e+01  1.150000e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[29] 1.100000e+01  1.050000e+01  1.000000e+01  9.500003e+00  9.000003e+00  8.500004e+00  8.000004e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[36] 7.500004e+00  7.000004e+00  6.500004e+00  6.000004e+00  5.500004e+00  5.000004e+00  4.500004e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[43] 4.000005e+00  3.500005e+00  3.000005e+00  2.500005e+00  2.000005e+00  1.500005e+00  1.000005e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[50] 5.000053e-01  <font color="##FF0000">5.420870e-06</font> -4.999945e-01 -9.999944e-01 -1.499994e+00 -1.999994e+00 -2.499994e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[57]-2.999994e+00 -3.499994e+00 -3.999994e+00 -4.499994e+00 -4.999993e+00 -5.499993e+00 -5.999993e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[64]-6.499993e+00 -6.999993e+00 -7.499993e+00 -7.999993e+00 -8.499993e+00 -8.999993e+00 -9.499993e+00</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[71]-9.999992e+00 -1.049999e+01 -1.099999e+01 -1.149999e+01 -1.199999e+01 -1.249999e+01 -1.299999e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[78]-1.349999e+01 -1.399999e+01 -1.449999e+01 -1.499999e+01 -1.549999e+01 -1.599999e+01 -1.649999e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[85]-1.699999e+01 -1.749999e+01 -1.799999e+01 -1.849999e+01 -1.899999e+01 -1.949999e+01 -1.999999e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[92]-2.049999e+01 -2.099999e+01 -2.149999e+01 -2.199999e+01 -2.249999e+01 -2.299999e+01 -2.349999e+01</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[99]-2.399999e+01 -2.449999e+01 <font color="##FF0000">-2.499999e+01</font></p>

> Componentes da velocidade

<p align="justify">A componente vx = vix é constante (43,30127 m/s). A velocidade da componente vy varia de uma maneira constante, pois faz parte de um MRUV. Vamos analisar os valores de vy.</p> 

<p align="justify"> Nessa simulação, a velocidade da componente na vertical, vy, na partida equivale a</p> 
$$2,500000e+01$$ 
$$= 2,500000.10^{1}$$
$$= 2,500000.10$$ 
$$= 25,000000$$ 
$$= 25m/s$$ 
<p align="justify"> e na altura máxima sua velocidade tende a zero (0,00000542087m/s). Na chegada ao solo, equivale a -24,99999m/s. Praticamente, é o mesmo valor da velocidade de saída, porém, com sinal contrário.</p>

> Comandos para explorar os valores de vy

<p align="justify"> Muitas informações podem ser extraídas dos valores das componentes da velocidade. Veja algumas:</p>

```{r}

# Extrai de vy 3 valores
# de partida e de 
vy[c(1,2,3)]
25.0 24.5 24.0
# chegada - compará-las
vy[c(101,100,99)]
-24.99999 -24.49999 -23.99999

# Extrai de vy os valores
# de 48 a 52
vy[c(48:52)]   
1.500005e+00  1.000005e+00  5.000053e-01  
5.420870e-06 -4.999945e-01

# Maior valor vy:
max(vy) 
25
# Menor valor vy:
min(vy)
-24.99999

# Variação entre cada elemento
# (constante)
diff(vy)
[1] -0.4999999 -0.4999999... 
[10]-0.4999999 -0.4999999... 
```
> Valores da vr

```{r}
# Aceleração da gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# Velocidade inicial:
vi <- 50
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * t ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar eixo X
X
# Mostrar eixo Y
Y
# Mostrar vx
vx
43.30127
# Mostrar vy
vy
# Mostrar vr
vr
```
<p style="font-family = Arial; font-size: 12px; text-align:left">
[1]<font color="##FF0000"> 50.00000 </font>49.75188 49.50758 49.26713 49.03060 48.79805 48.56954 48.34511 48.12484 47.90877 47.69696</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[12] 47.48947 47.28636 47.08768 46.89350 46.70385 46.51881 46.33843 46.16276 45.99185 45.82576 45.66454</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[23] 45.50824 45.35692 45.21062 45.06939 44.93328 44.80234 44.67662 44.55615 44.44097 44.33114 44.22669</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[34] 44.12766 44.03408 43.94599 43.86343 43.78641 43.71499 43.64917 43.58899 43.53447 43.48563 43.44249</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[45] 43.40507 43.37338 43.34743 43.32724 43.31282 43.30416 <font color="##FF0000">43.30127</font> 43.30416 43.31282 43.32724 43.34743</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[56] 43.37338 43.40507 43.44249 43.48563 43.53447 43.58899 43.64917 43.71499 43.78641 43.86342 43.94599</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[67] 44.03408 44.12765 44.22669 44.33114 44.44097 44.55614 44.67661 44.80234 44.93328 45.06939 45.21062</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[78] 45.35692 45.50824 45.66453 45.82575 45.99184 46.16275 46.33843 46.51881 46.70385 46.89349 47.08768</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[89] 47.28636 47.48947 47.69696 47.90876 48.12483 48.34511 48.56953 48.79805 49.03060 49.26712 49.50757</p>
<p style="font-family = Arial; font-size: 12px; text-align:left">
[100]49.75188 <font color="##FF0000">49.99999</font></p>

<p align="justify">Observe que o valor da velocidade resultante na saída e na chegada é o mesmo. A velocidade resultante na altura máxima é o mesmo valor da componente vix (43,30127 ), já que a vy é nula neste ponto. A velocidade resultante é sempre positiva. Muitas informações podem ser extraídas dos valores das componentes da velocidade. Veja algumas:</p>

```{r}
# Extrai da vr 3 valores
# de partida 
vr[c(1,2,3)]
50.00000 49.75188 49.50758
# E de chegada - compará-las
vr[c(101,100,99)]
49.99999 49.75188 49.50757
 
# Extrai de vr os valores
# de 48 a 52
vr[c(48:51)]   
43.32724 43.31282 43.30416 43.30127

# Maior valor de vr:
max(vr)
50

# Menor valor de vr
# - na altura máxima:
min(vr)
43.30127

# Variação entre cada elemento
# (não constante)
diff(vr)
[1] -0.248115560 -0.244309157... 
[9] -0.216070158 -0.211807357...
```

> fAZER A PARTIR DAQUI - DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Sendo que o alcance máximo acontece quando o ângulo de lançamento é equivalente a 45°, prove que esse alcance máximo (A) é quatro vezes maior que a altura máxima (hmáx). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>

```{r}
Aceleração da gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# componente vix:
vix <- vi * cos(teta)
# componente viy:
viy <- vi * sin(teta) 
# Tempo na thmax:
thmax <- viy/g
# tempo total:
ttot = 2 * thmax
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# alcance
A = vix * ttot
cat("A altura máxima é", hmax)
cat("O alcance é", A)
cat(A, "é 4 vezes", hmax)
```
> Compare sua resposta 

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  a) A hmax é 95.66327;<br>  b) O thmax é 4.418497;<br>  c) O alcance é 220.9248;<br>  d) vy: -43.30127, vr: 50, direção: -60; <br>  e) A posição em 5s é 125 e 94.00635.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes vx, vy e a direção do projétil ao chegar no solo. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Calcule a direção do projétil no tempo de trajeto. Você irá atribuir vy/vx a uma variável.</p>
<p align="justify"> - Leia todo o código do exercício e escreva a atribuição à variável.</p>
*** =hint
<p align="justify"> A direção ou ângulo formado em relação à horizontal, no momento em que o projétil chega ao chão, pode ser obtido pela seguinte expressão:</p> 
$$\theta = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em rad:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo tot de trajeto:
ttot = 2 * thmax
# Componente vertical de v:
vy <- viy - g * ttot
#Atribuir vy/vx a uma variável
tang <- 
# Atribuir valor do arc tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em rad:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo tot de trajeto:
ttot = 2 * thmax
# Componente vertical de v:
vy <- viy - g * ttot
#Atribuir vy/vx a uma variável
tang <- vy/vx
# Atribuir valor do arc tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =sct
```{r}
test_output_contains ("-60", incorrect_msg = "Escreva a expressão que atribua a uma variável (tang) a divisão entre as componentes vertical e horizontal da velocidade do projétil quando o mesmo alcança o tempo de trajeto.")
success_msg ("Bom trabalho! Você aprendeu a determinar a direção do projétil quando o mesmo alcança o solo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:cf63ed39fd
## Explorando dados do tempo

<p align="justify">Sabemos que um corpo está em movimento uniforme quando o mesmo percorre espaços iguais em intervalos de tempos iguais. O movimento do projétil no eixo X é constante, ou seja, a componente da velocidade inicial vix, que também é igual à componente da velocidade vx, é constante. Foi programado no R para que os espaços fossem divididos de 2,209248m em 2,209248m até atingir o alcance máximo de 220,9248m. Foram obtidos intervalos de tempos iguais, dividindo cada 2,209248m pelo valor da componente vix (43,30127m/s) que resultou em 0,0510204s. Vejamos o código:</p> 

```{r}
# Aceleração da gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 220.9248, by = 2.209248)
# Velocidade inicial:
vi <- 50
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
# Componente viy:
viy <- vi * sin(teta)
# O tempo na eq. MRU:
tempo <- (X - xi)/vix
# Posição X
X <- vix * tempo
# Posição Y
Y <- viy * tempo - (g * tempo ^ 2)/2 
# Componente vertical de v:
vy <- viy - g * tempo 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar o eixo X
X
# Mostrar o eixo Y
Y
# Mostrar vx
vx
43.30127
# Mostrar vy
vy
# Mostrar vr
vr
# Mostrar tempo
tempo
```
<p align="justify">Isso gerou os seguintes valores:</p>

> Valores do tempo

<p style="font-family = Arial; font-size: 12px; text-align:left">[1] <font color="##FF0000">0.0000000</font> 0.0510204 0.1020408 0.1530612 0.2040816 0.2551020 0.3061224 0.3571428 0.4081632 0.4591836<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[11] 0.5102040 0.5612244 0.6122448 0.6632652 0.7142856 0.7653060 0.8163264 0.8673468 0.9183671 0.9693875<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[21] 1.0204079 1.0714283 1.1224487 1.1734691 1.2244895 1.2755099 1.3265303 1.3775507 1.4285711 1.4795915<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[31] 1.5306119 1.5816323 1.6326527 1.6836731 1.7346935 1.7857139 1.8367343 1.8877547 1.9387751 1.9897955<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[41] 2.0408159 2.0918363 2.1428567 2.1938771 2.2448975 2.2959179 2.3469383 2.3979587 2.4489791 2.4999995<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[51] <font color="##FF0000">2.5510199</font> 2.6020403 2.6530606 2.7040810 2.7551014 2.8061218 2.8571422 2.9081626 2.9591830 3.0102034<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[61] 3.0612238 3.1122442 3.1632646 3.2142850 3.2653054 3.3163258 3.3673462 3.4183666 3.4693870 3.5204074<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[71] 3.5714278 3.6224482 3.6734686 3.7244890 3.7755094 3.8265298 3.8775502 3.9285706 3.9795910 4.0306114<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[81] 4.0816318 4.1326522 4.1836726 4.2346930 4.2857134 4.3367338 4.3877542 4.4387745 4.4897949 4.5408153<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[91] 4.5918357 4.6428561 4.6938765 4.7448969 4.7959173 4.8469377 4.8979581 4.9489785 4.9999989 5.0510193<p>
<p style="font-family = Arial; font-size: 12px; text-align:left">[101] <font color="##FF0000">5.1020397</font><p>

<p align="justify"> Baseado nos dados de vy, vr e tempo, observe que na altura máxima atingida pelo projétil, o tempo chega a 2,5510199s e a componente da velocidade, vy, tende a zero (0,00000542087m/s). Na chegada do projétil ao solo, a componente da velocidade vy tende a -25m/s (-24,99999m/s) e a velocidade resultante tende a 50 m/s (49,99999), isso quando completa o tempo de trajeto de 5,1020397s.</p>

> Comandos para explorar os valores do tempo

<p align="justify"> Muitas informações podem ser extraídas dos valores do tempo. Veja algumas:</p>

```{r}
# Extrai de tempo 3 valores
# de partida
tempo[c(1,2,3)]
0.0000000 0.0510204 0.1020408

# 3 valores de chegada
tempo[c(99, 100, 101)]
4.999999 5.051019 5.102040

# Extrai de tempo os valores
# de 50 a 52
tempo[c(50,51,52)]
2.499999 2.551020 2.602040

# Maior valor tempo:
max(tempo) 
5.1020425

# Variação entre cada elemento
# (constante)
diff(tempo)
[1] 0.0510204 0.0510204... 
[11] 0.0510204 0.0510204... 
 
# Resumo estatístico tempo:
summary(tempo)
Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
0.000   1.276   2.551   2.551   3.827   5.102 
```

> fAZER A PARTIR DAQUI - DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Sendo que o alcance máximo acontece quando o ângulo de lançamento é equivalente a 45°, prove que esse alcance máximo (A) é quatro vezes maior que a altura máxima (hmáx). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>

```{r}
Aceleração da gravidade:
g <- 9.8
# Velocidade inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# componente vix:
vix <- vi * cos(teta)
# componente viy:
viy <- vi * sin(teta) 
# Tempo na thmax:
thmax <- viy/g
# tempo total:
ttot = 2 * thmax
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# alcance
A = vix * ttot
cat("A altura máxima é", hmax)
cat("O alcance é", A)
cat(A, "é 4 vezes", hmax)
```
> Compare sua resposta 

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  a) A hmax é 95.66327;<br>  b) O thmax é 4.418497;<br>  c) O alcance é 220.9248;<br>  d) vy: -43.30127, vr: 50, direção: -60; <br>  e) A posição em 5s é 125 e 94.00635.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes vx, vy e a direção do projétil ao chegar no solo. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Calcule a direção do projétil no tempo de trajeto. Você irá atribuir vy/vx a uma variável.</p>
<p align="justify"> - Leia todo o código do exercício e escreva a atribuição à variável.</p>
*** =hint
<p align="justify"> A direção ou ângulo formado em relação à horizontal, no momento em que o projétil chega ao chão, pode ser obtido pela seguinte expressão:</p> 
$$\theta = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em rad:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo tot de trajeto:
ttot = 2 * thmax
# Componente vertical de v:
vy <- viy - g * ttot
#Atribuir vy/vx a uma variável
tang <- 
# Atribuir valor do arc tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em rad:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta)
# vx = vix
vx <- vix
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo tot de trajeto:
ttot = 2 * thmax
# Componente vertical de v:
vy <- viy - g * ttot
#Atribuir vy/vx a uma variável
tang <- vy/vx
# Atribuir valor do arc tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar vy:
vy
# Mostrar vx:
vx
# Mostrar direção:
graus
```
*** =sct
```{r}
test_output_contains ("-60", incorrect_msg = "Escreva a expressão que atribua a uma variável (tang) a divisão entre as componentes vertical e horizontal da velocidade do projétil quando o mesmo alcança o tempo de trajeto.")
success_msg ("Bom trabalho! Você aprendeu a determinar a direção do projétil quando o mesmo alcança o solo.")
```