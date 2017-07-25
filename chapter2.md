--- 
title_meta  : Capítulo 2
title       : Projeto - Lançamento Oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:8ea80fa0d0
## Componentes da velocidade inicial

<p align="justify">Um corpo lançado obliquamente possui dois tipos de movimentos: um segundo a horizontal e o outro segundo a vertical. O movimento descrito pelo corpo, lançado segundo a horizontal, é do tipo MRU (Movimento Retilíneo Uniforme). E o outro movimento descrito pelo corpo, lançado segundo a vertical, é do tipo MRUV (Movimento Retilíneo Uniformemente Variado). A trajetória descrita pelo corpo terá a forma parabólica.</p>

> Componentes da velocidade inicial do corpo

<p align="justify">Os módulos das componentes da velocidade inicial do corpo são dadas pelas seguintes equações:</p>

$$v _{ix} = v _{i}.cos(\theta)$$

e
 
$$v _{iy} = v _{i}.sen(\theta)$$

<p align="justify">onde, $v _{i}$ representa o módulo da velocidade inicial do corpo, $v _{ix}$ representa o módulo da componente da velocidade inicial na direção (horizontal) do eixo x, $v _{iy}$ representa o módulo da componente da velocidade inicial na direção (vertical) do eixo y e $\theta$ representa o ângulo de lançamento do corpo. Visualize os vetores velocidade inicial e suas componentes vetoriais na figura abaixo:</p>
![Componentes da velocidade inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo1.png "Componentes da velocidade inicial")

> Motivação

* <p align="justify">Um corpo é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 10 m/s<sup>2</sup>.</p> 

Dados:

$$\theta = 30°.$$ 
$$v_{i} = 50~m/s.$$ 
$$sen~30°= 0,5.$$
$$cos~30°\cong0,866.$$ 

<p align="justify">Observação: por enquanto, não usaremos o valor de g.</p>

> <p align="justify"> Determinando a componente da velocidade inicial na horizontal:</p>

$$v _{ix} = v _{i}.cos\theta= 50.0,866\cong43,30~m/s.$$

> <p align="justify"> Determinando a componente da velocidade inicial na vertical:</p>

$$v _{iy} = v _{i}.sen\theta= 50.0,5=25~m/s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos para calcular as componentes da velocidade inicial no R:</p>

<p align="justify"> Em R, os argumentos das funções trigonométricas, os graus, devem ser transformados em radianos multiplicando (pi/180) pelo ângulo dado. Desse resultado é extraído o cosseno (cos) e o seno (sin).</p> 

<p align="justify"> Determinaremos as componentes da velocidade inicial do projétil do problema dado.</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 50
# ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar vix e viy:
cat("A componente vix é", vix)
cat("A componente viy é", viy)

A componente vix é 43.30127
A componente viy é 25
```
> DEVER DE CASA - estude e execute no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade igual a 9,8 m/s<sup>2</sup>.Compare sua resposta logo abaixo.</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar vix e viy:
cat("A componente vix é",  vix)
cat("A componente viy é",  viy)

```
> Compare sua resposta

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A componente x da vi é = 70.71068; <br>  A componente y da vi é = 70.71068.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 9.8. m/s<sup>2</sup>.</p>

