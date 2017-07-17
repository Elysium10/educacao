--- 
title_meta  : Capítulo 2
title       : Projeto - Lançamento Oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:8ea80fa0d0
## Componentes da velocidade inicial

<p align="justify">Um corpo lançado obliquamente possui dois tipos de movimentos: um segundo a horizontal e o outro segundo a vertical. O movimento descrito pelo corpo, lançado segundo a horizontal, é do tipo MRU (Movimento Retilíneo Uniforme). E o outro movimento descrito pelo corpo, lançado segundo a vertical, é do tipo MRUV (Movimento Retilíneo Uniformemente Variado). A trajetória descrita pelo corpo terá a forma parabólica.</p>

> Componentes da velocidade inicial do corpo

<p align="justify">As componentes da velocidade inicial do corpo são dadas pelas seguintes equações:</p>

$$V _{ix} = V _{i}.cos(\theta)$$

e
 
$$V _{iy} = V _{i}.sen(\theta)$$

onde,

<p align="justify">$V _{i}$ representa a velocidade inicial do corpo, $V _{ix}$ representa a componente da velocidade inicial na direção (horizontal) do eixo x, $V _{iy}$ representa a componente da velocidade inicial na direção (vertical) do eixo y e $\theta$ representa o ângulo de lançamento do corpo. Visualize a velocidade inicial e suas componentes na figura abaixo:</p>
![Componentes da velocidade inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo1.png "Componentes da velocidade inicial")

> Motivação

* <p align="justify">Um corpo é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 10 m/s<sup>2</sup>.</p> 


Dados:

$$\theta = 30°.$$ 
$$V_{i} = 50~m/s.$$ 
$$sen(30°)= 0.5.$$
$$cos(30°)\cong0.866.$$ 

<p align="justify">Observação: por enquanto, não usaremos o valor de g.</p>

> <p align="justify"> Determinando a componente da velocidade inicial na horizontal:</p>

$$V _{ix} = V _{i}.cos\theta= 50.(0.866)\cong43,30~m/s.$$

> <p align="justify"> Determinando a componente da velocidade inicial na vertical:</p>

$$V _{iy} = V _{i}.sen\theta= 50.(0.5)=25~m/s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos para calcular as componentes da velocidade inicial no R:</p>

<p align="justify">- Use o problema anterior e determine as componentes da velocidade inicial do corpo.</p>

<p align="justify">Obs.: Em R, os argumentos das funções trigonométricas, os graus, devem ser transformados em radianos da seguinte maneira: (pi/180) multiplicado pelo ângulo. Após isso, tira-se o cosseno (cos) e o seno (sin) desse resultado.</p> 

```{r}
# aceleração da gravidade:
g <- 10
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

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 10 m/s<sup>2</sup>.</p> (Compare sua resposta: A componente x da vel. inicial é igual a: 70.71068 e a componente y da vel. inicial é igual a: 70.71068).</p>

```{r}
# aceleração da gravidade:
g <- 10
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
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes da velocidade inicial. Adote a aceleração da gravidade g = 10 m/s<sup>2</sup>.</p></p>

*** =instructions
<p align="justify"> Use o código estudado neste tópico para calcular as componentes x e y da velocidade inicial.</p> 
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
g <- 10
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
g <- 10
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

$$v _{y}^{2}= v _{iy}^{2}-2gh _{máx},$$

onde,

<p align="justify">$v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $g$ é a aceleração da gravidade a qual vamos considerar como 9.8m/s<sup>2</sup> e $h _{máx}$ é a altura máxima alcançada pelo projétil.</p>

<p align="justify">Sabemos que à medida que o projétil vai atingindo a altura máxima, sua velocidade vai dimunuindo. Quando chega exatamente no ponto da altura máxima, o projétil tem sua velocidade equivalente a zero. Portanto, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), ou seja,</p>
$$0= v _{iy}^{2}-2gh _{máx}.$$
<p align="justify">Daí, podemos obter a expresão para a altura máxima atingida pelo projétil:</p>
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Tempo para o projétil atingir a altura máxima

<p align="justify">Para determinar quanto tempo o projétil levará para atingir a altura máxima, adaptaremos a equação da velocidade do MRUV para:</p>
$$v _{y}=  v _{iy} - gt _{hmáx},$$

onde, 

<p align="justify">$v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $-g$ é a aceleração da gravidade de sentido oposto ao da velocidade inicial e $t _{hmáx}$ é o tempo necessário para que o projétil alcance a altura máxima. Já sabemos que, na altura máxima, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), portanto, a equação acima torna-se</p>

$$0=v _{iy}-gt _{hmáx} \rightarrow-v _{iy}=-gt _{hmáx} \rightarrow$$ 
$$v _{iy}=gt _{hmáx} \rightarrow t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$

