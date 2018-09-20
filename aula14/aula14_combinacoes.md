# Aula 14 - Combinação de Variáveis Aleatórias

## Combinações de variáveis aleatórias


Lembremos que:

Se $f(x)$ for uma função de densidade de probabilidade contínua

$\mu = E(X) = \int_{-\infty}^{\infty}x f(x) dx$

E que a variância:

$V(X) = \int_{-\infty}^{\infty}(x - \mu)^2f(x) dx$

E que ainda vale a propriedade:

$V(X) = E(X^2) - E(X)^2 = E(X^2) - \mu^2$

## Propriedades da esperança

Lembremos da aula 08 que, para o valor esperado ou esperança, vale, se $c$ e $d$ forem constantes:

$E(X+d) = E(X) + d$

$E(cX) = cE(X)$

Combinando as expressões acima:

$E(cX + d) = cE(X) + d$

E para a variância vale:

$V(X+d) = V(X)$

$V(cX) = c^2V(X)$

$V(cX + d) = c^2V(X)$

## Propriedades de combinações de variáveis aleatórias

### Propriedades da esperança

Sejam $a$ e $b$ constantes e $X$  e $Y$ variáveis aleatórias

$E(X + Y) = E(X) + E(Y)$

$E(aX + bY) = aE(X) + bE(Y)$

Estes resultados são sempre válidos, sejam $X$  e $Y$ dependentes ou independentes 

### Propriedades da variância

Sejam $X$  e $Y$ variáveis aleatórias

$V(X+Y) = V(X) + V(Y) + 2Cov(X,Y)$

$V(X-Y) = V(X) + V(Y) -2Cov(X,Y)$

Sendo que, como visto nas aulas de análise bidimensional, a covariância é definida como:


$Cov(X,Y) = E[(X-\mu_X))(Y-\mu_Y)] = E(XY) - \mu_X\mu_Y$

Dado que $\mu_X = E(X)$ e $\mu_Y = E(Y)$

### Variáveis independentes

$X$ e $Y$  independentes $\implies Cov(X,Y)=0$

Entretanto:

$Cov(X,Y) =0$ $\nRightarrow$ $X$ e $Y$  independentes

Se as variáveis $X$ e $Y$ forem independentes:

$V(X+Y) = V(X) + V(Y)$

$V(X-Y) = V(X) + V(Y)$


$E(X)E(Y) = \mu_X\mu_Y$


$Cov(X,Y) = E(XY) - \mu_X\mu_Y$


### Variância com coeficientes:

Sejam $a$ e $b$ constantes e $X$ e $Y$ variáveis aleatórias:

$V(aX + bY) = a^2 V(X) + b^2 V(X) + 2ab Cov(X,Y)$

$V(aX - bY) = a^2 V(X) + b^2 V(X) - 2ab Cov(X,Y)$

Se as variáveis $X$ e $Y$ forem independentes:

$V(aX+bY) = a^2V(X) + b^2V(Y)$

$V(aX-bY) = a^2V(X) + b^2V(Y)$


### Exemplo - soma de v.a

Um semicondutor tem 3 camadas. Supondo que as variâncias de espessura da primeira, segunda e terceira camada sejam 25, 40 e 30 $nm^2$, respectivamente, e que as espessuras sejam independentes, qual é o desvio padrão da espessura do produto final?

Sejam $X_1$, $X_2$ e $X_3$ as variáveis aleatórias que denotam as espessuras.

Então: 

$X = X_1 + X_2 + X_3$

Temos então que:

$V(X)=V(X_1)+V(X_2)+V(X_3) = 95 nm^2$

Consequentemente, o desvio padrão do produto final é: $9.747 nm$


### Exemplo

Um gerente quer melhorar o desempenho de sua fábrica. Para isso, ele quer comparar:

Uma máquina que leva um tempo médio para concluir um processo de E(X) e tem variância V(X) versus
duas máquinas independentes que têm tempo médio e variância iguais à metade de E(X) e V(X). 

É vantagem para ele realizar esta troca?


### Média e variância de uma média

Seja $\overline{X} = (X_1 + X_2 + \cdots + X_n)/n$, com $E(X_i) = \mu$ para todo $i=1,2,\cdots, n$

Temos que $E(\overline{X}) = \mu$

Se $X_1, X_2, \cdots, X_n$ forem indepententes com  $V(X_i) = \sigma^2$ para todo $i=1,2,\cdots, n$, temos:

$V(\overline{X}) = \frac{\sigma^2}{n}$


## Propriedade reprodutiva da normal


Sejam $X_1, X_2, \cdots, X_n$   variáveis aleatórias normais com $E(X_i) = \mu_i$ e $V(X_i) = \sigma_i^2$, para $i=1,2,\cdots, n$

Então:

$Y = c_1X_1 + c_2X_2 + \cdots + c_nX_n$ **será uma variável aleatória normal**, com $E(Y)$ e $V(Y)$ definidos conforme

$$E(Y) = c_1\mu_1 + c_2\mu_2 + \cdots + c_n\mu_n$$

$$V(Y) = c_1^2\sigma_1^2 + c_2^2\sigma_2^2 + \cdots + c_n^2\sigma_n^2$$