*** =instructions
<p align="justify"> Use o código estudado neste tópico para calcular as componentes x e y da velocidade inicial(vi).</p> 
<p align="justify"> Por enquanto, não usaremos o valor de g.</p>
*** =hint
<p align="justify"> - O ângulo dado equivale a 60° e a variável teta equivale a</p> 
$$(pi/180)*angulo.$$ 
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial(vi):
vi <- 200
# Escreva o ângulo dado em graus:
angulo <- 
# Graus em radianos:
teta <-
# Componentes da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar vix:
vix
# mostrar viy:
viy
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial(vi):
vi <- 200
# Escreva o ângulo dado em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar vix:
vix
# mostrar viy:
viy
```
*** =sct
```{r}
test_output_contains("173.20511", incorrect_msg = "Digite corretamente o valor da variável angulo. O valor da variável teta equivale a $$(pi/180)*angulo.$$.")
success_msg("Bom trabalho! Você adquiriu noções sobre as componentes da velocidade inicial do lançamento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:863cc9aee1
## Altura máxima

> Altura máxima no movimento oblíquo

<p align="justify">O valor da altura máxima, no movimento oblíquo, é obtido adaptando-se a a equação de Torricelli para</p>

$$v _{y}^{2}= v _{iy}^{2}-2gh _{máx}$$

<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $g$ é a aceleração da gravidade a qual vamos considerar como 9.8m/s<sup>2</sup> e $h _{máx}$ é a altura máxima alcançada pelo projétil.</p>

<p align="justify">Sabemos que à medida que o projétil vai atingindo a altura máxima, sua velocidade vai dimunuindo. Quando chega exatamente no ponto da altura máxima, o projétil tem sua velocidade equivalente a zero. Portanto, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), ou seja,</p>
$$0= v _{iy}^{2}-2gh _{máx}.$$
<p align="justify">Daí, podemos obter a expresão para a altura máxima alcançada pelo projétil:</p>
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow$$ 
$$v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Tempo para o projétil atingir a altura máxima

<p align="justify">Para determinar quanto tempo o projétil levará para atingir a altura máxima, adaptaremos a equação da velocidade do MRUV para:</p>
$$v _{y}=  v _{iy} - gt _{hmáx}$$
<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $-g$ é a aceleração da gravidade de sentido oposto ao da velocidade inicial e $t _{hmáx}$ é o tempo necessário para que o projétil alcance a altura máxima. Já sabemos que, na altura máxima, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), portanto, a equação acima torna-se</p>

$$0=v _{iy}-gt _{hmáx} \rightarrow$$
$$-v _{iy}=-gt _{hmáx} \rightarrow$$
$$v _{iy}=gt _{hmáx} \rightarrow$$
$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$

<p align="justify">Visualize, na figura abaixo, a representação de $hmáx$, $v _{y} = 0$, $v _{y}$, $g$, o alcance do projétil e todos os componentes do movimento oblíquo:</p>
![Componentes do movimento oblíquo inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo2.png "Componentes do movimento oblíquo")

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Neste problema, não usaremos nem a velocidade inicial ($v _{i}$) e nem a componente da velocidade inicial ($v _{ix}$)</p> 

<p align="justify">No tópico anterior foi determinado a componente da velocidade inicial, $v _{iy}$.</p>

Dado:

$$v _{iy} = 25~m/s.$$

> <p align="justify"> A altura máxima:</p>

$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}= \displaystyle \frac{25^{2}}{2.9,8}= \displaystyle \frac{625}{19,6}\cong 31,88~m.$$

> <p align="justify"> O tempo para atingir a altura máxima:</p>

$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}=\displaystyle\frac{25}{9,8}\cong 2,55~s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos no R para calcular a altura máxima e o tempo para alcançá-la:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy = 25
# Altura máxima:
hmax = (viy ^ 2)/(2 * g)
# Tempo da hmax
thmax = viy/g
# Mostrar a hmax e o thmax:
cat("A altura máxima é", hmax)
cat("O tempo até a hmax é", thmax)

A altura máxima é 31.88776
O tempo até a hmax é 2.5510204081632653061224489795918
```
> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. A componente y da vel. inicial é igual a: 70.71068 - calculada em tópico anterior. Compare sua resposta logo abaixo. </p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy =  70.71068
# Altura máxima:
hmax = (viy ^ 2)/(2 * g)
# Tempo até a hmax:
thmax = viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O tempo até a hmax é", thmax)
```
> Compare sua resposta

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A altura máxima é 255.1021; <br>  O tempo até a hmax é 7.215376.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>

