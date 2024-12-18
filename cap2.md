# Áreas entre curvas

Ahora vamos a usar la integral definida para calcular áreas limitadas por las gráficas de 2 funciones.Sean $f$ y $g$ 2 funciones continuas en el intervalo $[a, b]$ con la condición $f(x) \geq g(x)$ en $[a, b]$:

![](https://calculo21.com/wp-content/uploads/2019/12/6.1_2.png)

El área del rectangulo diferencial es:

**Altura**

$$
f(x_{i}) - g(x_{i})
$$

$$
x_{i} \in [x_{i-1}, x_{i}]
$$

**Grosor**

$$
\Delta x = \frac{b - a}{n}
$$

Por tanto:

$$
A = lim_{n \to \infty}{\sum_{i = 1}^{n}{f(x_{i}) - g(x_{i})}*\Delta x}
$$

El **área** $A$ de la región limitada por las curvas $y = f(x)$ y $y = g(x)$, y las rectas $x = a$, $x = b$, donde $f, g$ son funciones continuas y $f(x) \geq g(x)$, para todo $x \in [a, b]$, está dada por:

$$
A = \int_{a}^{b}{[f(x) - g(x)]}dx
$$

# Volúmenes

Sea $A(x)$ el área de la sección transversal para cada punto $x \in [a, b]$. Definimos el **volumen** del sólido $S$ por:

$$
V(S) = \int_{a}^{b}{A(x)}dx
$$

## Volúmenes mediante discos

$$
V(S) = \pi*\int_{a}^{b}{R^{2}(x)}dx
$$

## Volúmenes mediante arandelas

![](https://i.ytimg.com/vi/J0eyio8uAoA/maxresdefault.jpg)

$$
V(S) = \pi*\int_{a}^{b}{R^{2}(x) - r^{2}(x)}dx
$$

## Volúmenes mediante cascarones cilíndricos

$$
V(S) = 2\pi*\int_{a}^{b}{d(x)*f(x)}dx
$$

* **Distancia al eje de giro**: $d(x)$

* **Altura del cilidro**: $f(x)$

# Trabajo

Para el estudio de este tema recordemos antes algunas unidades de medida para cantidades fisicas.

<table>
<thead>
<th>Cantidad (símbolo)</th>
<th>Internacional</th>
<th>Ingles</th>
</thead>
<tbody>
<tr>
<th>Longitud (L)</th>
<td><strong>Metros</strong>: m</td>
<td>pies (ft) = 0.3048 m</td>
</tr>
<tr>
<th>Masa (m)</th>
<td><strong>Kilogramo</strong>: kg</td>
<td>slug = 14.5939 kg</td>
</tr>
<tr>
<th>Tiempo (t)</th>
<td colspan="2" style="text-align: center"><strong>Segundo</strong>: s</td>
</tr>
<tr>
<th>Fuerza (F)</th>
<td><strong>Newton</strong>: N</td>
<td>libras (lb) = 4.44822 N</td>
</tr>
<tr>
<th>Trabajo (W)</th>
<td><strong>Joule</strong>: J</td>
<td>Libras-pie (lb-ft) = 1.356 J</td>
</tr>
</tbody>
</table>

* Segunda Ley de movimiento de Newton: $F = m*a = m*v'(t)$

* Gravedad: $g = 9.8*\frac{m}{s^{2}} = 32.2*\frac{ft}{s^{2}}$

* Densidad del agua: $\rho = \frac{m}{v} = 1000*\frac{kg}{m^{3}} = 1.94*\frac{slug}{ft^{3}}$

* Peso específico del agua: $\gamma = \rho * g = 9800 * \frac{N}{m^{3}} = 62.4 * \frac{lb}{ft^{3}}$

> **Nota:** Al trabajar este tipo de problemas debemos expresar todas las cantidades físicas en las mismas unidades.

Se define el trabajo como la cantidad de fuerza necesaria para mover un objeto una cierta distancia. Cuando se trabaja con una fuerza constante, se define el trabajo (W) como

$$
W_{Trabajo} = F_{Fuerza}*L_{Distancia}
$$

Para el caso en que la Fuerza y la distancia se definan como funciones, el trabajo resultante se define como una integral.

## Ley de Hooke

La **fuerza** requerida para mantener un resorte estirado *x* unidades mas allá de su longitud natural es proporcional a *x*:

$$
F(x) = k*x
$$

Donde $k > 0$ es **la constante elastica** del resorte.

Por lo tanto para calcular el trabajo de mover un resorte desde a hasta b (con respecto a la posición natural), se define la integral de la siguiente forma:

$$
F = F(x) = k*x
$$

$$
L = dx
$$

$$
dW = F * L = k * x * dx
$$

$$
\int{W}dW =  \int_{a}^{b}{k*x}dx
$$

## Ascensores

$$
F = g*(m + ((L_{total} - y)*\rho_{L}))
$$

$$
L = dy
$$

$$
dW = F * L = g * (m + ((L_{total} - y) * \rho_{L}))dy
$$

$$
\int{W}dW =  \int_{a}^{b}{g*(m + ((L_{total} - y)*\rho_{L}))}dy
$$

## Vaciado de tanques

$$
F = \gamma*dV
$$

$$
L = (y_{f} - y)
$$

$$
dW = F * L = (y_{f} - y) * \gamma * dv
$$

$$
\int{W}dW =  \int_{a}^{b}{(y_{f} - y)*\gamma}dV
$$
