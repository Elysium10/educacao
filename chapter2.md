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

> <p align="justify"> Como determinar as componentes da velocidade inicial do projétil em R</p>

```{r}
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
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine as componentes da velocidade inicial.<p> 
*** =instructions
<p align="justify"> Use o código estudado neste tópico para calcular as componentes x e y da velocidade inicial(vi).</p> 

*** =hint
<p align="justify"> - O ângulo dado equivale a 60° e a variável teta equivale a</p> 
$$(pi/180)*angulo.$$ 
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Velocidad inicial(vi):
vi <- 200
# Escreva o ângulo dado em graus:
angulo <- 
# Escreva graus em radianos:
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
# Velocidad inicial(vi):
vi <- 200
# Escreva o ângulo dado em graus:
angulo <- 60
# Escreva graus em radianos:
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
--- type:NormalExercise lang:r xp:100 skills:1 key:0a2b6cd71d
## Atividade - Componentes da velocidade inicial

<p align="justify">Num lançamento oblíquo, quando o ângulo de elevação equivale a 45°, o alcance do projétil é máximo e as componentes da velocidade inicial possuem valores iguais. No decorrer do curso observaremos também que, quando o ângulo  equivale a 45°, o valor do alcance máximo é quatro vezes o valor da altura máxima alcançada pelo projétil.</p> 

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>

<p align="justify"> Um projétil é lançado a partir do solo com uma velocidade inicial igual a 100 m/s, formando com o mesmo um ângulo de 45°. Determine as componentes da velocidade inicial.</p>

*** =instructions
<p align="justify"> - Calcularemos as componentes da velocidade inicial (vi) pra  45°.</p> 
<p align="justify"> - Você irá completar as expressões que calculam as componentes vix e viy.</p>
<p align="justify"> - Obs.: clicando no R Console e depois utilizando as teclas Control + L, você pode limpar os dados do console.</p>
*** =hint
<p align="justify"> - Os valores das componentes vix e viy são dados pelas seguintes equações:</p>
$$v _{ix} = v _{i}.cos(\theta)$$
e
$$v _{iy} = v _{i}.sen(\theta)$$ 
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Velocidad inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# Escreva vix:
vix <- vi *   
# Escreva viy:
viy <- vi *   
# Mostrar vix:
vix
# Mostrar viy:
viy
```
*** =solution
```{r}
# Velocidad inicial:
vi <- 100
# Ângulo em graus:
angulo <- 45
# Graus em radianos:
teta <- (pi/180) * angulo
# Escreva vix:
vix <- vi * cos(teta)  
# Escreva viy:
viy <- vi * sin(teta)  
# Mostrar vix:
vix
# Mostrar viy:
viy
```
*** =sct
```{r}
test_output_contains("70.71068", incorrect_msg = "Digite corretamente as expressões que determinan os valores das componentes da velocidade inicial.")
success_msg("Bom trabalho! Você observou que, quando o ângulo de elevação equivale a 45°, as componentes da velocidade inicial possuem valores iguais.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:863cc9aee1
## Altura máxima

<p align="justify">O valor da altura máxima, no movimento oblíquo, é obtido adaptando-se a a equação de Torricelli para</p>

$$v _{y}^{2}= v _{iy}^{2}-2gh _{máx}$$

<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $g$ é a aceleração da gravidade a qual vamos considerar como 9.8m/s<sup>2</sup> e $h _{máx}$ é a altura máxima alcançada pelo projétil.</p>

<p align="justify">Sabemos que à medida que o projétil vai atingindo a altura máxima, sua velocidade vai dimunuindo. Quando chega exatamente no ponto da altura máxima, o projétil tem sua velocidade equivalente a zero. Portanto, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), ou seja,</p>
$$0= v _{iy}^{2}-2gh _{máx}.$$
<p align="justify">Daí, podemos obter a expresão para a altura máxima alcançada pelo projétil:</p>
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow$$ 
$$v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima alcançado pelo projétil. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p> 

<p align="justify">No tópico anterior foi determinado a componente da velocidade inicial, $v _{iy}$.</p>

Dado:

$$v _{iy} = 25~m/s.$$

> <p align="justify"> A altura máxima:</p>

$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}= \displaystyle \frac{25^{2}}{2.9,8}= \displaystyle \frac{625}{19,6}\cong 31,88~m.$$

> <p align="justify">Comandos no R para calcular a altura máxima:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 25
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Mostrar a hmax:
cat("A altura máxima é", hmax)

A altura máxima é 31.88776
```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a altura máxima atingida pelo projétil. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>

