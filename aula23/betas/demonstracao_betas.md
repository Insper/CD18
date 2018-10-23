## Obtenção dos estimadores

 Obtenha os estimadores de $\beta_0$ e $\beta_1$
a partir do Método dos Mínimos Quadrados, cujo objetivo
é encontrar a reta que passa mais próxima ao mesmo tempo de todos os pontos. Neste caso,
encontre os estimadores
$\hat{\beta_0}$
e
$\hat{\beta_1}$
que minimizam a soma dos erros ao quadrado.

Temos que o $\hat{y}_i$ estimado é dado pela relação:  $\hat{y}_i = \hat{\beta_0} + \hat{\beta_1} x_i$ 



E o erro é: $e_i = y_i - \hat{y}_i$



$$y_i = \hat{\beta_0} + \hat{\beta_1} x_i + e_i \,\!$$



$$S(\hat{\beta_0},\hat{\beta_1}) = \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) ^2$$

Aplicando a regra da cadeia para a derivada parcial sobre os eixos:

$$
\frac{\partial S}{\partial \hat{\beta_0}} = \frac{\partial S}{\partial \big[ \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right)  \big]} \cdot \frac{\partial \big[  \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) \big] }{\partial \hat{\beta_0}}$$


Temos que:

$$\frac{\partial S}{\partial \big[ \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right)  \big]}  =  2\sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) $$

e

$$\frac{\partial \big[ \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right)  \big] }{ \partial \hat{\beta_0}}  = -1 $$

Impondo a condição de valor mínimo do parabolóide para $\hat{\beta_0}$ :

$$\frac{\partial S }{ \partial \hat{\beta_0}}  =  2\sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) ( -1 ) = 0 $$

$$ \frac{\partial S }{ \partial \hat{\beta_0}}  = -2 \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) = 0 $$ 


E para $\hat{\beta_1}$ :


$$
\frac{\partial S}{\partial \hat{\beta_1}} = \frac{\partial S}{\partial \big[ \sum_{i=1}^n \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right)  \big]} \cdot \frac{\partial \big[  \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) \big] }{\partial \hat{\beta_1}}$$





$$\frac{\partial S }{ \partial \hat{\beta_1}}  = -2 \sum_{i=1}^n x_i \left( y_i - \hat{\beta_0} - \hat{\beta_1} x_i \right) = 0
$$

Dividindo por $2n \,\!$ e distribuindo


 $$\frac{-2 \sum_{i=1}^n y_i}{2n} + \frac{2 \sum_{i=1}^n \hat{\beta_0}} {2n} + \frac{2 \sum_{i=1}^n \hat{\beta_1} x_i }{2n} = \frac{0}{2n} $$

 $$\frac{-\sum_{i=1}^n y_i}{n} + \frac{\sum_{i=1}^n \hat{\beta_0}}{n} + \frac{\hat{\beta_1}   \sum_{i=1}^nx_i}{n} = 0 $$

$$-\bar{y} + \hat{\beta_0} + \hat{\beta_1} \bar{x} = 0 $$


Chegamos à expressão para $\hat{\beta_0}$ :

 $$\hat{\beta_0} = \bar{y} - \hat{\beta_1} \bar{x} $$

Na expressão acima  $\bar{y}$ é a Média Amostral de $y \,\!$ e $\bar{x}$ é a Média Amostral de $x \,\!$

Podemos substituir $\hat{\beta_0}$ na relação original:

 $$-2 \sum_{i=1}^n x_i \left(y_i - \bar{y} + \hat{\beta_1} \bar{x} - \hat{\beta_1} x_i \right) = 0 $$

 $$\sum_{i=1}^n \left[ x_i \left( y_i - \bar{y} \right) + x_i \hat{\beta_1} \left( \bar{x} - x_i \right) \right] = 0 $$

 $$\sum_{i=1}^n x_i \left( y_i - \bar{y} \right) + \hat{\beta_1}    \sum_{i=1}^n x_i \left( \bar{x} - x_i \right) = 0 $$

