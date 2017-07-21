--- 
title_meta  : Capítulo 2
title       : Projeto - Lançamento Oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:8ea80fa0d0
## Componentes da velocidade inicial

<p align="justify">Um corpo lançado obliquamente possui dois tipos de movimentos: um segundo a horizontal e o outro segundo a vertical. O movimento descrito pelo corpo, lançado segundo a horizontal, é do tipo MRU (Movimento Retilíneo Uniforme). E o outro movimento descrito pelo corpo, lançado segundo a vertical, é do tipo MRUV (Movimento Retilíneo Uniformemente Variado). A trajetória descrita pelo corpo terá a forma parabólica.</p>

> Componentes da velocidade inicial do corpo

<p align="justify">As componentes da velocidade inicial do corpo são dadas pelas seguintes equações:</p>

$$v _{ix} = v _{i}.cos(\theta) \qquad Eq. 01$$

e
 
$$v _{iy} = v _{i}.sen(\theta) \qquad Eq. 02$$

onde,

<p align="justify">$v _{i}$ representa a velocidade inicial do corpo, $v _{ix}$ representa a componente da velocidade inicial na direção (horizontal) do eixo x, $v _{iy}$ representa a componente da velocidade inicial na direção (vertical) do eixo y e $\theta$ representa o ângulo de lançamento do corpo. Visualize a velocidade inicial e suas componentes na figura abaixo:</p>
![Componentes da velocidade inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo1.png "Componentes da velocidade inicial")

> Motivação

* <p align="justify">Um corpo é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 10 m/s<sup>2</sup>.</p> 


Dados:

$$\theta = 30°.$$ 
$$v_{i} = 50~m/s.$$ 
$$sen(30°)= 0.5.$$
$$cos(30°)\cong0.866.$$ 

<p align="justify">Observação: por enquanto, não usaremos o valor de g.</p>

> <p align="justify"> Determinando a componente da velocidade inicial na horizontal (Eq. 01):</p>

$$v _{ix} = v _{i}.cos\theta= 50.(0.866)\cong43,30~m/s.$$

> <p align="justify"> Determinando a componente da velocidade inicial na vertical (Eq. 02):</p>

$$v _{iy} = v _{i}.sen\theta= 50.(0.5)=25~m/s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos para calcular as componentes da velocidade inicial no R:</p>

<p align="justify">- Use o problema anterior e determine as componentes da velocidade inicial do corpo.</p>

<p align="justify">Obs.: Em R, os argumentos das funções trigonométricas, os graus, devem ser transformados em radianos da seguinte maneira: ($pi/180$) multiplicado pelo ângulo. Após isso, tira-se o $cosseno (cos)$ e o $seno (sin)$ desse resultado.</p> 

```{r}
# aceleração da gravidade:
g <- 9.8
# velocidad inicial:
vi <- 50
# ângulo dado em graus:
angulo <- 30
# transformar graus em radianos:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar a componente x e y da vi:
cat("A componente x da vi é igual a:", vix)
cat("A componente y da vi é igual a:", viy)

A componente x da vel. inicial é igual a: 43.30127
A componente y da vel. inicial é igual a: 25
```

> DEVER DE CASA - estude e execute no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p> (Compare sua resposta: A componente x da vel. inicial é igual a: 70.71068 e a componente y da vel. inicial é igual a: 70.71068).</p>

```{r}
# aceleração da gravidade:
g <- 9.8
# velocidad inicial:
vi <- 100
# ângulo dado em graus:
angulo <- 45
# transformar graus em radianos:
teta <- (pi/180) * angulo
# componente x e y da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar as componentes x e y da vi:
cat("A componente x da vi é igual a:", vix)
cat("A componente y da vi é igual a:", viy)

```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 9.8. m/s<sup>2</sup>.</p></p>

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
# aceleração da gravidade:
g <- 9.8
# velocidad inicial(vi):
vi <- 200
# escreva o ângulo dado em graus:
angulo <- 
# transforme graus em radianos:
teta <-
# componente x da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar a componentes x da vi:
vix
# mostrar a componentes y da vi:
viy
```
*** =solution
```{r}
# aceleração da gravidade:
g <- 9.8
# velocidad inicial(vi):
vi <- 200
# escreva o ângulo dado em graus:
angulo <- 60
# transforme graus em radianos:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar a componentes x da vi:
vix
# mostrar a componentes y da vi:
viy
```
*** =sct
```{r}
test_output_contains("173.20511", incorrect_msg = "Digite corretamente o valor da variável angulo. O valor da variável teta equivale a $$(pi/180)*angulo.$$.")
success_msg("Bom trabalho! Você adquiriu noções sobre componentes da velocidade inicial do lançamento oblíquo da Física.")
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
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Tempo para o projétil atingir a altura máxima