<style type="text/css">
.letras{
width:580px;line-height:1.5;position:relative; text-align:justify;font-family:Calibri;font-size:20px;line-height:1.5em;border:#7FFF00 2px none;
padding:5px;border-radius:5px;-moz-border-radius:5px; -webkit-border-radius:5px;background:#DDD url(https://lh6.googleusercontent.com/-0X8KQIRPiuY/UxY5KmzdpsI/AAAAAAAABAo/RqqhQIR7Gf4/s800/pattern.png) repeat; text-shadow:1px 1px #fff;
box-shadow:0 0 0 6px #33a0c2;
}
</style>
<body>
<div class="letras">

<p align="justify">O valor da altura máxima, no movimento oblíquo, é obtido adaptando-se a a equação de Torricelli para</p>

$$v _{y}^{2}= v _{iy}^{2}-2gh _{máx}$$

<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $g$ é a aceleração da gravidade a qual vamos considerar como 9.8m/s<sup>2</sup> e $h _{máx}$ é a altura máxima alcançada pelo projétil.</p>

<p align="justify">Sabemos que à medida que o projétil vai atingindo a altura máxima, sua velocidade vai dimunuindo. Quando chega exatamente no ponto da altura máxima, o projétil tem sua velocidade equivalente a zero. Portanto, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), ou seja,</p>
$$0= v _{iy}^{2}-2gh _{máx}.$$
<p align="justify">Daí, podemos obter a expresão para a altura máxima alcançada pelo projétil:</p>
$$-v _{iy}^{2}= -2gh _{máx}\rightarrow$$ 
$$v _{iy}^{2}= 2gh _{máx}\rightarrow$$ 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a altura máxima alcançado pelo projétil. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p> 

<p align="justify">No tópico anterior foi determinado a componente da velocidade inicial, $v _{iy}$.</p>

Dado:

$$v _{iy} = 25~m/s.$$

> <p align="justify"> A altura máxima:</p>

$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}= \displaystyle \frac{25^{2}}{2.9,8}= \displaystyle \frac{625}{19,6}\cong 31,88~m.$$

> <p align="justify">Comandos no R para calcular a altura máxima:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 25
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Mostrar a hmax:
cat("A altura máxima é", hmax)

