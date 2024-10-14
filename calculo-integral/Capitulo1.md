# Notación Sigma

El **operador sumatoria** nos permite escribir la suma de varios numeros $a_m ,..., a_n (m \leq n)$ en la forma compacta

$$
\sum^n_{i=m}a_i = a_m + a_{m+1} + ... + a_{n-1} + a_n
$$

Por definición:

* Indica terminar en i = n

* La letra $\sum$ significa suma

* Indica iniciar en i = m

> **Propiedades**
> 
> Siendo *c* una constante
> 
> * $\sum_{i=1}^n c = n*c$
> * $\sum_{i=1}^n c*a_i = c\sum_{i=1}^n a_i$
> * $\sum_{i=1}^n (a_i \pm b_i) = \sum_{i=1}^n a_i \pm \sum_{i=1}^n b_i$

# Antiderivadas

En sesiones anteriores, vimos cómo evaluar integrales definidas usando sumas de Riemann. Ahora, la idea es obtener un método más eficiente y menos tedioso para calcular $\int_a^b f(x)dx$. Para tal fin introducimos el concepto de antiderivada.

> **Definición**
> 
> Una función F se dice que es una *antiderivada* (o una primitiva) de una función $f$ sobre un intervalo $I$ si $F'(x) = f(x)$ para todo $x \in I$

**Ejemplo.** $F(x) = \frac{x^4}{4}$ Es una antiderivada de $f(x) = x^{3} en I = (-\inf, \inf)$. En efecto,

$$
F'(x) = \frac{1}{4}*4x^3 = f(x)
$$

para todo $x \in I$

Notemos que $G(x) = \frac{x^4}{4} + 2024$ es otra antiderivada de $f(x) = x^{3}$ en $I$. En general, cualquier función de la forma

$$
H(x) = \frac{x^4}{4} + C \ , C \in \mathbb{R}
$$

es una antiderivada de $f(x) = x^3$ en $I$.

> **Teorema**
> 
> Si F es una antiderivada de $f$ sobre $I$, entonces la antiderivada más general de $f$ sobre $I$ es
> 
> $F(x) + C$
> 
> Donde $C \in \mathbb{R}$ es una constante arbitraria

Necesitamos una notación adecuada para las antiderivadas que nos facilite el trabajo con ellas.

# Integral Indefinida

$$
\int{f(x)}dx = F(x) + C => F'(x) = f(x)
$$

Observemos que una integral definida es un n«umero y que una integral indefinida es una familia de funciones.

> **Propiedades de la integral indefinida**
> 
> Donde $k \in \mathbb{R}$
> 
> * $\int{k*f(x)}dx = k*\int{f(x)}dx$
> 
> * $\int{f(x) \pm g(x)}dx = \int{f(x)}dx \pm \int{g(x)}dx$

## Lista de integrales fundamentales

* $\int{x^n}dx = \frac{x^{n+1}}{n+1} + C$
* $\int{k}dx = k*x + C$
* $\int{\frac{1}{x}}dx = ln|x| + C$
* $\int{e^{x}}dx = e^{x} + C$
* $\int{k^{x}}dx = \frac{k^{x}}{ln(k)} + C$
* $\int{cos(x)}dx = sin(x) + C$
* $\int{sin(x)}dx = -cos(x) + C$
* $\int{sec²(x)}dx = tan(x) + C$
* $\int{csc²(x)}dx = -cot(x) + C$
* $\int{sec(x)tan(x)}dx = sec(x) + C$
* $\int{csc(x)cot(x)}dx = -csc(x) + C$
* $\int{\frac{1}{\sqrt{1-x²}}}dx = sin^{-1}(x) + C$
* $\int{\frac{-1}{\sqrt{1-x²}}}dx = cos^{-1}(x) + C$
* $\int{\frac{1}{1-x²}}dx = tan^{-1}(x) + C$

# Teorema Fundamental del Calculo - Cómo evaluar integrales definidas

