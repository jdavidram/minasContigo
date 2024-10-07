# Calculo Integral

**Capitulo 1**

1. [Notación Sigma](#notación-sigma)
2. El problema del área
3. El problema de la distancia
4. La integral definida
5. Propiedades de la integral definida
6. [Antiderivadas](#antiderivadas)
7. Integral indefinida
8. Movimiento rectilíneo
9. **Teorema Fundamental del Calculo** - Cómo evaluar integrales definidas
10. **Teorema Fundamental del Calculo** - Cómo construir antiderivadas
11. La derivación y la integración como procesos inversos
12. Aplicaciones del teorema de evaluación
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

### Capitulo 1

## Notación Sigma

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

## Antiderivadas

En sesiones anteriores, vimos cómo evaluar integrales definidas usando sumas de Riemann. Ahora, la idea es obtener un método más eficiente y menos tedioso para calcular $\int_a^b f(x)dx$. Para tal fin introducimos el concepto de antiderivada.

> **Definición**
>
> Una función F se dice que es una *antiderivada* (o una primitiva) de una función $f$ sobre un intervalo $I$ si
> $$
> F'(x) = f(x)
> $$
> para todo $x \in I$

**Ejemplo.** $F(x) = \frac{x^4}{4}$ Es una antiderivada de $f(x) = x^{3} en I = (-\inf, \inf)$. En efecto,

$$
F'(x) = \frac{1}{4}*4x^3 = f(x)
$$

para todo $x \in I$

Notemos que $G(x) = \frac{x^4}{4} + 2024 es otra antiderivada de $f(x) = x^{3} en I$. En general, cualquier función de la forma

$$
H(x) = \frac{x^4}{4} + C \ , C \in \mathbb{R}
$$

es una antiderivada de $f(x) = x^3$ en $I$.

> **Teorema**
>
> Si F es una antiderivada de $f$ sobre $I$, entonces la antiderivada más general de $f$ sobre $I$ es
> $$
> F(x) + C
> $$
> Donde $C \in \mathbb{R}$ es una constante arbitraria

Necesitamos una notación adecuada para las antiderivadas que nos facilite el trabajo con ellas.