A altura máxima é 31.88776
```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine a altura máxima atingida pelo projétil. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
</div>
</body>

*** =instructions
<p align="justify"> - Use o código estudado neste tópico para calcular altura máxima.</p> 
<p align="justify"> - Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>e a componente vertical da velocidade inicial, determinado em tópico anterior, equivale a 173,2051.</p>
<p align="justify"> - Escreva a expressão para determinar a altura máxima.</p>
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
g <- 9.8
# Componente viy:
viy <- 173.2051
# Escreva altura máxima:
hmax <- 
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax:
hmax
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 173.2051
# Escreva altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax:
hmax
```
*** =sct
```{r}
test_output_contains("1530.613", incorrect_msg = "Digite corretamente a expressão para determinar a altura máxima alcançada pelo projétil.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular a altura máxima alcançada pelo projétil.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:218ca06138
## Atividade - Altura máxima

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo com uma velocidade inicial igual a 200m/s, formando com o mesmo um ângulo de 45°. Determine a altura máxima alcançada pelo projétil. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>

*** =instructions
<p align="justify"> Use o código estudado neste tópico para calcular altura máxima.</p> 
<p align="justify"> Escreva o valor da aceleração da gravidade adotada neste estudo e a expressão para a altura máxima.
<p align="justify"> A componente vertical da velocidade inicial é equivalente a 173.2051, calculado no tópico anterior.</p>
*** =hint
<p align="justify"> A altura máxima no movimento oblíquo é dada pela seguinte expressão:</p> 
$$h _{máx}= \displaystyle \frac{v _{iy}^{2}}{2g}\cdot$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Escreva acel. gravidade:
g <- 9.8
# Componente viy:
viy <- 70.71068
# Escreva altura máxima:
hmax <- 
# Mostrar hmax
hmax
```
*** =solution
```{r}
# Escreva acel. gravidade:
g <- 9.8
# Componente viy:
viy <- 70.71068
# Escreva altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Mostrar hmax
hmax
```
*** =sct
```{r}
test_output_contains("255.1021", incorrect_msg = "Digite corretamente o valor da aceleração da gravidade e a expressão para a altura máxima alcançada pelo projétil.")
success_msg("Bom trabalho! Você adquiriu mais noções sobre como calcular a altura máxima alcançada pelo projétil e o tempo gasto para atingí-la.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:7c6dfaabfd
## Tempo de subida

<p align="justify">Para determinar quanto tempo o projétil levará para atingir a altura máxima, adaptaremos a equação da velocidade do MRUV para:</p>
$$v _{y}=  v _{iy} - gt _{hmáx}$$
<p align="justify">onde, $v _{y}$ é a componente vertical da velocidade no instante t, $v _{iy}$ é a componente da velocidade inicial na direção (vertical) y, $-g$ é a aceleração da gravidade de sentido oposto ao da velocidade inicial e $t _{hmáx}$ é o tempo necessário para que o projétil alcance a altura máxima. Já sabemos que, na altura máxima, a velocidade do corpo na direção vertical torna-se nula ($v _{y}$ = 0), portanto, a equação acima torna-se</p>

$$0=v _{iy}-gt _{hmáx} \rightarrow$$
$$-v _{iy}=-gt _{hmáx} \rightarrow$$
$$v _{iy}=gt _{hmáx} \rightarrow$$
$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$

> Motivação

* <p align="justify">Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p> 

> <p align="justify"> O tempo para atingir a altura máxima:</p>

$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}=\displaystyle\frac{25}{9,8}\cong 2,55~s.$$

<p align="justify"> Auxílio para simular um lançamento de projéteis, acesse o link abaixo e clique em "Disparar".</p>

[Lançamento de projéteis.](https://phet.colorado.edu/sims/projectile-motion/projectile-motion_pt_BR.html)

> <p align="justify">Comandos no R para calcular a altura máxima:</p>

```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 25
# Tempo da hmax
thmax <- viy/g
# Mostrar a hmax e o thmax:
cat("O tempo até a hmax é", thmax)

