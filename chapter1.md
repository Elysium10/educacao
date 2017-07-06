
---
title       : Introdução 
description : Insert the chapter description here
attachments :
--- type:NormalExercise lang:r xp:100 skills:1 key:aad1409c3d

## Comandos básicos do R

<table
style="background-color: rgb(204, 204, 255); height: 370px; width: 570px;"
border="1">
  <tbody>
    <tr align="center">
      <td style="vertical-align: top; background-color: rgb(5, 10, 5); text-align: center; width: 167px;" colspan="4" rowspan="1"><span style="background-color: white; color: white;"></span><big><big><big><span style="color: white;">COMANDOS BÁSICOS DO R</span></big></big></big><br>
      </td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; background-color: rgb(204, 255, 255); text-align: center; color: rgb(0, 0, 153); font-weight: bold;">Digitar e teclar Enter<br>
</td>
      <td style="vertical-align: top; background-color: rgb(204, 255, 255); color: rgb(0, 0, 153); width: 98px; text-align: center; font-weight: bold;">Resultado</td>
      <td style="vertical-align: top; width: 167px; background-color: rgb(204, 255, 255); color: rgb(0, 0, 153); text-align: center; font-weight: bold;">Digitar e teclar Enter</td>
      <td style="vertical-align: top; width: 98px; background-color: rgb(204, 255, 255); color: rgb(0, 0, 153); text-align: center; font-weight: bold;">Resultado</td>
    </tr>
<tr>
      <td style="vertical-align: top; text-align: center; width: 182px; background-color: rgb(147, 255, 39); color: red;">

```{r}
cos(x)
```
</td>
      <td style="vertical-align: top; background-color: white; color: black; text-align: center; width: 98px;">
      
