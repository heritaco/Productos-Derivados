La **regla de Taylor** es una **función de reacción** para fijar la tasa objetivo $i_t$ en función de la inflación y la brecha de producto, diseñada para anclar precios y estabilizar el ciclo.

Versión con $r^*$ y $\pi^*$.

# Regla de Taylor

## 1) Forma canónica e intuición

$$
\boxed{\,i_t \;=\; r_t^{*} + \pi_t \;+\; \phi_{\pi}\,(\pi_t-\pi^{*}) \;+\; \phi_x\,x_t \;+\; \varepsilon_t\,}
$$

* $r_t^{*}$: tasa real neutral.
* $\pi^{*}$: objetivo de inflación.
* $\phi_{\pi}>1$: principio de Taylor. La tasa nominal sube más que la inflación ⇒ la tasa **real** aumenta ⇒ demanda se enfría.

Con inercia:

$$
i_t =(1-\rho)\Big[r_t^{*} + \pi_t + \phi_{\pi}(\pi_t-\pi^{*}) + \phi_x x_t\Big] + \rho\, i_{t-1} + \varepsilon_t,\quad \rho\in[0,1).
$$

## 2) Bloque nuevo-keynesiano

$$
\begin{aligned}
x_t &= \mathbb E_t x_{t+1} - \sigma\big(i_t - \mathbb E_t \pi_{t+1} - r_t^{*}\big),\\
\pi_t &= \beta\,\mathbb E_t \pi_{t+1} + \kappa\,x_t + u_t.
\end{aligned}
$$

Sustituir $i_t$ da un sistema con determinación única si $\phi_\pi>1$.

## 3) Lectura mecánica

* Shock de demanda $x_t\uparrow$ → $i_t\uparrow$ → $x_t\downarrow$, $\pi_t\downarrow$.
* Shock de oferta $u_t>0$: la regla limita el traspaso a $\pi$ sin colapsar actividad si $\phi_x>0$.
* $\rho$ reduce volatilidad financiera al suavizar trayectorias.

## 4) Neutralidad variable

$r_t^{*}$ cambia en el tiempo. Reglas prácticas filtran $r_t^{*}$ para evitar sesgos sistemáticos.

## 5) Economía abierta

Con prima cambiaria $\varphi_t$:

$$
i_t - i_t^{\text{ext}} \approx \mathbb E_t[\Delta s_{t+1}] + \varphi_t.
$$

Extensiones incluyen respuesta parcial a $\Delta s_t$ con cuidado para no violar $\phi_\pi>1$.

## 6) Parámetros y ZLB

Rangos empíricos: $\phi_\pi\in[1.3,2.0]$, $\phi_x\in[0.1,1.0]$, $\rho\in[0.5,0.9]$. En el **piso efectivo** se complementa con forward guidance y compras de activos.

## 7) Problemas empíricos

Medición en tiempo real de $x_t$ y $r_t^{*}$, endogeneidad de $\pi_t$, y riesgo de dominancia fiscal. Identificación vía SVARs o evidencia narrativa.

## 8) Estabilidad algebraica (esbozo)

Con $\rho=0$, alrededor de $(\pi^{*},x=0)$, la condición práctica es $\phi_\pi>1$ para evitar indeterminación expectacional.

## 9) Pseudocódigo

```
Input: π_t, x_t, π*, r*_t, φπ, φx, ρ
core = r*_t + π_t + φπ*(π_t - π*) + φx*x_t
i_t = (1-ρ)*core + ρ*i_{t-1}
Output: i_t
```

## 10) Síntesis

La regla de Taylor es un controlador parsimonioso que transforma señales de inflación y ciclo en una tasa $i_t$. Su potencia depende de tres piezas: reacción suficiente a la inflación ($\phi_\pi>1$), suavizamiento ($\rho>0$) y un $r_t^{*}$ bien estimado.

**En una línea**:

$$
\boxed{\text{Regla de Taylor}:\ i_t=r_t^{*}+\pi_t+\phi_\pi(\pi_t-\pi^{*})+\phi_x x_t\ \text{con}\ \phi_\pi>1,\ \rho>0,\ r_t^{*}\ \text{variable.}}
$$