<p align="justify">Para determinar quanto tempo o projétil levará para atingir a altura máxima, adaptaremos a equação da velocidade do MRUV para:</p>
$$v _{y}=  v _{iy} - gt _{hmáx}$$
<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $-g$ é a aceleração da gravidade de sentido oposto ao da velocidade inicial e $t _{hmáx}$ é o tempo necessário para que o projétil alcance a altura máxima. Já sabemos que, na altura máxima, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), portanto, a equação acima torna-se</p>

$$0=v _{iy}-gt _{hmáx} \rightarrow$$
$$-v _{iy}=-gt _{hmáx} \rightarrow v _{iy}=gt _{hmáx} \rightarrow$$
$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$

<p align="justify">Visualize na figura abaixo a representação de $hmáx$, $v _{y} = 0$, $v _{y}$, $g$, o alcance do projétil e todos os componentes do movimento oblíquo:</p>
![Componentes do movimento oblíquo inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo2.png "Componentes do movimento oblíquo")

> Motivação

* <p align="justify">Aproveitaremos o primeiro exemplo do tópico anterior: um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Neste problema, não usaremos nem a velocidade inicial ($v _{i}$) e nem a componente da velocidade inicial ($v _{ix}$)</p> 

<p align="justify">Observação: no tópico anterior foi determinado a componente da velocidade inicial, $v _{iy}$.</p>

Dado:

$$v _{iy} = 25~m/s.$$

> <p align="justify"> A altura máxima:</p>

$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}= \displaystyle \frac{25^{2}}{2.9,8}= \displaystyle \frac{625}{19,6}\cong 31,88~m.$$

> <p align="justify"> O tempo para atingir a altura máxima:</p>

$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}=\displaystyle\frac{25}{9,8}\cong 2,55~s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos no R para calcular a altura máxima e o tempo para alcançá-la:</p>

<p align="justify">- Determinaremos a altura máxima e o tempo para alcançá-la.</p>

```{r}
# aceleração da gravidade:
g <- 9.8
# componente vertical de vi:
viy = 25
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax = viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
cat("A altura máxima é = :", hmax)
cat("O tempo gasto para atingir a hmax é = ", thmax)

A altura máxima é = 31.88776
O tempo gasto para atingir a hmax é = 2.5510204081632653061224489795918
```
> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. A componente y da vel. inicial é igual a: 70.71068 - calculada em tópico anterior. (Compare sua resposta: A altura máxima alcançada pelo projétil é igual a: 255.1021 e o tempo gasto para atingir o ponto mais alto da trajetória é igual a 7.215376). </p>