```{r}
x <- 30
cos(30)
```   
scale="1.5" height="16" width="12"></td>
      <td style="vertical-align: top; text-align: center; width: 167px; background-color: rgb(147, 255, 39); color: red;">\sim</td>
      <td style="vertical-align: top; background-color: white; text-align: center; width: 98px;"><img src="https://s0.wp.com/latex.php?latex=%5Csim&bg=ffffff&fg=7c705e&s=0" alt="\sim" title="\sim" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csim&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="5" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; text-align: center; width: 182px; background-color: rgb(147, 255, 39); color: red;">\subset</td>
      <td style="vertical-align: top; background-color: white; color: black; text-align: center; width: 98px;"><img src="https://s0.wp.com/latex.php?latex=%5Csubset&bg=ffffff&fg=7c705e&s=0" alt="\subset" title="\subset" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csubset&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="11"></td>
      <td style="vertical-align: top; text-align: center; width: 167px; background-color: rgb(147, 255, 39); color: red;">\ll</td>
      <td style="vertical-align: top; background-color: white; text-align: center; width: 98px;"><img src="https://s0.wp.com/latex.php?latex=%5Cll&bg=ffffff&fg=7c705e&s=0" alt="\ll" title="\ll" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cll&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\leq</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cleq&bg=ffffff&fg=7c705e&s=0" alt="\leq" title="\leq" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cleq&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\equiv</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cequiv&bg=ffffff&fg=7c705e&s=0" alt="\equiv" title="\equiv" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cequiv&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="8" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\geq</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cgeq&bg=ffffff&fg=7c705e&s=0" alt="\geq" title="\geq" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cgeq&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\gg</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cgg&bg=ffffff&fg=7c705e&s=0" alt="\gg" title="\gg" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cgg&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\doteq</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cdoteq&bg=ffffff&fg=7c705e&s=0" alt="\doteq" title="\doteq" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cdoteq&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\propto</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpropto&bg=ffffff&fg=7c705e&s=0" alt="\propto" title="\propto" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpropto&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="8" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\bigotimes</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cbigotimes&bg=ffffff&fg=7c705e&s=0" alt="\bigotimes" title="\bigotimes" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cbigotimes&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="18"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\ni</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cni&bg=ffffff&fg=7c705e&s=0" alt="\ni" title="\ni" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cni&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\in</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cin&bg=ffffff&fg=7c705e&s=0" alt="\in" title="\in" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cin&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\prec</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cprec&bg=ffffff&fg=7c705e&s=0" alt="\prec" title="\prec" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cprec&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\succ</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csucc&bg=ffffff&fg=7c705e&s=0" alt="\succ" title="\succ" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csucc&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\vdash</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvdash&bg=ffffff&fg=7c705e&s=0" alt="\vdash" title="\vdash" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvdash&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\dashv</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cdashv&bg=ffffff&fg=7c705e&s=0" alt="\dashv" title="\dashv" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cdashv&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\preceq</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpreceq&bg=ffffff&fg=7c705e&s=0" alt="\preceq" title="\preceq" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpreceq&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\succeq</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csucceq&bg=ffffff&fg=7c705e&s=0" alt="\succeq" title="\succeq" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csucceq&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\models</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmodels&bg=ffffff&fg=7c705e&s=0" alt="\models" title="\models" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmodels&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="13"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\perp</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cperp&bg=ffffff&fg=7c705e&s=0" alt="\perp" title="\perp" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cperp&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">-</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=-&bg=ffffff&fg=7c705e&s=0" alt="-" title="-" class="latex" srcset="https://s0.wp.com/latex.php?latex=-&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="1" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\parallel</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cparallel&bg=ffffff&fg=7c705e&s=0" alt="\parallel" title="\parallel" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cparallel&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="4"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">!</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%21&bg=ffffff&fg=7c705e&s=0" alt="!" title="!" class="latex" srcset="https://s0.wp.com/latex.php?latex=%21&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="3"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\mid</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmid&bg=ffffff&fg=7c705e&s=0" alt="\mid" title="\mid" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmid&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="2"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\pm</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpm&bg=ffffff&fg=7c705e&s=0" alt="\pm" title="\pm" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpm&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">+</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%2B&bg=ffffff&fg=7c705e&s=0" alt="+" title="+" class="latex" srcset="https://s0.wp.com/latex.php?latex=%2B&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\mp</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmp&bg=ffffff&fg=7c705e&s=0" alt="\mp" title="\mp" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmp&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\times</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctimes&bg=ffffff&fg=7c705e&s=0" alt="\times" title="\times" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctimes&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="8" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\prod</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cprod&bg=ffffff&fg=7c705e&s=0" alt="\prod" title="\prod" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cprod&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="15"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\lim_{\dot{x}}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Clim_%7B%5Cdot%7Bx%7D%7D&bg=ffffff&fg=7c705e&s=0" alt="\lim_{\dot{x}}" title="\lim_{\dot{x}}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Clim_%7B%5Cdot%7Bx%7D%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="16" width="30"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\%</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5C%25&bg=ffffff&fg=7c705e&s=0" alt="\%" title="\%" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5C%25&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="15" width="13"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\div</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cdiv&bg=ffffff&fg=7c705e&s=0" alt="\div" title="\div" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cdiv&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\infty</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=7c705e&s=0" alt="\infty" title="\infty" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cinfty&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="8" width="15"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\cdot</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ccdot&bg=ffffff&fg=7c705e&s=0" alt="\cdot" title="\cdot" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ccdot&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="2" width="3"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\triangle</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctriangle&bg=ffffff&fg=7c705e&s=0" alt="\triangle" title="\triangle" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctriangle&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="14"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\sum</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csum&bg=ffffff&fg=7c705e&s=0" alt="\sum" title="\sum" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csum&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="17"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\angle</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cangle&bg=ffffff&fg=7c705e&s=0" alt="\angle" title="\angle" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cangle&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\int</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cint&bg=ffffff&fg=7c705e&s=0" alt="\int" title="\int" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cint&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="19" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\aleph</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Caleph&bg=ffffff&fg=7c705e&s=0" alt="\aleph" title="\aleph" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Caleph&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\oint</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Coint&bg=ffffff&fg=7c705e&s=0" alt="\oint" title="\oint" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Coint&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="19" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\hbar</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Chbar&bg=ffffff&fg=7c705e&s=0" alt="\hbar" title="\hbar" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Chbar&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\imath</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cimath&bg=ffffff&fg=7c705e&s=0" alt="\imath" title="\imath" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cimath&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="5"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\emptyset</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cemptyset&bg=ffffff&fg=7c705e&s=0" alt="\emptyset" title="\emptyset" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cemptyset&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="15" width="8"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\jmath</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cjmath&bg=ffffff&fg=7c705e&s=0" alt="\jmath" title="\jmath" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cjmath&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="7"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\nabla</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cnabla&bg=ffffff&fg=7c705e&s=0" alt="\nabla" title="\nabla" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cnabla&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="14"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\ell</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cell&bg=ffffff&fg=7c705e&s=0" alt="\ell" title="\ell" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cell&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="7"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\surd</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csurd&bg=ffffff&fg=7c705e&s=0" alt="\surd" title="\surd" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csurd&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="14"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\wp</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cwp&bg=ffffff&fg=7c705e&s=0" alt="\wp" title="\wp" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cwp&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\partial</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpartial&bg=ffffff&fg=7c705e&s=0" alt="\partial" title="\partial" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpartial&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Re</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CRe&bg=ffffff&fg=7c705e&s=0" alt="\Re" title="\Re" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CRe&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\top</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctop&bg=ffffff&fg=7c705e&s=0" alt="\top" title="\top" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctop&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Im</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CIm&bg=ffffff&fg=7c705e&s=0" alt="\Im" title="\Im" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CIm&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\ldots</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cldots&bg=ffffff&fg=7c705e&s=0" alt="\ldots" title="\ldots" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cldots&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="2" width="18"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\prime</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cprime&bg=ffffff&fg=7c705e&s=0" alt="\prime" title="\prime" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cprime&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="5"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\vdots</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvdots&bg=ffffff&fg=7c705e&s=0" alt="\vdots" title="\vdots" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvdots&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="3"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\cdots</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ccdots&bg=ffffff&fg=7c705e&s=0" alt="\cdots" title="\cdots" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ccdots&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="2" width="18"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\varepsilon</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvarepsilon&bg=ffffff&fg=7c705e&s=0" alt="\varepsilon" title="\varepsilon" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvarepsilon&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="8"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\ddots</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cddots&bg=ffffff&fg=7c705e&s=0" alt="\ddots" title="\ddots" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cddots&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="16"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\zeta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Czeta&bg=ffffff&fg=7c705e&s=0" alt="\zeta" title="\zeta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Czeta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="8"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\alpha</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Calpha&bg=ffffff&fg=7c705e&s=0" alt="\alpha" title="\alpha" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Calpha&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\eta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ceta&bg=ffffff&fg=7c705e&s=0" alt="\eta" title="\eta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ceta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\beta</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cbeta&bg=ffffff&fg=7c705e&s=0" alt="\beta" title="\beta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cbeta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\theta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctheta&bg=ffffff&fg=7c705e&s=0" alt="\theta" title="\theta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctheta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="8"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\gamma</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cgamma&bg=ffffff&fg=7c705e&s=0" alt="\gamma" title="\gamma" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cgamma&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\vartheta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvartheta&bg=ffffff&fg=7c705e&s=0" alt="\vartheta" title="\vartheta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvartheta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\delta</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cdelta&bg=ffffff&fg=7c705e&s=0" alt="\delta" title="\delta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cdelta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="8"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\iota</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ciota&bg=ffffff&fg=7c705e&s=0" alt="\iota" title="\iota" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ciota&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="6"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\epsilon</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cepsilon&bg=ffffff&fg=7c705e&s=0" alt="\epsilon" title="\epsilon" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cepsilon&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="7"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\kappa</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ckappa&bg=ffffff&fg=7c705e&s=0" alt="\kappa" title="\kappa" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ckappa&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\lambda</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Clambda&bg=ffffff&fg=7c705e&s=0" alt="\lambda" title="\lambda" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Clambda&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\tau</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctau&bg=ffffff&fg=7c705e&s=0" alt="\tau" title="\tau" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctau&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\mu</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmu&bg=ffffff&fg=7c705e&s=0" alt="\mu" title="\mu" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmu&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\upsilon</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cupsilon&bg=ffffff&fg=7c705e&s=0" alt="\upsilon" title="\upsilon" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cupsilon&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\nu</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cnu&bg=ffffff&fg=7c705e&s=0" alt="\nu" title="\nu" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cnu&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\phi</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=7c705e&s=0" alt="\phi" title="\phi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cphi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\xi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cxi&bg=ffffff&fg=7c705e&s=0" alt="\xi" title="\xi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cxi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="8"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\varphi</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvarphi&bg=ffffff&fg=7c705e&s=0" alt="\varphi" title="\varphi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvarphi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\pi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpi&bg=ffffff&fg=7c705e&s=0" alt="\pi" title="\pi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\chi</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cchi&bg=ffffff&fg=7c705e&s=0" alt="\chi" title="\chi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cchi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\varpi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvarpi&bg=ffffff&fg=7c705e&s=0" alt="\varpi" title="\varpi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvarpi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="14"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\psi</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cpsi&bg=ffffff&fg=7c705e&s=0" alt="\psi" title="\psi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cpsi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="14" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\rho</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Crho&bg=ffffff&fg=7c705e&s=0" alt="\rho" title="\rho" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Crho&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\omega</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Comega&bg=ffffff&fg=7c705e&s=0" alt="\omega" title="\omega" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Comega&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\varrho</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvarrho&bg=ffffff&fg=7c705e&s=0" alt="\varrho" title="\varrho" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvarrho&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="8"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Gamma</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CGamma&bg=ffffff&fg=7c705e&s=0" alt="\Gamma" title="\Gamma" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CGamma&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="10"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\sigma</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csigma&bg=ffffff&fg=7c705e&s=0" alt="\sigma" title="\sigma" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csigma&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="7" width="10"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Delta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CDelta&bg=ffffff&fg=7c705e&s=0" alt="\Delta" title="\Delta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CDelta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="13"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\varsigma</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvarsigma&bg=ffffff&fg=7c705e&s=0" alt="\varsigma" title="\varsigma" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvarsigma&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="7"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Theta</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CTheta&bg=ffffff&fg=7c705e&s=0" alt="\Theta" title="\Theta" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CTheta&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="12"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Lambda</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CLambda&bg=ffffff&fg=7c705e&s=0" alt="\Lambda" title="\Lambda" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CLambda&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Omega</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5COmega&bg=ffffff&fg=7c705e&s=0" alt="\Omega" title="\Omega" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5COmega&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Xi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CXi&bg=ffffff&fg=7c705e&s=0" alt="\Xi" title="\Xi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CXi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\gets</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cgets&bg=ffffff&fg=7c705e&s=0" alt="\gets" title="\gets" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cgets&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Pi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CPi&bg=ffffff&fg=7c705e&s=0" alt="\Pi" title="\Pi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CPi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\to</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cto&bg=ffffff&fg=7c705e&s=0" alt="\to" title="\to" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cto&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Sigma</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CSigma&bg=ffffff&fg=7c705e&s=0" alt="\Sigma" title="\Sigma" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CSigma&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\leftarrow</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cleftarrow&bg=ffffff&fg=7c705e&s=0" alt="\leftarrow" title="\leftarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cleftarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Upsilon</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CUpsilon&bg=ffffff&fg=7c705e&s=0" alt="\Upsilon" title="\Upsilon" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CUpsilon&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Leftarrow</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CLeftarrow&bg=ffffff&fg=7c705e&s=0" alt="\Leftarrow" title="\Leftarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CLeftarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Phi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CPhi&bg=ffffff&fg=7c705e&s=0" alt="\Phi" title="\Phi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CPhi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="11"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\rightarrow</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Crightarrow&bg=ffffff&fg=7c705e&s=0" alt="\rightarrow" title="\rightarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Crightarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Psi</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CPsi&bg=ffffff&fg=7c705e&s=0" alt="\Psi" title="\Psi" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CPsi&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="12"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Rightarrow</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CRightarrow&bg=ffffff&fg=7c705e&s=0" alt="\Rightarrow" title="\Rightarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CRightarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="16"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\leftrightarrow</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cleftrightarrow&bg=ffffff&fg=7c705e&s=0" alt="\leftrightarrow" title="\leftrightarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cleftrightarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\grave{x}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cgrave%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\grave{x}" title="\grave{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cgrave%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\Leftrightarrow</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5CLeftrightarrow&bg=ffffff&fg=7c705e&s=0" alt="\Leftrightarrow" title="\Leftrightarrow" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5CLeftrightarrow&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="17"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\tilde{x}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ctilde%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\tilde{x}" title="\tilde{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ctilde%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\mapsto</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmapsto&bg=ffffff&fg=7c705e&s=0" alt="\mapsto" title="\mapsto" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmapsto&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="9" width="16"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\mathring{x}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cmathring%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\mathring{x}" title="\mathring{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cmathring%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\hat{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Chat%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\hat{x}" title="\hat{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Chat%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="13" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\bar{x}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cbar%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\bar{x}" title="\bar{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cbar%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="9"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\check{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Ccheck%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\check{x}" title="\check{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Ccheck%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\vec{x}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cvec%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\vec{x}" title="\vec{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cvec%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="11"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\dot{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cdot%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\dot{x}" title="\dot{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cdot%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\widehat{x+y}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cwidehat%7Bx%2By%7D&bg=ffffff&fg=7c705e&s=0" alt="\widehat{x+y}" title="\widehat{x+y}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cwidehat%7Bx%2By%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="19" width="37"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\breve{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cbreve%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\breve{x}" title="\breve{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cbreve%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\widetilde{x+y}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cwidetilde%7Bx%2By%7D&bg=ffffff&fg=7c705e&s=0" alt="\widetilde{x+y}" title="\widetilde{x+y}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cwidetilde%7Bx%2By%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="37"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\acute{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cacute%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\acute{x}" title="\acute{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cacute%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\{