O tempo até a hmax é 2.5510204081632653061224489795918
```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine o tempo necessário para atingir a altura máxima. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>

*** =instructions
<p align="justify"> Determinaremos o tempo necessário para atingir a altura máxima.</p> 
<p align="justify"> Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>e a componente vertical da velocidade inicial, calculado anteriormente, equivale a 173.2051..</p>
*** =hint
<p align="justify"> O tempo necessário para que o projétil alcance a altura máxima é dado pela seguinte expressão:</p> 
$$$$t _{hmáx}= \displaystyle \frac{v _{iy}}{g}\cdot$$$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 173.2051
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Escreva tempo na hmax:
thmax <-  
# Mostrar thmax:
thmax
```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 173.2051
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Escreva tempo na hmax:
thmax <- viy/g
# Mostrar thmax:
thmax
```
*** =sct
```{r}
test_output_contains("17.67399", incorrect_msg = "Escreva a expressão que determina o valor do tempo necessário para que o projétil alcance a altura máxima.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular o tempo gasto para o projétil alcançar a altura máxima.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:e1a3b0c037
## Atividade - Tempo de subida

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Determine o tempo necessário para atingir esta altura. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>. A componente y da vel. inicial é igual a: 70.71068 - calculada em tópico anterior.</p>

*** =instructions
<p align="justify"> Mostre na tela o tempo que o projétil gasta para atingir a altura máxima.</p> 
<p align="justify"> Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>e a componente vertical da velocidade inicial equivalente a 70.71068, calculado anteriormente.</p>
*** =hint
<p align="justify"> Para mostrar na tela o tempo que o projétil gasta para atingir a altura máxima, basta digitar thmax.</p> 

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 70.71068
# Tempo até a hmax:
thmax <- viy/g
# Escreva como mostrar thmax:

```
*** =solution
```{r}
# Aceleração da gravidade:
g <- 9.8
# Componente viy:
viy <- 70.71068
# Tempo até a hmax:
thmax <- viy/g
# Escreva como mostrar thmax:
thmax
```
*** =sct
```{r}
test_output_contains("17.67399", incorrect_msg = "Digite corretamente o valor da aceleração da gravidade e a expressão para a altura máxima alcançada pelo projétil.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular a altura máxima alcançada pelo projétil e o tempo gasto para atingí-la.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:12980fa718
## Tempo de trajeto

<p align="justify">Neste estudo estamos desprezando a resistência do ar, por isso o tempo que o projétil leva para atingir a altura máxima (tempo de subida) é o mesmo tempo gasto para voltar da altura máxima até o solo (tempo de descida). Portanto, o tempo total gasto em todo o trajeto pode ser  dado pela seguinte expressão:</p>
$$t _{tot} = 2t _{hmáx}$$
<p align="justify">onde, $t _{tot}$ corresponde ao tempo total ou tempo de trajeto e $t _{hmáx}$ ao tempo necessário para o projétil alcançar a altura máxima.</p>

> Motivação

* <p align="justify"> Um projétil é lançado obliquamente, a partir do solo, com uma velocidade inicial igual a 50m/s e um ângulo de lançamento igual a 30°. Determine o tempo gasto pelo projétil até sua chegada no solo. Dados: $9,8~m/s^{2}$. O $t _{hmáx}=2,55~s$ e a $v _{ix}=43,30127~m/s$ já foram determinados anteriormente.</p>

<p align="justify">O tempo de trajeto pode ser determinado por:</p> 

$$t _{tot} = 2t _{hmáx} = 2.2,55 = 5,1~s.$$

> <p align="justify">Comandos no R para calcular o tempo de trajeto:</p>

```{r}
# Dado a componente vix:
vix <- 43.30127
# Dado o tempo da hmax:
thmax <- 2.5510204081632653061224489795918
# Tempo total:
ttot <- 2 * thmax
cat("O tempo de trajeto é", ttot)

O tempo de trajeto é 5.102041
```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado obliquamente, a partir do solo, com uma velocidade inicial igual a 100m/s e um ângulo de lançamento igual a 45°. Calcule todos os elementos do lançamento oblíquo, visto até agora. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>

*** =instructions
<p align="justify"> - Determine no R as componentes da velocidade inicial vix e viy, a altura máxima, o tempo de subida, o tempo de descida e o tempo de trajeto do projétil.</p> 
<p align="justify"> - Escreva a expressão do tempo de trajeto.</p>
*** =hint
<p align="justify"> O tempo total gasto em todo o trajeto pode ser  dado pela seguinte expressão:</p>
$$t _{tot} = 2t _{hmáx}$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
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
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O thmax é", thmax)
# Tempo descida = tempo de subida:
td <- thmax
cat("O tempo de descida é", td)
# Escreva tempo de trajeto:
ttot <- 
# Mostrar tempo total:
ttot
```
*** =solution
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
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O thmax é", thmax)
# Tempo descida = tempo de subida:
td <- thmax
cat("O tempo de descida é", td)
# Escreva tempo de trajeto:
ttot <- 2 * thmax
# Mostrar tempo total:
ttot
```
*** =sct
```{r}
test_output_contains("14.43075", incorrect_msg = "Veja nas dicas qual é a expressão que determina o tempo gasto em toda a trajetória.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular o tempo de trajeto no movimento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:b95850435c
## Atividade - Tempo de trajeto

<p align="justify">Já sabemos que o tempo de trajeto equivale a duas vezes o tempo que o projétil gasta para atingir a altura máxima.</p>

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>

<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 60°, com uma velocidade inicial igual a 200 m/s. Determine todos os elementos do lançamento oblíquo visto até agora. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Use os códigos estudados no tópico sobre o tempo de trajeto para calcular todos os elementos do lançamento oblíquo visto até agora.</p> 
<p align="justify"> - Escreva a expressão para a componente vix e para o tempo de trajeto.</p>

*** =hint
<p align="justify"> O valor da componente da velocidade inicial na direção vertical e do tempo de trajeto são dados, respectivamente, por
$$v _{iy} = v _{i}.sin(\theta)$$
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
# Componente vix:
vix <- vi * cos(teta)
# Escreva a componente viy:
viy <-   
# Mostrar compon. vix:
vix
# Mostrar compon. viy:
viy
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax:
hmax
# Mostrar thmax:
thmax
# Escreva o tempo total:
ttot <- 
# Mostrar ttot:
ttot
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
# Componente vix:
vix <- vi * cos(teta)
# Escreva a componente viy:
viy <- vi * sin(teta)  
# Mostrar compon. vix:
vix
# Mostrar compon. viy:
viy
# Altura máxima:
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax:
thmax <- viy/g
# Mostrar hmax:
hmax
# Mostrar thmax:
thmax
# Escreva o tempo total:
ttot <- 2 * thmax
# Mostrar ttot:
ttot
```
*** =sct
```{r}
test_output_contains("35.34798", incorrect_msg = "Veja nas dicas as expressões que determinam o valor da componente da velocidade inicial e o valor do tempo gasto em toda trajetória.")
success_msg("Bom trabalho! Você adquiriu mais noções sobre a o tempo de trajeto de um projétil no movimento oblíquo.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:0da2105cd7
## Alcance

<p align="justify"> Sabemos que o movimento do projétil, na direção horizontal, é do tipo Movimento Retilíneo Uniforme (MRU). Para determinar o alcance, ou seja, a distância percorrida pelo projétil da posição de lançamento até tocar no solo, adaptaremos a equação do espaço do MRU ($X= v _{ix}.t$) para</p>
$$A=v _{ix}.t _{tot}$$
<p align="justify">onde $A$ corresponde ao alcance, $v _{ix}$ à componente da velocidade inicial na direção X, e $t _{tot}$ ao tempo total ou tempo de trajeto.</p>

> Motivação

* <p align="justify"> Um projétil é lançado a  partir do solo, formando com o mesmo um ângulo de 30°, com uma velocidade inicial igual a 50 m/s. Determine a o tempo total gasto e o alcance do projétil. Dados: $9,8~m/s^{2}$. O $t _{hmáx}=2,55~s$ e a $v _{ix}=43,30127~m/s$ já foram determinados anteriormente.</p>

<p align="justify">Já sabemos que o tempo de trajeto pode ser determinado por:</p> 

$$t _{tot} = 2t _{hmáx} = 2.2,55 = 5,1~s.$$

<p align="justify">O alcance do projétil pode ser determinado por:</p>

$$A=v _{ix}.t _{tot} =  43,30127.5,1 = 220,83 m/s.$$

> <p align="justify">Comandos no R para calcular o tempo de trajeto e o alcance:</p>

```{r}
# Componente vix:
vix <- 43.30127
# Tempo da hmax:
thmax <- 2.5510204081632653061224489795918
# Tempo total:
ttot <- 2 * thmax
# Alcance:
A = vix * ttot
cat("O tempo de trajeto é", ttot)
cat("O alcance é ", A)

O tempo de trajeto é 5.102041
O alcance é 220.9248
```
<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo, formando com o mesmo um ângulo de 45°, com uma velocidade inicial igual a 100 m/s. Calcular os elementos do lançamento oblíquo. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Determinar os elementos do lançamento oblíquo visto até agora.</p> 
<p align="justify"> - Escreva a expressão que determina o alcance máximo do projétil.</p>
*** =hint
<p align="justify"> - A expressão que determina o alcance máximo do projétil é dada por </p> 
$$A=v _{ix}.t _{tot}$$
*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
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
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax
thmax <- viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O thmax é", thmax)
# Tempo total ou de trajeto:
ttot <- 2 * thmax
# Mostrar tempo trajeto:
cat("O tempo total é", ttot)
# Escrever alcance máximo:
A <- 
# Mostrar o Alcance máximo
A
```
*** =solution
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
hmax <- (viy ^ 2)/(2 * g)
# Tempo da hmax
thmax <- viy/g
# Mostrar hmax e thmax:
cat("A altura máxima é", hmax)
cat("O thmax é", thmax)
# Tempo total ou de trajeto:
ttot <- 2 * thmax
# Mostrar tempo trajeto:
cat("O tempo total é", ttot)
# Escrever alcance máximo:
A <- vix * ttot
# Mostrar o Alcance máximo
A
```
*** =sct
```{r}
test_output_contains("1020.408", incorrect_msg = "Veja nas dicas a expressão que determina o valor do alcance máximo do projétil.")
success_msg("Bom trabalho! Você adquiriu noções sobre como calcular o alcance máximo de um projétil.")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:c0c16b98ca
## Atividade - Alcance

<p style="background-color:#33a0c2; font-weight: bold; font-size: 20px; text-align:center"><font color="#ffffff">EXERCÍCIO PROPOSTO</font></p>
<p align="justify"> Um projétil é lançado a partir do solo com uma velocidade inicial igual a 200 m/s e formando um ângulo de lançamento igual a 60°. Determine os elementos do lançamento oblíquo. Adote a aceleração da gravidade g = 9.8 m/s<sup>2</sup>.</p>
*** =instructions
<p align="justify"> - Determinar os elementos do lançamento oblíquo.</p> 
<p align="justify"> - Escreva a expressão que determina o alcance máximo e o tempo de trajeto do projétil.</p>
*** =hint
<p align="justify"> - As expressões que determinam o tempo de trajeto e o alcance máximo do projétil é dada, respectivamente, por </p> $$t _{tot} = 2t _{hmáx}$$
e
$$A=v _{ix}.t _{tot}$$
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
ttot <- 
# Escreva o alcance
A <- 
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
# Escreva o alcance
A <- vix * ttot
# Mostrar ttot e A:
ttot
A
```
*** =sct
```{r}
test_output_contains("3534.798", incorrect_msg = "Veja nas dicas as expressões que dão o valor do tempo de trajeto e o alcance máximo de um projétil no movimento oblíquo.")
success_msg("Bom trabalho! Você adquiriu mais noções sobre como calcular o tempo de trajeto e o alcance máximo de um projétil no movimento oblíquo.")
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
<p align="justify"> - Use os comandos estudados neste tópico para calcular a componente vertical da velocidade e a velocidade resultante do projétil no tempo da altura máxima.</p>
<p align="justify"> - Escreva a expressão para a velocidade resultante do projétil.</p>
*** =hint
<p align="justify"> - O valor da velocidade resultante no movimento oblíquo é dado pela seguinte expressão:</p>
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
# Escreva a veloc. resultante:
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
# Escreva a veloc. resultante:
vr <- sqrt(vx ^ 2 + vy ^ 2)
# Mostrar vy:
vy
# Mostrar vr:
vr
```
*** =sct
```{r}
test_output_contains("100", incorrect_msg = "Escreva corretamente a expressão que calcula a velocidade resultante. Veja nas dicas a expressão que usamos para determinar a velocidade resultante.")
success_msg("Bom trabalho! Você aprendeu a determinar o valor de vy e o valor da velocidade resultante do projétil quando o mesmo alcança a altura máxima.")
```