```{r}
# aceleração da gravidade:
g <- 9.8
# componente vertical de vi:
viy =  70.71068
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax = viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
cat("A altura máxima é igual a:", hmax)
cat("O tempo gasto na hmax é igual a:", thmax)
```
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
# aceleração da gravidade:
g <- 
# componente vertical de vi:
viy =  173.2051
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax = 
# mostrar a altura máxima e o tempo de alcançá-la:
hmax
thmax
```
*** =solution
```{r}
# aceleração da gravidade:
g <- 9.8
# componente vertical de vi:
viy =  173.2051
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax = viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
hmax
thmax
```
*** =sct
```{r}
test_output_contains("17.67399", incorrect_msg = "Digite corretamente o valor da aceleração da gravidade e a expressão para a altura máxima.")
success_msg("Bom trabalho! Você adquiriu noções sobre a altura máxima e sobre o tempo gasto para atingí-la.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:12980fa718
## Tempo de trajeto
> Tempo de subida mais o tempo de descida

<p align="justify">Neste estudo estamos desprezando a resistência do ar. O tempo que o projétil leva para atingir a altura máxima é o mesmo tempo gasto para voltar da altura máxima até o solo. Portanto,  o tempo total gasto em todo o trajeto pode ser  dado pela seguinte expressão:</p>
$$t _{tot} = 2t _{hmáx} \qquad Eq. 01$$
<p align="justify">onde, $t _{tot}$ corresponde ao tempo total ou tempo de trajeto e $t _{hmáx}$ ao tempo necessário para o projétil alcançar a altura máxima.</p>
#### Alcance
<p align="justify"> Sabemos que o movimento do projétil, na direção horizontal, é do tipo Movimento Retilíneo Uniforme (MRU). Para determinar o alcance, ou seja, a distância percorrida pelo projétil da posição de lançamento até tocar no solo, adaptaremos a equação do espaço do MRU ($X= v _{ix}.t) para</p>
$$A=v _{ix}.t _{tot} \qquad Eq. 02$$
<p align="justify">onde $A$ corresponde ao alcance, $v _{ix}$ à componente da velocidade inicial na direção x, e 
$t _{tot}$ ao tempo total ou tempo de trajeto.</p> 

> Motivação

* <p align="justify">Continuação do resolução do exercício: um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a o tempo total gasto e o alcance do projétil. Dados: $9,8~m/s^{2}$. O $t _{hmáx}=2,55~s$ e a $v _{ix} =  43.30127~m/s$ já foram determinados em tópicos anteriores.</p>

<p align="justify">Pela equação 01 deste tópico é determinado o tempo de trajeto:</p> 

$$t _{tot} = 2t _{hmáx} = 2.2,55 = 5,1~s.$$

<p align="justify">Pela equação 02 é determinado o alcance do projétil:</p>

$$A=v _{ix}.t _{tot} =  43,30127.5,1 = 220,83 m/s.$$

> <p align="justify">Comandos no R para calcular o tempo de trajeto e o alcance:</p>

```{r}
# componente horizontal de vi:
vix = 43.30127
# tempo da altura máxima
thmax = 2.5510204081632653061224489795918
# tempo total ou de trajeto:
ttot = 2 * thmax
# alcance
A = vix * ttot
cat("O tempo de trajeto é igual a:", ttot)
cat("O alcance é igual a:", A)

O tempo de trajeto é igual a: 5.102041
O alcance é igual a: 220.9248
```
> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Calcule todos os elementos do lançamento oblíquo, visto até agora. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. (Compare sua resposta: A componente x da vi é igual a: 70.71068, A componente y da vi é igual a: 70.71068, A altura máxima alcançada pelo projétil é igual a: 255.102, O tempo gasto para atingir o ponto mais alto da trajetória é igual a: 7.215375, O tempo de trajeto é igual a: 14.43075, O alcance é igual a: 1020.408).</p>
```{r}
# aceleração da gravidade:
g <- 9.8
# velocidad inicial:
vi <- 100
# ângulo dado em graus:
angulo <- 45
# transformar graus em radianos:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar a componente x e y da vi:
cat("A componente x da vi é = ", vix)
cat("A componente y da vi é = ", viy)
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax = viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
cat("A altura máxima é = ", hmax)
cat("O tempo para atingir a hmax é = ", thmax)
# tempo total ou de trajeto:
ttot = 2 * thmax
# alcance:
A = vix * ttot
cat("O tempo de trajeto é = ", ttot)
cat("O alcance é = ", A)
```
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
# aceleração da gravidade:
g <- 9.8
# velocidad inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em radianos:
teta <- (pi/180) * angulo
# Escreva a componente x da vi:
vix <-  
viy <- vi * sin(teta)  
# mostrar a componente x e y da vi:
vix
viy
# altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax <- viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
hmax
thmax
# Escreva o tempo de trajeto:
ttot <- 
# alcance
A <- vix * ttot
# mostrar tempo de trajeto e alcance:
ttot
A
```
*** =solution
```{r}
# aceleração da gravidade:
g <- 9.8
# velocidad inicial:
vi <- 200
# ângulo dado em graus:
angulo <- 60
# transformar graus em radianos:
teta <- (pi/180) * angulo
# Escreva a componente x da vi:
vix <- vi * cos(teta)  
viy <- vi * sin(teta)  
# mostrar a componente x e y da vi:
vix
viy
# altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# tempo da altura máxima
thmax <- viy/g
# mostrar a altura máxima e o tempo de alcançá-la:
hmax
thmax
# Escreva o tempo de trajeto:
ttot <- 2 * thmax
# alcance
A <- vix * ttot
# mostrar tempo de trajeto e alcance:
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
# ângulo dado em graus:
angulo <- 30
# transformar graus em radianos:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta) 
# Componente y da vi:
viy <- vi * sin(teta) 
# Movimento uniforme (vx = vix):
vx <- vix
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy é igual a:", vy)
cat("A vr é igual a:", vr)

A vy é igual a: 5.4
A vr é igual a: 43.63668
```

> <p align="justify"> Na altura máxima a velocidade do projétil na direção vertical é nula?</p>

<p align="justify"> Sim. Para provar que isso é verdade, precisamos apenas do tempo que o projétil levou até na altura máxima que já foi calculado como 2.551 ou, para ser mais exato, como 2.55102040816.... Basta implementar esse dado no código em R:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 2.5510204081632653061224489795918
# Componente horizontal de v:
vx <- 43.30127
# Componente vertical de vi:
viy <- 25
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)

cat("A vy no tempo da hmax é = ", vy)
cat("A vr no tempo da hmax é = ", vr)

A vy no tempo da hmax é =  0
A vr no tempo da hmax é =  43.30127
```
> <p align="justify"> Velocidade do projétil ao atingir o solo</p>

<p align="justify"> Na altura máxima a a componente vy é nula, porém, a velocidade resultante (vr) não é nula, tem valor mínimo igual à componente horizontal (vx = vix = 43.30127). Para atingir a altura máxima (31,88776 m) o projétil leva exatamente 2,55102040816326530.... Se multiplicarmos esse tempo por dois (tempo de subida e tempo de descida) chegaremos ao tempo total ou de trajeto igual a 5,102040816.... Pergunta-se: qual é o valor da velocidade da componente vertical e da velocidade resultante quando o projétil alcançar o tempo de trajeto (ao atingir o solo)? Basta implementar o tempo de trajeto no código em R:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 5.1020408163265306122448979591836
# Componente horizontal de v:
vx <- 43.30127
# Componente vertical de vi:
viy <- 25
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy no tempo de trajeto é = ", vy)
cat("A vr no tempo de trajeto é = ", vr)

A vy no tempo de trajeto é =  -25
A vr no tempo de trajeto é =  50
```
> Dados interessantes

<p align="justify"> - A velocidade que o projétil cai no chão é a mesma velocidade inicial de lançamento (50 m/s). O valor da componente vertical da velocidade de saída (no problema viy = 25 m/s) do projétil é o mesmo na sua chegada ao chão, porém, de sinal contrário (-25 m/s). Em qualquer posição (X,Y) da trajetória parabólica o projétil possui duas velocidades de mesmo módulo, uma positiva ao subir e uma negativa ao descer.</p>

<p align="justify"> - Ao subir, o projétil executa um movimento progressivo (quando o deslocamento do corpo ocorre no sentido crescente da trajetória) e retardado (velocidade e aceleração da gravidade têm sinais contrários). Ao descer, o projétil executa um movimento retrógrado (quando o deslocamento do corpo ocorre no sentido decrescente da trajetória) e acelerado (velocidade e aceleração da gravidade têm mesmo sinais)</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine a componente vertical da velocidade (vy) e a velocidade resultante (vr) do projétil no instante em que o mesmo alcança a altura máxima. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Já calculados: a componente x da vi é a mesma componente x da v que é igual a 70.71068, a componente y da vi também é igual a 70.71068, o tempo gasto para o projétil atingir o ponto mais alto da trajetória é igual a 7.215376. (Compare sua resposta: a vy ao atingir o t da hmax é = 0 e a vr ao atingir a hmax é = 70.71068.</p>

```{r}
g <- 9.8
# Componente horizontal de v:
vx <- 70.71068
# Componente vertical de vi:
viy <- 70.71068
# Tempo na altura máxima:
thmax <- viy/g
# Componente vertical de v:
vy <- viy - g * thmax
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A vy ao atingir o t da hmax é = ", vy)
cat("A vr ao atingir a hmax é = ", vr)
```
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
#Ângulo dado em graus:
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
# Componente vertical de v:
vy <- viy - g * thmax
# escreva a velocidade resultante:
vr <- 
# Mostrar comp. vertical da veloc:
vy
# Mostrar valor da veloc. result.:
vr
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Velocidad inicial:
vi <- 200
#Ângulo dado em graus:
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
# Componente vertical de v:
vy <- viy - g * thmax
# escreva a velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar comp. vertical da veloc:
vy
# Mostrar valor da veloc. result.:
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
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("Posição do projétil: ",  X, "e", Y)
cat("Componentes de v: ", vx, "e", vy)
cat("Velocidade resultante: ", vr)

Posição do projétil: 86.60254 e 30.4
Componentes de v: 43.30127 e 5.4
Velocidade resultante: 43.63668
```
> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal de v, a componente vertical de v e a velocidade resultante - todos no tempo de altura máxima:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante da altura máxima:
t <- 2.5510204081632653061224489795918
# Componente horizontal de vi:
vix <- 43.30127
# Componente vertical de vi:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# vx é igual a vix:
vx <- vix
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A posição do projétil na hmax equivale a",  X, "e", Y)
cat("As componentes de v equivale a ", vx, "e", vy)
cat("A vr no tempo dado equivale a ", vr)

A posição do projétil na hmax equivale a 110.4624 e 31.88776
As componentes de v equivale a  43.30127 e 0
A vr no tempo dado equivale a  43.30127
```
<p align="justify">Observe que o valor de X na altura máxima equivale a 110,4624 m, a metade do alcance (A = 220,9248m). Observe também que o valor de Y, para esse tempo exato, equivale à altura máxima (31.88776). Observe que a componente da velocidade na horizontal (vx = vix), em um dado tempo, não varia.</p>

> <p align="justify">Comandos no R para determinar, além da posição do projétil, a componente horizontal de v, a componente vertical de v e a velocidade resultante - todos no tempo de 4s):</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Instante dado:
t <- 4
# Componente horizontal de vi:
vix <- 43.30127
# Componente vertical de vi:
viy <- 25
# Posição X
X <- vix * t
# Posição Y
Y <- viy * t - (g * t ^ 2)/2 
# Componente horizontal de v:
vx <- vix
# Componente vertical de v:
vy <- viy - g * t 
# Velocidade resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
cat("A posição do projétil em 4s equivale a",  X, "e", Y)
cat("As componentes de v equivale a ", vx, "e", vy)
cat("A vr no tempo dado equivale a ", vr)

A posição do projétil em 4s equivale a 173.2051 e 21.6
As componentes de v equivale a  43.30127 e -14.2
A vr no tempo dado equivale a  45.57017
```

<p align="justify">Observe que após o tempo de altura máxima (2,5510...), no caso 4s, o projétil já está caindo e, no eixo X, o projétil já passou da metade do alcance (110,4624), no caso, 173,2051m. Observe que na queda do projétil a componente vertical da velocidade está negativa e o vetor resultante é positivo.</p>

> DEVER DE CASA - estude e execute os comandos abaixo no seu ambiente R:

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Sendo que o alcance máximo acontece quando o ângulo de lançamento é equivalente a 45°, prove que esse alcance máximo (A) é quatro vezes maior que a altura máxima (hmáx). Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. (Compare sua resposta: A altura máxima é = 255.102, O alcance é =  1020.408 e sabemos que 1020.408 é 4 vezes 255.102.</p>

```{r}
g <- 9.8
# Instante da altura máxima:
vi <- 100
# ângulo dado em graus:
angulo <- 45
# transformar graus em radianos:
teta <- (pi/180) * angulo
# componente x da vi:
vix <- vi * cos(teta)
# componente y da vi:
viy <- vi * sin(teta) 
# Tempo na altura máxima:
thmax <- viy/g
# tempo total ou de trajeto:
ttot = 2 * thmax
# altura máxima:
hmax = (viy ^ 2)/(2 * g)
# alcance
A = vix * ttot
cat("A altura máxima é = ", hmax)
cat("O alcance é = ", A)
cat(A, "é 4 vezes", hmax)
```
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

<p align="justify"> A direção do projeto em um dado instante t é determinada pelo cálculo da tangente entre a componente da velocidade na vertical e a componente da velocidade na horizontal. A expressão que calcula a tangente de um ângulo é dada por:</p>

$$tg~ \theta = \displaystyle \frac{v _{y}}{v _{x}}$$

<p align="justify"> onde, $\theta$ corresponde ao ângulo formado entre a componente horizontal e a direção da velocidade resultante num dado instante, $v _{y}$ corresponde à componente da velocidade segundo a vertical e $v _{x}$ corresponde à componente da velocidade segundo a horizontal.</p>

<p align="justify">Da expressão acima podemos encontar o valor do ângulo $\theta$:</p> 

$$\theta = arc~tg~\displaystyle \frac{v _{y}}{v _{x}}\cdot$$

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a direção do projétil ao atingir o solo. Considere $g = 9,8~m/s^{2}$, a $v _{x} = 43,30127~m/s$ e a $v _{y} = -25~m/s$ foram determinados em tópicos anteriores.</p>

> Determinando a tangente do ângulo

$$tg~ \theta = \displaystyle \frac{v _{y}}{v _{x}}= \frac{-25}{43,30127}\cong-0,57735.$$

Link para auxílio no cálculo da tangente (use números com vírgula):

[Calculadora on-line da tangente.](https://www.calculadoraconversor.com/tangente/)

> Determinando o ângulo

$$\theta = arc~tg~(-0,5773503) = -30°.$$

> <p align="justify">-30° é o ângulo formado, em relação à horizontal, no momento em que o projétil chega ao chão.</p>

Link para auxílio no cálculo do arco tangente (use números com vírgula): 

[Calculadora on-line de arco tangente.](https://www.calculadoraconversor.com/arcotangente/)

> <p align="justify">Comandos no R para determinar a direção do projétil, em relação à horizontal, ao atingir o solo:</p>

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

> <p align="justify">* Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Determine a direção do projétil ao atingir o solo. Considere $g = 9,8~m/s^{2}$, a $v _{x} = 25 m/s$ e a $v _{y} = -53~m/s$.</p>

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

<p align="justify"> Aplique os comandos utilizados em R para resolver o seguinte problema: Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 50 m/s. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.Determine: a) A altura máxima desenvolvida pelo projétil; b) O tempo gasto para chegar na altura máxima; c) O alcance desenvolvido pelo projétil; d) A velocidade da componente vertical, a velocidade resultante e a direção do projétil ao alcançar o solo; e) A posição do projétil no tempo de 5 segundos. Compare sua resposta logo abaixo.</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Vel. inicial:
vi <- 50
# ângulo dado em graus:
angulo <- 60
# transformar graus em radianos:
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
# Atribuir valor do arco tg
angulo <- atan(tang)
# Atribuir valor de angulo/(pi/180)
graus <- angulo/(pi/180)
cat("a) A hmax é igual a:", hmax)
cat("b) O thmax é igual a:", thmax)
cat("c) O alcance é igual a:", A)
cat("d) A vy:", vy, "A vr:", vr, "A direção:", graus)
cat("e) A posição em 5 segundos:", X, "e", Y)
```
> Compare sua resposta 

```{r}
a) A hmax é igual a: 95.66327
b) O thmax é igual a: 4.418497
c) O alcance é igual a: 220.9248
d) A vy: -43.30127, A vr: 50, A direção: -60
e) A posição em 5 segundos: 125 e 94.00635
```
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
