# Calculo Integral

**Capitulo 1**

1. [Notación Sigma](#notación-sigma)
2. El problema del área
3. El problema de la distancia
4. La integral definida
5. Propiedades de la integral definida
6. [Antiderivadas](#antiderivadas)
7. [Integral indefinida](#integral-indefinida)
8. Movimiento rectilíneo
9. [**Teorema Fundamental del Calculo** - Cómo evaluar integrales definidas](#teorema-fundamental-del-calculo---cómo-evaluar-integrales-definidas)
10. **Teorema Fundamental del Calculo** - Cómo construir antiderivadas
11. [La derivación y la integración como procesos inversos](#la-derivación-y-la-integración-como-procesos-inversos)
12. [Aplicaciones del teorema de evaluación](#aplicaciones-del-teorema-de-evaluación)
13. La Regla de Sustitución
14. Técnica de integración por partes
15. Integrales trigonométricas
16. Sustitución trigonométrica
17. Integración de funciones racionales mediante fracciones parciales
18. Integrales impropias de tipo 1: Intervalos infinitos
19. Integrales impropias de tipo 2: Integrandos con discontinuidad infinita
20. Prueba de comparación para integrales impropias

**Capitulo 2**

1. Áreas entre curvas
2. Volúmenes
3. Volúmenes mediante arandelas
4. Volúmenes mediante cascarones cilíndricos
5. Curvas definidas por medio de ecuaciones paramétricas
6. Cálculo con curvas paramétricas
    6.1. Tangentes
    6.2. Área en paramétricas
    6.3. Longitud de arco
7. Coordenadas polares
8. Curvas en polares
9. Áreas en coordenadas polares
10. Longitud de arco en polares
11. Trabajo
    11.1. Resortes
    11.2 Vaciado de tanques
12. Momentos y centros de masa

**Capitulo 3**

1. Sucesiones
2. Sucesiones monótonas
    2.1. Sucesiones recursivas
3. Series
4. Álgebra de series
5. Prueba de la integral
6. Prueba por comparación
7. Prueba por comparación en el límite
8. Series alternantes
    8.1. Estimación de la suma de una serie alternante
9. Convergencia absoluta
10. Pruebas de la razón y de la raíz
11. Series de potencias
    11.1. Radio e intervalo de convergencia
12. Representación de funciones como series de potencias
    12.1. Derivación e integración de series de potencias
13. Series de Taylor y de Maclaurin
    13.1. Series importantes de Maclaurin y sus radios de convergencia
    13.2. Multiplicación y división de series de potencias
    13.3. Aproximación de funciones por polinomios

<hr />

## Capitulo 1

### Notación Sigma

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

### Antiderivadas

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

### Integral Indefinida

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

#### Lista de integrales fundamentales

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

### Teorema Fundamental del Calculo - Cómo evaluar integrales definidas

El Teorema Fundamental del Cálculo recibe de manera apropiada este nombre porque establece una conexión entre las 2 ramas del cálculo: el cálculo
diferencial y el cálculo integral. Usando la relación inversa entre la integral y la derivada que afirma el teorema, Newton y Leibniz desarrollaron un
método sistemático que nos permite calcular con gran facilidad áreas, distancias e integrales definidas, sin tener que evaluarlas como límites de sumas.

> **Teorema de evaluación**
> 
> Sean $f$ una función continua en [a,b] y $F(x)$ una antiderivada de $f(x)$ en [a,b]. Entonces:
> 
> $\int_{a}^{b}{f(x)}dx = F(x)|_{a}^{b} = F(b) - F(a)$

### La derivación y la integración como procesos inversos

$$
\int_{a}^{x}{f(t)}dt = F(x) - F(a)
$$

$$
\frac{d}{dx}(F(x) - F(a)) = f(x)
$$

$$
\frac{d}{dx}\int_{a}^{x}{f(t)}dt = f(x)
$$

### Aplicaciones del teorema de evaluación

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

### Técnica de integración por partes

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
