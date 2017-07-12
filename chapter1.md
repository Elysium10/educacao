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

> <p align="center">É o valor que mais se aproxima do valor real de uma medida. Para obtê-la basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas.</p>

<p align="justify">Por exemplo, numa experiência foram obtidas as seguintes medidas: 4m, 5m, 8m, 9m, 5m. Em R a média aritmética $\bar{x}$ pode ser calculada da seguinte maneira:</p>

```{r}
x <- c(4, 5, 8, 9, 5)
mean(x)
```
<p align="justify">Nos comandos acima podemos observar que um vetor c, formado pelas medidas dadas, foi armazenado em uma variável x. Por meio do comando mean(x) é obtido a média das medidas, ou seja, o comando mean(x) vai somar 4 + 5 + 8 + 9 + 5, dividir o resultado por 5 e mostrá-lo na tela assim que teclarmos em 'Submit Answer', no editor do ambiente R.</p>

> <p align="center">Atividade - cálculo de $\bar{x}$</p>

* Calcule a média aritmética das seguintes medidas: 10, 20, 30, 50, 100, 123, 233.

*** =instructions

- Use o mesmo procedimento feito no código deste tópico.

- O vetor é c(10, 20, 30, 50, 100, 123, 233). Armazene-o numa variável x.

*** =hint
Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x e use o comando mean(x)

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Escreva o comando para atribuir a uma variável x os números 10, 20, 30, 50, 100, 123, 233
x <- 
# Determine a média: 
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
success_msg("Bom trabalho! Agora você sabe calcular a média aritmética usando o R!")
```
--- type:NormalExercise lang:r xp:100 skills:1 key:dd48eb091a
## Média harmônica (H)

> A média harmônica entre números reais e positivos é definida como o quociente entre a quantidade (n) de números pela soma dos inversos desses números. A média harmônica tmabém é deifinida como sendo o inverso da média aritmética do inverso destes números. Simbolicamente, temos

$$H = \displaystyle \frac{n}{\frac{1}{X1}+\frac{1}{X2}+ \frac{1}{X3}+...+\frac{1}{Xi}},$$

ou de uma maneira mais compacta:

$$H = \displaystyle \frac{n} { \displaystyle \sum_{i=1}^{n} \left(\frac{1}{Xi} \right)}\cdot$$

Exemplos de como é calculada a média harmônica no R:

```{r}
x <- c(3, 8, 5, 10.5)
1/mean(1/x)
[1] 5.308057
```
ou

```{r}
x <- c(3, 8, 5, 10.5)
(1/4*sum(1/c(3, 8, 5, 10.5)))^(-1)
[1] 5.308057
```
> Aplicação 1

* Um móvel se desloca até uma certa cidade com uma velocidade média de 18 km/h. Depois retorna pelo mesmo percurso com uma velocidade média de 72 km/h. Determine a velocidade média do percurso completo (ida e volta).

$$H = \displaystyle \frac{2} { \displaystyle \frac{1}{18} +\frac{1}{72}}=\displaystyle \frac{2} {\displaystyle\frac{5}{72}}=\displaystyle\frac{144}{5}=28.8~km/h \cdot $$

- No seu ambiente R, exercite os códigos abaixo:

```{r}
# Atribui à variável x o vetor c
x <- c(18,72)
# Determina o inverso média do inverso dos números 
# contidos na variável x
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

* Uma motocicleta percorreu a distância entre duas cidades, com velocidade média de 60 km/h e fez a viagem de regresso com velocidade média de 40 km/h. Determine qual foi a velocidade média do percurso total, de ida e volta.

$$H = \displaystyle \frac{2} { \displaystyle \frac{1}{60} +\frac{1}{40}}=\displaystyle \frac{2} {\displaystyle\frac{5}{120}}=\displaystyle\frac{240}{5}=48~km/h \cdot $$

- No seu ambiente R, exercite o código abaixo:

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

### Atividade

> Encontre a média harmônica entre 2, 5 e 10.

*** =instructions

* Aplique o comando para encontrar a média entre os números 2, 5, 10;

* Um auxílio para comparar cálculos de média harmônica pode ser encontrado neste link: 
[Cálculo de média harmônica.](http://www.gyplan.com.br/pt/harmonic_mean_pt.html)

*** =hint

- Atribua à variável x um vetor contendo os três números.

- O vetor deve começar com c. Assim: c(3,5,10).

- Observação: a solução matemática é 

$$H = \displaystyle \frac{3} { \displaystyle \frac{1}{2} +\frac{1}{5} + \frac{1}{10}}$$
$$ =\displaystyle \frac{3} {\displaystyle {\frac{13}{15}}}=\displaystyle\frac{45}{13}\cong3.46.$$


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
46
```
*** =sct
```{r}
test_output_contains("46", incorrect_msg = "Os números devem estar separados com vírgula e antecedidos pela letra c. Após isso, tecle em 'Submit Answer'.")
success_msg("Bom trabalho! Você adquiriu noções sobre média harmônica aplicada na Física em velocidades médias e em números.")
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

$$\sqrt{log(1)}+\sqrt{log(10)}+\sqrt{log(100)}+ \sqrt{log(1000)}+\sqrt{log(10000)}+ \sqrt{log(100000)}+\sqrt{log(10000000)}$$

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