x \}</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5C%7B++x+%5C%7D&bg=ffffff&fg=7c705e&s=0" alt="\{  x \}" title="\{  x \}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5C%7B++x+%5C%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="24"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\ddot{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Cddot%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\ddot{x}" title="\ddot{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cddot%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="12" width="9"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\|
x \|</td>
      <td style="vertical-align: top; width: 98px; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5C%7C++x+%5C%7C&bg=ffffff&fg=7c705e&s=0" alt="\|  x \|" title="\|  x \|" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5C%7C++x+%5C%7C&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="21"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\langle{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Clangle%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\langle{x}" title="\langle{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Clangle%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="14"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\frac{x}{y}</td>
      <td style="vertical-align: top; width: 98px; text-align: center; background-color: white;"><img src="https://s0.wp.com/latex.php?latex=%5Cfrac%7Bx%7D%7By%7D&bg=ffffff&fg=7c705e&s=0" alt="\frac{x}{y}" title="\frac{x}{y}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cfrac%7Bx%7D%7By%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="19" width="7"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\rangle</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Crangle&bg=ffffff&fg=7c705e&s=0" alt="\rangle" title="\rangle" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Crangle&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="18" width="5"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">x^y</td>
      <td style="vertical-align: top; width: 98px; text-align: center; background-color: white;"><img src="https://s0.wp.com/latex.php?latex=x%5Ey&bg=ffffff&fg=7c705e&s=0" alt="x^y" title="x^y" class="latex" srcset="https://s0.wp.com/latex.php?latex=x%5Ey&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="11" width="15"></td>
    </tr>
    <tr>
      <td style="vertical-align: top; width: 182px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\sqrt{x}</td>
      <td style="width: 98px; color: black; background-color: white; text-align: center;"><img src="https://s0.wp.com/latex.php?latex=%5Csqrt%7Bx%7D&bg=ffffff&fg=7c705e&s=0" alt="\sqrt{x}" title="\sqrt{x}" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Csqrt%7Bx%7D&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="17" width="23"></td>
      <td style="vertical-align: top; width: 167px; text-align: center; background-color: rgb(147, 255, 39); color: red;">\epsilon_0</td>
      <td style="vertical-align: top; width: 98px; text-align: center; background-color: white;"><img src="https://s0.wp.com/latex.php?latex=%5Cepsilon_0&bg=ffffff&fg=7c705e&s=0" alt="\epsilon_0" title="\epsilon_0" class="latex" srcset="https://s0.wp.com/latex.php?latex=%5Cepsilon_0&bg=ffffff&fg=7c705e&s=0&zoom=2 1.5x" scale="1.5" height="10" width="13"></td>
    </tr>
   </tbody>
</table>

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
--- type:NormalExercise lang:r xp:100 skills:1 key:955002b2b7
## Média aritmética

É o valor que mais se aproxima do valor real. Para obtê-la basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas. Por exemplo, numa experiência foram obtidas as seguintes medidas: 4m, 5m, 8m, 9m, 5m. Em R a média aritmética $\bar{x}$ pode ser calculada da seguinte maneira:

<p style="background-color: rgb(102, 255, 255);">É o valor que mais se aproxima do valor real. Para obtê-la basta dividir a soma dos valores das medidas efetuadas pelo número destas medidas. Por exemplo, numa experiência foram obtidas as seguintes medidas: 4m, 5m, 8m, 9m, 5m. Em R a média aritmética $\bar{x}$ pode ser calculada da seguinte maneira:</p>

<div style="font-size: large; font-family: sans-serif">
  <p style="color: #000000; background-color: #ffffff">Text color: black, background-color: white</p>
  <p style="color: #ffffff; background-color: #000000">Text color: white, background-color: black</p>
  <p style="color: #ff0000; background-color: #ffffff">Text color: red, background-color: white</p>
  <p style="color: blue; background-color: #ffffff">Text color: blue, background-color: white</p>
  <p style="color: green; background-color: #ffff42">Text color: green, background-color: yellow</p>
  <p style="color: #ffffff; background-color: #ff0000">Text color: white, background-color: red</p>
</div>

```{r}
x <- c(4, 5, 8, 9, 5)
mean(x)
```
Depois basta teclar enter para obter o resultado.

> #### Efetuando várias medidas -  cálculo de $\bar{x}$

> Calcule a média aritmética das seguintes medidas: 10, 20, 30, 50, 100, 123, 233.

*** =instructions
- Use o mesmo procedimento feito no código acima acima.
- O vetor é c(10, 20, 30, 50, 100, 123, 233). Armazene-o numa variável.

*** =hint
Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x e use o comando mean(x)

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Calcule a média aritmética pedida
x <- mean(x)
```
*** =*** =solution
```{r}
x <- c(10, 20, 30, 50, 100, 123, 233)
mean(x)
```
*** =sct
```{r}
test_output_contains("80.85714", incorrect_msg = "Voce tem certeza que armazenou o vetor c na variavel x?")
success_msg("Parabéns! Agora você sabe calcular a média aritmética usando o R!")
```

--- type:NormalExercise lang:r xp:100 skills:1 key:dd48eb091a
## Erro absoluto (E)

Podemos encontrar o erro aboluto de uma medida usando a seguinte expressão: 

> $$E = {\left |m-\bar{m}  \right |}$$

> onde,

> $E$ - erro absoluto.

> $m$ - valor correto.

> $\bar{m}$ - valor obtido nas medidas.

No R, a fórmula de erro absoluto é escrita assim:

```{r}
E <- abs(m - mean(x))
E
```
Depois basta teclar enter para obter o resultado.

> #### Medindo alturas - cálculo do E

> Suponha que você tenha a tarefa de medir várias vezes a altura de uma porta e obteve as seguintes medidas: 2.17, 2.20, 2.15 e 2.12. Se o valor correto da medida da altura da porta corresponde a 2.10m, calcule o erro absoluto (E).

*** =instructions
- Calcule a média aritmética das medidas ==> mean(x). 
- Subtraia a média encontrada da medida correta ==> m - mean(x). 
- Obtenha o módulo (valor absoluto) dessa diferença ==> abs(m - mean(x)).
*** =hint

Armazene 2.10 na variável m.
Crie um vetor c com as medidas dadas. Armazene o vetor c em uma variável x e o valor 
da medida correta numa variável m e use o comando mean(x).

*** =pre_exercise_code
```{r}
# no pec
```
*** =sample_code
```{r}
# Armazene o valor da medida correta. 
m <- 
# Crie um vetor c com as medidas dadas e o armazene em uma variável x.
x <- 
# Use o comando mean(x) para calcular a média.
mean ()
# Obtenha o módulo (valor absoluto) dessa diferença e armazene a média numa variável.
E <- abs(m - mean(x))
# Mostre o valor de E na tela.
E
```
*** =solution
```{r}
m <- 2.10
x <- c(2.17, 2.20, 2.15, 2.12)
mean(x)
E <- abs(m - mean(x))
E 
```
*** =sct
```{r}
test_output_contains("0.06", incorrect_msg = "Você armazenor corretamente o vetor x <- c(2.17, 2.20, 2.15, 2.12) na variável x?")
success_msg("Parabéns! Agora você sabe calcular o erro absoluto usando o R!")
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
E <- abs(9.8 - 10.2)
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