El Teorema Fundamental del Cálculo recibe de manera apropiada este nombre porque establece una conexión entre las 2 ramas del cálculo: el cálculo
diferencial y el cálculo integral. Usando la relación inversa entre la integral y la derivada que afirma el teorema, Newton y Leibniz desarrollaron un
método sistemático que nos permite calcular con gran facilidad áreas, distancias e integrales definidas, sin tener que evaluarlas como límites de sumas.

> **Teorema de evaluación**
> 
> Sean $f$ una función continua en [a,b] y $F(x)$ una antiderivada de $f(x)$ en [a,b]. Entonces:
> 
> $\int_{a}^{b}{f(x)}dx = F(x)|_{a}^{b} = F(b) - F(a)$

# La derivación y la integración como procesos inversos

$$
\int_{a}^{x}{f(t)}dt = F(x) - F(a)
$$

$$
\frac{d}{dx}(F(x) - F(a)) = f(x)
$$

$$
\frac{d}{dx}\int_{a}^{x}{f(t)}dt = f(x)
$$

# Aplicaciones del teorema de evaluación

> **Teorema del cambio neto**
> 
> La integral de una razón de cambio es el cambio neto (o total)
> 
> $\int_{a}^{b}{Q'(x)}dx = Q(b) - Q(a)$

* Si $V(t)$ es el volumen de agua en un tanque $V'(t)$
  es la razón a la cual fluye (entra o sale) el agua en el instante $t$. Por tanto la variación del volumen entre el tiempo $t_1$ y $t_2$ es:

$$
\int_{t_1}^{t_2}{V'(t)}dt = V(t_2) - V(t_1)
$$

* Si $m(x)$ es la masa de una varilla, medida del extremo izquierdo hasta un punto $x$, la *densidad lineal* es $\rho(x) = m'(x)$. Por lo que la masa de la varilla desde un extremo $a$ a $b$ es:

$$
\int_{a}^{b}{\rho(x)}dx = m(b) - m(a)
$$

* Si $C(x)$ es el costo de producir $x$ unidades de un artículo, el *costo marginal* es la derivada $C'(x)$. De esa manera el incremento cuando la producción aumenta de $x_1$ a $x_2$ unidades es:

$$
\int_{x_1}^{x_2}{C'(x)}dx = C(x_2) - C(x_1)
$$

* Si un objeto se mueve a lo largo de una línea recta con función posición $s(t)$, su velocidad es $v(t) = s'(t)$. De modo que el *desplazamiento* de la particula desde $t_1$ hasta $t_2$ es:

$$
\int_{t_1}^{t_2}{v(t)}dt = s(t_2) - s(t_1)
$$

* Pero, si queremos calcular la *distancia recorrida durante el intervalo*, tenemos que integrar la rapidez.

$$
\int_{t_1}^{t_2}{|v(t)|}dt = DistanciaTotal
$$

# Técnica de integración por partes

Cada regla de derivación tiene una correspondiente regla de integración. Por ejemplo, la regla de sustitución de la clase anterior corresponde a la regla de la cadena. A la regla del producto le corresponde la denominada **Regla de integración por partes**.

> **Regla de integración por partes**
> $$\int{f(x)*g'(x)}dx = f(x)*g(x) - \int{f'(x)*g(x)}dx$$

En la práctica, la regla es más fácil de recordar y de aplicar si se escribe usando *diferenciales*:

* $u = f(x) \wedge du = f'(x)dx$
* $dv = g'(x)dx \wedge v = g(x)$

Sustituyendo, se obtiene

> **Fórmula de integración por partes**
> $$\int{u}dv = u*v - \int{v}du$$

Cuando se presentan varias opciones en la elección de $u$ y $dv$, hay que aplicar 2 criterios:

1. $v$ debe ser fácil de calcular a partir de $dv$
2. La integral $\int{v}du$ debe ser, en cierto sentido, más fácil que la integral original $\int{u}dv$

<hr />

El siguiente *ejemplo* ilustra esta idea.

$$
\int{x*\cos{x}}dx
$$

* $u = x \wedge dv = \cos(x)dx$

* $du = dx \wedge v = \sin(x)$

$$
\int{x*\cos{x}}dx = x*\sin{x} - \int{\sin{x}}dx = x*\sin{x} + \cos{x} + C
$$

Si hubiéramos elegido $u = \cos{x} \wedge dv = x*dx$, entonces habríamos enfrentado una integral más difícil que la original:

$$
\int{x*\cos{x}}dx = \frac{x^2}{2}*\cos{x} + \frac{1}{2}*\int{x^2*\sin{x}}dx
$$

Al integrar por partes, se recomienda usar la regla de **LIATE**: una estrategia heurística que propone un orden de prioridad

* **L**ogarítmica
* **I**nversa trigonometrica
* **A**lgebraica
* **T**rigonométrica
* **E**xponencial

en la elección de $u$ y $dv$. Por ejemplo, al integrar $\int{x^2\arctan{x}}dx$, se elige $u = \arctan{x} \wedge dx = x^2dx$.

<hr />

> **Evaluando integrales definidas por partes**
>
> $$\int_{a}^{b}{f(x)*g'(x)}dx = f(x)*g(x)|_{a}^{b} - \int_{a}^{b}{g(x)*f'(x)}dx$$

# Integrales trigonométricas

> **Estrategia para evaluar** $\int{\sin^{m}{x}*\cos^{n}{x}}dx$
>
> 1. Si la potencia de $\cos{x}$ es **impar**, escriba $n = 2*k + 1$, separe un factor $\cos{x}$ y use $\cos^{2}{x} = 1 - \sin^{2}{x}$:
>
> $$\int{\sin^{m}{x}*\cos^{2*k + 1}{x}}dx = \int{\sin^{m}{x}*(\cos^{2}{x})^{k}*\cos{x}}dx = \int{\sin^{m}{x}*(1 - \sin^{2}{x})^{k}*\cos{x}}dx$$
>
> $$u = \sin{x} \wedge du = \cos{x}$$
>
> 2. Si la potencia de $\sin{x}$ es **impar**, escriba $m = 2*k + 1$, separe un factor $\sin{x}$ y use $\sin^{2}{x} = 1 - \cos^{2}{x}$:
>
> $$\int{\sin^{2*k + 1}{x}*\cos^{n}{x}}dx = \int{(\sin^{2}{x})^{k}*\cos^{n}{x}*\sin{x}}dx = \int{(1 - \cos^{2}{x})^{k}*\cos^{n}{x}*\sin{x}}dx$$
>
> $$u = \cos{x} \wedge du = -\sin{x}$$
>
> 3. Si las potencias de ambos, $\sin{x}$ y $\cos{x}$, son **pares**, utilice las identidades del ángulo medio:
>
> $$ \cos^{2}{x} = \frac{1 + \cos{2x}}{2} \\ \sin^{2}{x} = \frac{1 - \cos{2x}}{2}$$
>
> También puede ser útil la identidad de ángulo doble: $\sin{x}*\cos{x} = \frac{1}{2}*\sin{2x}$

> **Estrategia para evaluar** $\int{\tan^{m}{x}*\sec^{n}{x}}dx$
>
> 1. Si la potencia de $\sec{x}$ es **par**, escriba $n = 2*k$, separe un factor de $\sec^{2}{x}$ y use $\sec^{2}{x} = 1 + \tan^{2}{x}$:
>
> $$\int{\tan^{m}{x}*(\sec^{2}{x})^{k-1}*\sec^{2}{x}}dx = \int{\tan^{m}{x}*(1 + \tan^{2}{x})^{k-1}*\sec^{2}{x}}dx$$
>
> $$u = \tan{x} \\ du = \sec^{2}{x}dx$$
>
> 2. Si la potencia de $\tan{x}$ es **impar**, escriba $m = 2*k + 1$, separe un factor de $\sec{x}*\tan{x}$ y use $\tan^{2}{x} = \sec^{2}{x} -1$:
>
> $$\int{(\tan^{2}{x})^{k}*\tan{x}*\sec^{n-1}{x}*\sec{x}}dx = \int{(\sec^{2}{x} -1)^{k}*\sec^{n-1}{x}*\sec{x}*\tan{x}}dx$$
>
> $$u = \sec{x} \\ du = \sec{x}*\tan{x}dx$$
>
> 3. Para los otros casos, no hay guías claras: puede requerir identidades, integración por partes y un poco de ingenio.

# Integración de funciones racionales mediante fracciones parciales

Motivación. Si sumamos las fracciones $\frac{4}{x-1}$ y $\frac{-2}{x+2}$, se obtiene:

$$
\frac{4}{x-1} + \frac{-2}{x+2} = \frac{4*(x+2) - 2*(x-1)}{(x-1)*(x+2)} = \frac{2x + 10}{x^{2} + x -2}
$$

Luego,

$$
\int{\frac{2x+10}{x^2+x-2}}dx = \int{(\frac{4}{x-1} - \frac{2}{x+2})}dx = 4*\int{\frac{dx}{x-1}} - 2*\int{\frac{dx}{x+2}} = 4*ln|x-1| - 2*ln|x+2| + C
$$

La suma $\frac{4}{x-1} - \frac{2}{x+2}$ se denomina *descomposición en fracciones parciales* de la función racional $f(x) = \frac{2x+10}{x^2+x-2}$

> **Nota**
>
> Este método se puede aplicar si $f(x) = \frac{P(x)}{Q(x)}$ es una *fracción propia* (el grado del numerador $P$ es *menor* que el grado del denominador $Q$). Si la fracción es impropia, se debe realizar el paso preliminar de dividir $P$ por $Q$.

> **Método de fracciones parciales para evaluar** $\int{\frac{P(x)}{Q(x)}}dx$
>
> 1. Factorice $Q(x)$ tanto como sea posible en factoriales lineales y/o factores cuadráticos irreducibles.
>
> 2. Descomponga la fracción propia como una suma de *fracciones parciales* de la forma $\frac{A}{(ax+b)^{i}}$ o $\frac{Ax+B}{(ax^2+bx+c)^{j}}$.
>
> 3. Halle las constantes $A, B,...$ usando el hecho de que 2 polinomios son iguales si y sólo si sus coeficientes son iguales.
>
> 4. Integre de acuerdo a cada caso.

**Caso 1: El denominador $Q(X)$ es producto de factores lineales distintos**.

*Ejemplo*. Evalúe $\int{\frac{3x^2+7x-2}{x^3-x}}dx$.

Factorizamos $Q(x) = x^3 -x = x*(x^2 -1) = x*(x-1)*(x+1)$. Por tanto,

$$
\frac{3x^2 +7x -2}{x^3 -x} = \frac{A}{x} + \frac{B}{x-1} + \frac{C}{x+1} \Rightarrow 3x^2 + 7x -2 = A*(x^2-1) + Bx*(x+1) + Cx*(x-1)
$$

Encontramos las constantes, sustituyendo las raíces de $Q(X)$ en la ecuación anterior:

$$
x=0 \Rightarrow -2 = A(-1) \Rightarrow A = 2 \\ x=1 \Rightarrow 8=B(2) \Rightarrow B = 4 \\ x=-1 \Rightarrow -6=C(2) \Rightarrow C = -3
$$

Luego,

$$
\int{\frac{3x^2 + 7x -2}{x^3 -x}}dx = \int{\frac{2dx}{x}} + \int{\frac{4dx}{x-1}} - \int{\frac{3dx}{x+1}}
$$

**Caso 2: $Q(X)$ es producto de factores lineales, algunos de los cuales se repiten**.

 *Ejemplo*. Evalúe $\int{\frac{4x^2 + 2x +3}{(x-4)*(x+1)^2}}dx$.

 Primero, notamos que $Q(x)$ ya está factorizado. Por tanto,

$$
\frac{4x^2 + 2x +3}{(x-4)*(x+1)^2} = \frac{A}{x-4} + \frac{B}{x+1} + \frac{C}{(x+1)^2} \Rightarrow 4x^2 + 2x +3 = A(x+1)^2 + B(x-4)(x+1) + C(x-4)
$$

De nuevo, hallamos las constantes, sustituyendo valores adecuados de $x$ en la ecuación anterior:

$$
x=4 \Rightarrow 75=A(5)^2 \Rightarrow A=3 \\ x=-1 \Rightarrow 5=C(-5) \Rightarrow C=-1 \\ x=0 \Rightarrow 3=3+B(-4)+4 \Rightarrow B=1
$$

Luego,

$$
\int{\frac{4x^2 + 2x +3}{(x-4)(x+1)^2}}dx = 3*\int{\frac{dx}{x-4}} + \int{\frac{dx}{x+1}} - \int{\frac{dx}{(x+1)^2}}
$$

> **Nota**
>
> * Un factor cuadrático $a^2 + bx +c$ se dice que es irreducible si $b^2 - 4ac < 0$ (es decir, su discriminante es negativo).
>
> * *Todo polinomio se factoriza como producto de factores lineales y cuadráticos irreducibles*.
>
> * Para los siguientes 2 casos es útil saber que
>
> $$\int{\frac{1}{x^2 + a^2}}dx = \frac{1}{a}*\arctan{\frac{x}{a}} + C$$

**Caso 3: $Q(X)$ contiene factores cuadráticos irreducibles, de los cuales ninguo se repite**.

*Ejemplo*. Evalúe $\int{\frac{x^3 -x +6}{x^3 + 4x}}dx$.

Divimos la fracción, resultando:

$$
f(x) = 1 + \frac{-5x +6}{x*(x^2 +4)} = 1 + \frac{A}{x} + \frac{Bx +C}{x^2 +4}
$$

Igualando $\Rightarrow -5x +6 = A(x^2 +4) + Bx^2 + Cx \Rightarrow A=\frac{3}{2}, B=\frac{-3}{2}, C=-5$. Por tanto,

$$
\int{\frac{x^3 -x +6}{x^3 +4x}}dx = \int{1}dx + \frac{3}{2}*\int{\frac{dx}{x}} - \frac{3}{2}*\int{\frac{x}{x^2 +4}}dx - 5*\int{\frac{1}{x^2 +4}}dx
$$

**Caso 4: $Q(X)$ contiene factores cuadráticos irreducibles repetidos**.

*Ejemplo*. Evalúe $\int{\frac{-x^3 +2x^2 -x +1}{x*(x^2 +1)^2}}dx$.

En este caso,

$$
\frac{-x^3 +2x^2 -x +1}{x*(x^2 +1)^2} = \frac{A}{x} + \frac{Bx +C}{x^2 +1} + \frac{Dx +E}{(x^2 +1)^2}
$$

Procediendo como en los ejemplos anteriores, se llega a que $A=1$, $B=-1$, $C=-1$, $D=1$ y $E=0$.

$$
\int{\frac{-x^3 +2x^2 -x +1}{x*(x^2 +1)^2}}dx = \int{\frac{dx}{x}} - \int{\frac{x}{x^2 +1}}dx - \int{\frac{1}{x^2 +1}}dx + \int{\frac{x}{(x^2 +1)^2}}dx
$$

> **Nota**
>
> Existen muchas funciones a las que no les podemos hallar una antiderivada con los métodos vistos. Por ejemplo,
>
> $\int{\frac{e^x}{x}}dx$; $\int{\frac{\sin{x}}{x}}dx$; $\int{\frac{1}{ln(x)}}dx$; $\int{\cos{e^x}}dx$; $\int{\sin{x^2}}dx$; $\int{\sqrt{x^3 +1}}dx$
>
> Son integrales que no podemos expresar como funciones elementales. Para resolverlas requerimos otros métodos.

En esta clase extendemos el concepto de integral definida al caso en que el intervalo de integración sea infinito, y también al caso en que $f$ tiene una discontinuidad infinita en $[a, b]$. En cada caso, la integral se denomina impropia.