*** =instructions
<p align="justify"> Use o código estudado neste tópico para calcular altura máxima e o tempo necessário para atingir esta altura.</p> 
<p align="justify"> Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>e a componente vertical da velocidade inicial equivalente a 173.2051, calculado no tópico anterior.</p>
*** =hint
<p align="justify"> A altura máxima no movimento oblíquo é dada pela seguinte expressão:</p> 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 
# Componente viy:
viy =  173.2051
# Altura máxima:
hmax = (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax = 
# Mostrar hmax e thmax:
hmax
thmax
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy =  173.2051
# Altura máxima:
hmax = (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax = viy/g
# Mostrar hmax e thmax:
hmax
thmax
```
*** =sct
```{r}
test_output_contains("17.67399", incorrect_msg = "Digite corretamente o valor da aceleração da gravidade e a expressão para a altura máxima alcançada pelo projétil.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular a altura máxima alcançada pelo projétil e o tempo gasto para atingí-la.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:12980fa718
## Tempo de trajeto
> Tempo de subida mais o tempo de descida

<p align="justify">Neste estudo estamos desprezando a resistência do ar, por isso o tempo que o projétil leva para atingir a altura máxima é o mesmo tempo gasto para voltar da altura máxima até o solo. Portanto,  o tempo total gasto em todo o trajeto pode ser  dado pela seguinte expressão:</p>
$$t _{tot} = 2t _{hmáx}$$
<p align="justify">onde, $t _{tot}$ corresponde ao tempo total ou tempo de trajeto e $t _{hmáx}$ ao tempo necessário para o projétil alcançar a altura máxima.</p>
> Alcance

<p align="justify"> Sabemos que o movimento do projétil, na direção horizontal, é do tipo Movimento Retilíneo Uniforme (MRU). Para determinar o alcance, ou seja, a distância percorrida pelo projétil da posição de lançamento até tocar no solo, adaptaremos a equação do espaço do MRU ($X= v _{ix}.t$) para</p>
$$A=v _{ix}.t _{tot}$$
<p align="justify">onde $A$ corresponde ao alcance, $v _{ix}$ à componente da velocidade inicial na direção x, e $t _{tot}$ ao tempo total ou tempo de trajeto.</p> 
> Motivação

* <p align="justify">Continuação do resolução do exercício: um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a o tempo total gasto e o alcance do projétil. Dados: $9,8~m/s^{2}$. O $t _{hmáx}=2,55~s$ e a $v _{ix}=43,30127~m/s$ já foram determinados em tópicos anteriores.</p>

<p align="justify">O tempo de trajeto pode ser determinado por:</p> 

$$t _{tot} = 2t _{hmáx} = 2.2,55 = 5,1~s.$$

<p align="justify">O alcance do projétil pode ser determinado por:</p>

$$A=v _{ix}.t _{tot} =  43,30127.5,1 = 220,83 m/s.$$

> <p align="justify">Comandos no R para calcular o tempo de trajeto e o alcance:</p>

```{r}
# Componente vix:
vix = 43.30127
# Tempo da hmax:
thmax = 2.5510204081632653061224489795918
# Tempo total:
ttot = 2 * thmax
# Alcance:
A = vix * ttot
cat("O tempo de trajeto é", ttot)
cat("O alcance é ", A)

O tempo de trajeto é 5.102041
O alcance é 220.9248
```
> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Calcule todos os elementos do lançamento oblíquo, visto até agora. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. (Compare sua resposta logo abaixo</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar componentes da vi:
cat("A componente vix é", vix)
cat("A componente viy é", viy)
# Altura máxima:
hmax = (viy ^ 2)/(2 * g)
# Tempo da hmax
thmax = viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O thmax é", thmax)
# tempo total ou de trajeto:
ttot = 2 * thmax
# alcance:
A = vix * ttot
cat("O tempo total é", ttot)
cat("O alcance é", A)
```
> Compare sua resposta

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">   A componente vix é 70.71068; <br>  A componente viy é 70.71068; <br>  A altura máxima é 255.102; <br>  O thmax é 7.215375; <br>  O tempo total é 14.43075; <br>  O alcance é 1020.408.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine todos os elementos do lançamento oblíquo visto até agora. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> Use os códigos estudados neste tópico para calcular todos os elementos do lançamento oblíquo visto até agora.</p> 
<p align="justify"> Adotaremos sempre a aceleração da gravidade como g = 9.8 m/s<sup>2</sup>.</p>
*** =hint
<p align="justify"> A componente da velocidade inicial na direção horizontal e o tempo de trajeto são dados, respectivamente, por
$$v _{ix} = v _{i}.cos(\theta)$$
e
$$t _{tot} = 2t _{hmáx}.$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 200
# Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Escreva a componente vix:
vix <-   
viy <- vi * sin(teta)  
# Mostrar compon.da vi:
vix
viy
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar a hmax e thmax:
hmax
thmax
# Escreva o tempo total:
ttot <- 
# Alcance
A <- vix * ttot
# Mostrar ttot e A:
ttot
A
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 200
# Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Escreva a componente vix:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# Mostrar compon.da vi:
vix
viy
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar a hmax e thmax:
hmax
thmax
# Escreva o tempo total:
ttot <- 2 * thmax
# Alcance
A <- vix * ttot
# Mostrar ttot e A:
ttot
A
```
*** =sct
```{r}
test_output_contains("3534.798", incorrect_msg = "Veja nas dicas o valor da componente da velocidade inicial e do tempo gasto em toda trajetória.")
success_msg("Bom trabalho! Você adquiriu noções sobre a o tempo de trajeto e o alcance de um projétil no movimento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:314c81a391
## Componentes da velocidade
<p align="justify"> Assim como a velocidade inicial possui suas componentes, a velocidade no instante t e na posição p também possui suas componentes dadas pelas seguintes equações:</p>

$$v _{x} = v _{ix} = v _{i}.cos(\theta)$$

e
 
$$v _{y} = v _{iy} - gt$$

<p align="justify">onde, $v _{x}$ corresponde à componente horizontal da velocidade e $v _{y}$ corresponde à componente vertical da velocidade num determinado instante. Observe que na primeira equação a componente horizontal da velocidade inicial equivale à componente horizontal da velocidade, num dado instante e numa dada posição.</p> 

> Velocidade resultante

<p align="justify">No lançamento oblíquo, quando queremos determinar a velocidade resultante de um projétil num determinado ponto e instante, podemos recorrer à seguinte equação:</p>

$$v _{r}= \sqrt{v _{x}^{2}+ v _{y}^{2}}$$

<p align="justify">onde, $v _{r}$ corresponde à velocidade resultante do projétil em um ponto $p$ num determinado instante $t$ e $v _{x}$, que é constante, corresponde à componente horizontal da velocidade e $v _{y}$ corresponde à componente vertical da velocidade.</p>

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Considere $g = 9,8~m/s^{2}$ e determine a velocidade resultante do projétil no instante 2 segundos. As componentes da velocidade inicial já foram determinadas em tópicos anteriores.</p>

> <p align="justify"> A componente $v _{x}$ é constante:</p> 

$$v _{x} = v _{ix} = 43.30127~m/s.$$

> <p align="justify"> A componente $v _{y}$ pode ser obtida pela equação:</p>

$$v _{y} = v _{iy} - gt = 25 - 9,8.2$$ 
$$= 25 - 19,6 = 5,4~m/s.$$

> <p align="justify"> A velocidade resultante pode ser obtida utilizando-se a equação:</p>

$$v _{r}= \sqrt{v _{x}^{2}+ v _{y}^{2}} = \sqrt{43.30^{2}+ 5,4^{2}}$$ 
$$= \sqrt{1874,89 + 29,16}$$ 
$$= \sqrt{1904,05} = 43,635~m/s.$$

> <p align="justify">Comandos no R para determinar a $v _{r}$:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 2
# Velocidade inicial:
vi <- 50
# Ângulo em graus:
angulo <- 30
# Graus em radianos:
teta <- (pi/180) * angulo
# Componente vix:
vix <- vi * cos(teta) 
# Componente viy:
viy <- vi * sin(teta) 
# MRU (vx = vix):
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy é", vy)
cat("A vr é", vr)

A vy é 5.4
A vr é 43.63668
```
> <p align="justify"> Na altura máxima a velocidade do projétil na direção vertical é nula?</p>

<p align="justify"> Sim. Para provar que isso é verdade, precisamos apenas do tempo que o projétil levou até na altura máxima que já foi calculado como 2.551 ou, para ser mais exato, como 2.55102040816.... Basta implementar esse dado no código em R:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 2.5510204081632653061224489795918
# Componente vx:
vx <- 43.30127
# Componente viy:
viy <- 25
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)

cat("A vy na hmax é", vy)
cat("A vr na hmax é", vr)

A vy na hmax é 0
A vr na hmax é 43.30127
```
> <p align="justify"> Velocidade do projétil ao atingir o solo</p>

<p align="justify"> Na altura máxima a a componente vy é nula, porém, a velocidade resultante (vr) não é nula, tem valor mínimo igual à componente horizontal (vx = vix = 43.30127). Para atingir a altura máxima (31,88776 m) o projétil leva exatamente 2,55102040816326530.... Se multiplicarmos esse tempo por dois (tempo de subida e tempo de descida) chegaremos ao tempo total ou de trajeto igual a 5,102040816.... Pergunta-se: qual é o valor da velocidade da componente vertical e da velocidade resultante quando o projétil alcançar o tempo de trajeto (ao atingir o solo)? Basta implementar o tempo de trajeto no código em R:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 5.1020408163265306122448979591836
# Componente vx:
vx <- 43.30127
# Componente viy:
viy <- 25
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy no tempo total é", vy)
cat("A vr no tempo total é", vr)

A vy no tempo total é -25
A vr no tempo total é  50
```
> Dados interessantes

<p align="justify"> - A velocidade que o projétil cai no chão é a mesma velocidade inicial de lançamento (50 m/s). O valor da componente vertical da velocidade de saída (no problema viy = 25 m/s) do projétil é o mesmo na sua chegada ao chão, porém, de sinal contrário (-25 m/s). Em qualquer posição (X,Y) da trajetória parabólica o projétil possui duas velocidades de mesmo módulo, uma positiva ao subir e uma negativa ao descer.</p>

<p align="justify"> - Ao subir, o projétil executa um movimento progressivo (quando o deslocamento do corpo ocorre no sentido crescente da trajetória) e retardado (velocidade e aceleração da gravidade têm sinais contrários). Ao descer, o projétil executa um movimento retrógrado (quando o deslocamento do corpo ocorre no sentido decrescente da trajetória) e acelerado (velocidade e aceleração da gravidade têm mesmo sinais)</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine a componente vertical da velocidade (vy) e a velocidade resultante (vr) do projétil no instante em que o mesmo alcança a altura máxima. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Já calculados: a componente x da vi é a mesma componente x da v que é igual a 70.71068, a componente y da vi também é igual a 70.71068, o tempo gasto para o projétil atingir o ponto mais alto da trajetória é igual a 7.215376. Compare sua resposta logo abaixo.</p>

```{r}
g <- 9.8
# Componente vx:
vx <- 70.71068
# Componente viy:
viy <- 70.71068
# Tempo na hmax:
thmax <- viy/g
# Componente vy:
vy <- viy - g * thmax
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy na hmax é", vy)
cat("A vr na hmax é", vr)
```
> Compare sua resposta

<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A vy na hmax é 0 (zero); <br>  A vr na hmax é 70.71068.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a componente vertical da velocidade (vy) e a velocidade resultante (vr) do projétil no instante em que o mesmo alcança a altura máxima. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> Use os comandos estudados neste tópico para calcular a componente vertical da velocidade e a velocidade resultante do projétil no tempo da altura máxima.</p> 
<p align="justify"> Adotaremos sempre a aceleração da gravidade como g = 9.8 m/s<sup>2</sup>.</p>
*** =hint
<p align="justify"> O valor da velocidade resultante no movimento oblíquo é dado pela seguinte expressão:</p>
$$v _{r}= \sqrt{v _{x}^{2}+ v _{y}^{2}}.$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 200
#Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes x e y da vi:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
viy <- vi * sin(teta)  
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# tempo da hmax
thmax <- viy/g
# Componente vy:
vy <- viy - g * thmax
# escreva a veloc. resultante:
vr <- 
# Mostrar vy:
vy
# Mostrar vr:
vr
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 200
#Ângulo em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes x e y da vi:
vix <- vi * cos(teta)
# vx é igual a vix:
vx <- vix
viy <- vi * sin(teta)  
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# tempo da hmax
thmax <- viy/g
# Componente vy:
vy <- viy - g * thmax
# escreva a veloc. resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar vy:
vy
# Mostrar vr:
vr
```
*** =sct
```{r}
test_output_contains ("100", incorrect_msg = "Escreva corretamente a expressão que calcula a velocidade resultante. Veja nas dicas a expressão que usamos para determinar a velocidade resultante.")
success_msg ("Bom trabalho! Você aprendeu a determinar o valor da componente vertical da velocidade e o valor da velocidade resultante do projétil quando o mesmo alcança a altura máxima.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:92a2d6e6a2
## Posição do projétil
<p align="justify"> A equação que fornece a posição do projétil no instante t, segundo o eixo horizontal (X), é dada por </p>

$$X= v _{ix}.t$$

<p align="justify"> e a equação que fornece a posição do projétil no instante t, segundo o eixo vertical (Y), é dada por </p>
 
$$Y = v _{ix}.t- \displaystyle \frac{g.t^{2}}{2}\cdot$$

<p align="justify">Para determinar uma posição qualquer do projétil, basta obter os valores de X e Y.</p> 

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a posição do projétil em 2 segundos e em 4 segundos. Considere $g = 9,8~m/s^{2}$, a $v _{ix} = 43.30~m/s$ e a $v _{iy} = 25~m/s$ foram determinados em tópicos anteriores.</p>

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

> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal e vertical de v e a velocidade resultante - todos no tempo de dois segundos:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 2
# vix - já calculado:
vix <-  43.30127
# viy - já calculado:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# vx é uniforme e igual a vix:
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A posição do projétil é",  X, "e", Y)
cat("As componentes de v:", vx, "e", vy)
cat("A velocidade resultante é", vr)

A posição do projétil é 86.60254 e 30.4
As componentes de v: 43.30127 e 5.4
A velocidade resultante é 43.63668
```
> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal de v, a componente vertical de v e a velocidade resultante - todos no tempo de altura máxima:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante na hmax:
t <- 2.5510204081632653061224489795918
# Componente vix:
vix <- 43.30127
# Componente viy:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# vx é igual a vix:
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A posição X na hmax é",  X, "e", Y)
cat("As componentes de v:", vx, "e", vy)
cat("A vr no tempo dado é", vr)

A posição X na hmax é 110.4624 e 31.88776
As componentes de v: 43.30127 e 0
A vr no tempo dado é 43.30127
```
<p align="justify">Observe que o valor de X na altura máxima equivale a 110,4624 m, a metade do alcance (A = 220,9248m). Observe também que o valor de Y, para esse tempo exato, equivale à altura máxima (31.88776). Observe que a componente da velocidade na horizontal (vx = vix), em um dado tempo, não varia.</p>

> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal de v, a componente vertical de v e a velocidade resultante - todos no tempo de 4s:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 4
# Componente vix:
vix <- 43.30127
# Componente viy:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# Componente vx:
vx <- vix
# Componente vy:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("Posição do projétil:",  X, "e", Y)
cat("Componentes de v:", vx, "e", vy)
cat("vr no tempo dado é", vr)
Posição do projétil: 173.2051 e 21.6
Componentes de v: 43.30127 e -14.2
vr no tempo dado é: 45.57017
```
<p align="justify">Observe que após o tempo de altura máxima (2,5510...), no caso 4s, o projétil já está caindo e, no eixo X, o projétil já passou da metade do alcance (110,4624), no caso, 173,2051m. Observe que na queda do projétil a componente vertical da velocidade está negativa e o vetor resultante é positivo.</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Sendo que o alcance máximo acontece quando o ângulo de lançamento é equivalente a 45°, prove que esse alcance máximo (A) é quatro vezes maior que a altura máxima (hmáx). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>

```{r}
# Aceleração da gravidade:
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
<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A altura máxima é 255.102; <br>  O alcance é 1020.408; <br>  1020.408 é 4 vezes 255.102.</font></p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a posição do projeto no tempo de 2 segundos. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Use os comandos em R, estudados neste capítulo, para calcular a posição do projétil no tempo de 2s. Você escreverá apenas a equação da posição do projétil no eixo X.</p>
<p align="justify"> - Leia todo o código do exercício e digite a equação onde tá escrito "# Escreva a eq. da posição em X".</p>
*** =hint
<p align="justify"> O valor da posição do projétil, no eixo X, é obtido pela seguinte expressão:</p>
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
t <- 2
# Velocidad inicial:
vi <- 200
#Ângulo dado em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes x e y da vi:
vix <- vi * cos(teta)
viy <- vi * sin(teta)
# vx é uniforme e igual a vix:
# Escreva a eq. da posição em X
X <- 
# Equação da a posição em Y
Y <- viy * t - (g * t ^ 2)/2 
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
t <- 2
# Velocidad inicial:
vi <- 200
#Ângulo dado em graus:
angulo <- 60
# Graus em radianos:
teta <- (pi/180) * angulo
# Componentes x e y da vi:
vix <- vi * cos(teta)
viy <- vi * sin(teta)
# vx é uniforme e igual a vix:
# Escreva a eq. da posição em X
X <- vix * t
# Equação da a posição em Y
Y <- viy * t - (g * t ^ 2)/2 
# Mostrar posição Y
Y
# Mostrar posição X
X
```
*** =sct
```{r}
test_output_contains ("200", incorrect_msg = "Escreva a expressão que calcula o valor da posição de um projétil no eixo X. Não esqueça que o símbolo para multiplicar é o asterisco. Veja nas dicas essa expressão.")
success_msg ("Bom trabalho! Você aprendeu a determinar o valor da posição (X, Y) do projétil em um determinado tempo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:289ca73696
## Direção do projétil

<p align="justify"> O ângulo de lançamento do projétil foi chamado de $\theta$. Chamaremos de $\alpha$ a direção do projétil em um dado instante t que será determinada pelo cálculo da tangente entre a componente da velocidade na vertical e a componente da velocidade na horizontal. A expressão que calcula a tangente de um ângulo é dada por:</p>

$$tg~ \alpha  = \displaystyle \frac{v _{y}}{v _{x}}$$

<p align="justify"> onde, $\alpha$ corresponde ao ângulo formado entre a componente horizontal e a direção da velocidade resultante num dado instante, $v _{y}$ corresponde à componente da velocidade segundo a vertical e $v _{x}$ corresponde à componente da velocidade segundo a horizontal.</p>

<p align="justify">Da expressão acima podemos encontar o valor do ângulo $\alpha$:</p> 

$$\alpha = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$

> Motivação 1

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a direção do projétil ao atingir o solo. Considere $g = 9,8~m/s^{2}$, a $v _{x} = 43,30127~m/s$ e a $v _{y} = -25~m/s$ foram determinados em tópicos anteriores.</p>

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
# Atribuir o valor vy/vx:
tang <- vy/vx
# Atribuir o valor do arco tg
angulo <- atan(tang)
# Atribuir o valor angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar variável graus
graus

 -30
```
<p align="justify">Portanto, o ângulo cuja tangente é igual a -0,57735031 equivale a -30°.</p>

> Mais um exemplo

* <p align="justify"> Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Determine a direção do projétil ao atingir o solo. Considere $g = 9,8~m/s^{2}$, a $v _{x} = 25 m/s$ e a $v _{y} = -53~m/s$.</p>

```{r}
# vx e vy dados no problema:
vx <-  25
vy <- -53
# Atribuir valor vy/vx:
tang <- vy/vx
# Atribuir valor do arco tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
# Mostrar variável graus
graus

-64.74684 
```
<p align="justify"> Aproximadamente -65° é o ângulo formado, em relação à horizontal, no momento em que o projétil chega ao chão.</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Determine: a) A altura máxima desenvolvida pelo projétil; b) O tempo gasto para chegar na altura máxima; c) O alcance desenvolvido pelo projétil; d) A velocidade da componente vertical, a velocidade resultante e a direção do projétil ao alcançar o solo; e) A posição do projétil no tempo de 5 segundos. Compare sua resposta logo abaixo.</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 50
# ângulo dado em graus:
angulo <- 60
# transformar graus em rad:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta)
# altura máxima
hmax = (viy ^ 2)/(2 * g)
# Tempo na hmax:
thmax <- viy/g
# tempo tot de trajeto:
ttot = 2 * thmax
# alcance:
A = vix * ttot
# Instante dado:
t = 5
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2
# vx é uniforme e igual a vix:
vx <- vix
# Componente vertical de v:
vy <- viy - g * ttot 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Atribuir o valor vy/vx:
tang <- vy/vx
# Atribuir valor do arc tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
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
--- type:NormalExercise lang:r xp:100 skills:1 key:dee61a2620
## Explorando dados dos Eixos

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

> Valores do eixo X (Distância horizontal)

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine e analise os valores das distâncias (coordenadas X) e as alturas (coordenadas Y) do projétil a cada 2,209248 m de distância horizontal a partir de onde onde foi lançado (de 0 m) até o alcance (A = 220,9248 m). Considere $g = 9,8~m/s^{2}$.</p>

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
#Mostrar o eixo X
X
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

# Extrai o valor nº 51 do eixo Y
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

```{r}
<p align="justify">Observe que o valor de X na altura máxima equivale a 110,4624 m, a metade do alcance (A = 220,9248m). Observe também que o valor de Y corresponde à altura máxima (31.88776).</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil com uma velocidade inicial igual a 100 m/s é lançado a partir do solo, formando com o mesmo um ângulo de 45°. Particione o alcance máximo (1020,408m), numa sequência de 1,020408m em 1,020408m, escrevendo um comando que indique a posição do projétil na altura máxima (correspondende à metade do alcance máximo). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Compare sua resposta logo abaixo.</p>



Sendo que o alcance máximo é igual a 
<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">  A altura máxima é 255.102; <br>  O alcance é 1020.408; <br>  1020.408 é 4 vezes 255.102.</font></p>

1020.408

```{r}
# Aceleração da O alcance é gravidade:
g <- 9.8
# Espaço inicial:
xi <- 0
# Espaço final:
yi <- 0
# Sequência de 0 até o Alcance indo de 2.209248 em 2.209248:
X <- seq(from = 0, to = 1020.408, by = 1.020408)
# Velocidade inicial:
vi <- 100
# ângulo em graus:
angulo <- 45
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
# Maximo no Y
max(Y)
255.102
# Maximo no X
1020.408
# Posições X,Y na hmax
X[c(501)]; Y[c(501)]
510.204
255.102
```
> Compare sua resposta 


<p style="background-color:#000000; font-weight: bold; font-size: 20px; text-align:justify"><font color="#ffffff">[1] 510.204
[1] 255.102</font></p>

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
--- type:NormalExercise lang:r xp:100 skills:1 key:b9d71cd47e
## Gráfico do lançamento oblíquo

<p align="justify">eSCREVER SOBRE O GRÁFICO -- Sabemos que um corpo está em movimento uniforme quando o mesmo percorre espaços iguais em intervalos de tempos iguais. O movimento do projétil no eixo X é constante, ou seja, a componente da velocidade inicial vix, que também é igual à componente da velocidade vx, é constante. Foi programado no R para que os espaços fossem divididos de 2,209248m em 2,209248m até atingir o alcance máximo de 220,9248m. Foram obtidos intervalos de tempos iguais, dividindo cada 2,209248m pelo valor da componente vix (43,30127m/s) que resultou em 0,0510204s. Vejamos o código:</p> 

<p align="justify"> Para testar os códigos em R, acesse o link abaixo:</p>

[R-Fiddle](http://www.r-fiddle.org/#/)


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
# Traçar gráfico
plot(X, Y, main="Lançamento oblíquo", xlim = c(0, 220.924800), ylim = c(0, 31.88776), col="blue" , type="l", xlab = "Alcance (m)", ylab = "Altura (m)")
abline(h = 31.88776, col="red")
abline(v = 110.4624002, col="red")
```
CONTINUAR

<p align="justify">Isso gerou os seguintes valores:</p>



<p align="justify"> Baseado nos dados de vy, vr e tempo, observe que na altura máxima atingida pelo projétil, o tempo chega a 2,5510199s e a componente da velocidade, vy, tende a zero (0,00000542087m/s). Na chegada do projétil ao solo, a componente da velocidade vy tende a -25m/s (-24,99999m/s) e a velocidade resultante tende a 50 m/s (49,99999), isso quando completa o tempo de trajeto de 5,1020397s.</p>

> Comandos para explorar os valores 

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