--- 
title_meta  : Capítulo 2
title       : Projeto - Lançamento Oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>
--- type:NormalExercise lang:r xp:100 skills:1 key:8ea80fa0d0
## Lançamento bolíquo

<p align="justify">Um corpo lançado obliquamente possui dois tipos de movimentos: um segundo a horizontal e o outro segundo a vertical. O movimento descrito pelo corpo, lançado segundo a horizontal, é do tipo MRU (Movimento Retilíneo Uniforme). E o outro movimento descrito pelo corpo, lançado segundo a vertical, é do tipo MRUV (Movimento Retilíneo Uniformemente Variado). A trajetória descrita pelo corpo terá a forma parabólica.</p>

> Componentes da velocidade inicial do corpo

<p align="justify">As componentes da velocidade inicial do corpo são dadas pelas seguintes equações:</p>

$$V _{ix} = V _{i}.cos(\theta)$$

e
 
$$V _{iy} = V _{i}.sen(\theta)$$

onde,

<p align="justify">$V _{i}$ representa a velocidade inicial do corpo, $V _{ix}$ representa a componente da velocidade inicial na horizontal, $V _{iy}$ representa a componente da velocidade inicial na vertical e $\theta$ representa o ângulo de lançamento do corpo.</p> 

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
vox <- vi * cos(teta)  
voy <- vi * sin(teta)  
# mostrar a componente x e y da vi:
cat("A componente x da vi é igual a:", vox)
cat("A componente y da vi é igual a:", voy)

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
vox <- vi * cos(teta)  
voy <- vi * sin(teta)  
# mostrar as componentes x e y da vi:
cat("A componente x da vi é igual a:", vox)
cat("A componente y da vi é igual a:", voy)

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
vox <- vi * cos(teta)  
voy <- vi * sin(teta)  
# mostrar as componentes x e y da vi:
vox 
voy
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
vox <- vi * cos(teta)  
voy <- vi * sin(teta)  
# mostrar as componentes x e y da vi:
vox 
voy
```
*** =sct
```{r}
test_output_contains("vox = 100 voy = 173.20511"), incorrect_msg = "Digite corretamente o valor da variável angulo. O valor da variável teta equivale a $$(pi/180)*angulo.$$.")
success_msg("Bom trabalho! Você adquiriu noções sobre componentes da velocidade inicial do lançamento oblíquo da Física.")
```