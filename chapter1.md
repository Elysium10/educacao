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
