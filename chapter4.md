--- 
title_meta  : Capítulo 4
title       : Gráficos do movimento oblíquo
description : <p align="justify">Neste capítulo você aprenderá sobre os comandos básicos do programa R, enfatizando o seu uso no dia a dia e na sala de aula. Aprenderá a criar funções básicas para usá-las em problemas de Matemática, Física, Estatística e outras ciências. Por meio do editor do texto do curso você perceberá a facilidade de uso dos comandos. Se você é aluno ou professor, terá dicas de auxílios na resolução dos problemas propostos e poderá levar a metodologia para usar em sala de aula. Será muito divertido o estudo com o auxílio da plataforma R. Seja bem vindo e bons estudos!</p>

--- type:NormalExercise lang:r xp:100 skills:1 key:c4baaf5225
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
test_output_contains("-60", incorrect_msg = "Escreva a expressão que atribua a uma variável (tang) a divisão entre as componentes vertical e horizontal da velocidade do projétil quando o mesmo alcança o tempo de trajeto.")
success_msg("Bom trabalho! Você aprendeu a determinar a direção do projétil quando o mesmo alcança o solo.")
```