<p align="justify">Visualize na figura abaixo a representação de $hmáx$, $v _{y} = 0$, $v _{y}$, $g$, o alcance do projétil e todos os componentes do movimento oblíquo:</p>
![Componentes do movimento oblíquo inicial](http://s3.amazonaws.com/assets.datacamp.com/production/course_4551/datasets/Lancobliquo2.png "Componentes do movimento oblíquo")

> Motivação

* <p align="justify">Aproveitaremos o primeiro exemplo do tópico anterior: um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote, desta vez, a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Neste problema, não usaremos nem a velocidade inicial ($v _{i}$) e nem a componente da velocidade inicial ($v _{ix}$)</p> 

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

<p align="justify">- Do problema anterior, determinaremos a altura máxima e o tempo para alcançá-la.</p>

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
cat("A altura máxima alcançada pelo projétil é igual a:", hmax)
cat("O tempo gasto para atingir o ponto mais alto da trajetória é igual a:", thmax)

A altura máxima do projétil é igual a: 31.88776
O tempo gasto para atingir o ponto mais alto da trajetória é igual a: 2.55102
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
cat("A altura máxima alcançada pelo projétil é igual a:", hmax)
cat("O tempo gasto para atingir o ponto mais alto da trajetória é igual a:", thmax)
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
--- type:NormalExercise lang:r xp:100 skills:1 key:d4e07e2920
## Tempo de trajeto

> Tempo de subida e de descida

<p align="justify">O valor da altura máxima, no movimento oblíquo, é obtido adaptando-se a a equação de Torricelli para</p>

$$v _{y}^{2}= v _{iy}^{2}-2gh _{máx},$$

onde,

<p align="justify">$v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $g$ é a aceleração da gravidade a qual vamos considerar como 9.8m/s<sup>2</sup> e $h _{máx}$ é a altura máxima alcançada pelo projétil.</p>

<p align="justify">Sabemos que à medida que o projétil vai atingindo a altura máxima, sua velocidade vai dimunuindo. Quando chega exatamente no ponto da altura máxima, o projétil tem sua velocidade equivalente a zero. Portanto, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), ou seja,</p>
$$0= v _{iy}^{2}-2gh _{máx}.$$
<p align="justify">Daí, podemos obter a expresão para a altura máxima atingida pelo projétil:</p>
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Tempo para o projétil atingir a altura máxima

<p align="justify">Para determinar quanto tempo o projétil levará para atingir a altura máxima, adaptaremos a equação da velocidade do MRUV para:</p>
$$v _{y}=  v _{iy} - gt _{hmáx},$$

onde, 

<p align="justify">$v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $-g$ é a aceleração da gravidade de sentido oposto ao da velocidade inicial e $t _{hmáx}$ é o tempo necessário para que o projétil alcance a altura máxima. Já sabemos que, na altura máxima, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), portanto, a equação acima torna-se</p>

$$0=v _{iy}-gt _{hmáx} \rightarrow-v _{iy}=-gt _{hmáx} \rightarrow$$ 
$$v _{iy}=gt _{hmáx} \rightarrow t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$

<p align="justify">Visualize na figura abaixo a representação de $hmáx$, $v _{y} = 0$, $v _{y}$, $g$, o alcance do projétil e todos os componentes do movimento oblíquo:</p>
![Componentes do movimento oblíquo inicial]( "Componentes do movimento oblíquo")

> Motivação

* <p align="justify">Aproveitaremos o primeiro exemplo do tópico anterior: um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima e o tempo necessário para atingir esta altura. Adote, desta vez, a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. Neste problema, não usaremos nem a velocidade inicial ($v _{i}$) e nem a componente da velocidade inicial ($v _{ix}$)</p> 

<p align="justify">Observação: no tópico anterior foi determinado a componente da velocidade inicial, $v _{iy}$.</p>

Dado:

$$v _{iy} = 25~m/s.$$

> <p align="justify"> A altura máxima:</p>

$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}= \displaystyle \frac{25^{2}}{2.9,8}= \displaystyle \frac{625}{19,6}\cong 31,88~m.$$

> <p align="justify"> O tempo para atingir a altura máxima:</p>

$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}=\displaystyle\frac{25}{9,8}\cong 2,55~s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.]()

> <p align="justify">Comandos no R para calcular a altura máxima e o tempo para alcançá-la:</p>

<p align="justify">- Do problema anterior, determinaremos a altura máxima e o tempo para alcançá-la.</p>

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
cat("A altura máxima alcançada pelo projétil é igual a:", hmax)
cat("O tempo gasto para atingir o ponto mais alto da trajetória é igual a:", thmax)

A altura máxima do projétil é igual a: 31.88776
O tempo gasto para atingir o ponto mais alto da trajetória é igual a: 2.55102
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
cat("A altura máxima alcançada pelo projétil é igual a:", hmax)
cat("O tempo gasto para atingir o ponto mais alto da trajetória é igual a:", thmax)
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