Que nos dá, isolando $\beta1$ :


$$ \hat{\beta_1} = \frac{ \sum_{i=1}^n x_i \left( y_i - \bar{y} \right)  }  {   \sum_{i=1}^n x_i \left( \bar{x} - x_i \right)  } 
$$


Reescrevendo levando em conta as relações $$ \sum_{i=1}^n ( x_i - \overline{x} )^2 = \sum_{i=0}^n ( x_i^2 - x_i \overline{x} )   $$ e $$ \sum_{i=1}^n ( x_i - \overline{x} )( y_i - \overline{y} ) = \sum_{i=0}^n ( x_i y_i - y_i \overline{x} )    $$  desenvolvidas mais abaixo, temos:
  

 $$\hat{\beta_1} = \frac{\sum_{i=1}^n \left( x_i - \bar{x} \right) \left( y_i - \bar{y} \right)}{ 
 {\sum_{i=1}^n \left( x_i - \bar{x} \right)^2}}$$


###  Relações auxiliares

Temos que $$\frac{1}{n} \sum_{i=1}^{n}x_i = \overline{x}$$


portanto 

$$\sum_{i=1}^{n}x_i = n \overline{x}$$

e temos que 

$$\frac{1}{n} \sum_{i=1}^{n}y_i = \overline{y}$$



portanto $$\sum_{i=1}^{n}y_i = n \overline{y}$$


### Relação 1

A igualdade abaixo é importante para entendermos a fórmula dos $\beta$ :

$$
\sum_{i=1}^n ( x_i - \overline{x} )( y_i - \overline{y} ) = \sum_{i=0}^n ( x_i y_i - y_i \overline{x} ) 
$$


Vamos estudar como reescrever a relação:

$$\sum_{i=1}^n ( x_i - \overline{x} )( y_i - \overline{y} )$$


Aplicando a propriedade distributiva:

$$\sum_{i=1}^n ( x_i y_i - x_i \overline{y}  - \overline{x} y_i + \overline{x} \overline{y} ) = $$


$$\sum_{i=1}^n  x_i y_i -  \overline{y} \sum_{i=1}^n  x_i   - \overline{x} \sum_{i=1}^n y_i + \overline{x} \overline{y} \sum_{i=1}^n 1  = $$

$$\sum_{i=1}^n  x_i y_i -  \overline{y} n \overline{x}  - \overline{x} n \overline{y} + \overline{x} \overline{y} n  = $$

$$\sum_{i=1}^n  x_i y_i -  n \overline{x} \overline{y}  $$

A relação acima pode ser escrita como:

$$\sum_{i=1}^n  x_i y_i -  n \overline{x} \overline{y}  = \sum_{i=1}^n  x_i y_i - \overline{x}  \sum_{i=0}^n y_i  = $$

$$
\sum_{i=0}^n ( x_i y_i - y_i \overline{x} ) 
$$





### Relação 2

Outra relação importante é a seguinte :

$$
\sum_{i=1}^n ( x_i - \overline{x} )^2 = \sum_{i=0}^n ( x_i^2 - x_i \overline{x} ) 
$$


Vamos estudar como reescrever a relação:

$$\sum_{i=1}^n ( x_i - \overline{x} )^2$$


Expandindo o quadrado: 

$$\sum_{i=1}^n ( x_i^2 - 2 x_i \overline{x} + \overline{x}^2) = $$





$$\sum_{i=1}^n  x_i^2  - 2 n \overline{x}^2 + \sum_{i=1}^n  x_i^2 \overline{x}^2 = $$

$$\sum_{i=1}^n  x_i^2  - 2 n \overline{x}^2 + n x_i^2 \overline{x}^2 = $$

$$\sum_{i=1}^n  x_i^2  - n \overline{x}^2  = $$

$$\sum_{i=1}^n  x_i^2  -  \sum_{i=1}^n x_i \overline{x}  = \sum_{i=1}^n \left( x_i^2  -  x_i \overline{x} \right) $$
