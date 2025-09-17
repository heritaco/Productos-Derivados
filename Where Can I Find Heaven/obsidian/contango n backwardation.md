Paso a paso con $S_0=50$, futuro a $F=80$ en 1 mes ($T$), sin costos ni conveniencia:

1. Calcula el “justo” sin fricciones

$$
F^{*}=S_0\,e^{rT}=50\,e^{rT}.
$$

2. Compara 80 contra $F^{*}$

## Contango
A) Si $80>F^{*}$  → **cash-and-carry** (arbitraje corto plazo) 

* Hoy $t=0$:

  1. Pide prestado $50$ al rate $r$.
  2. Compra 1 unidad del activo al contado $S_0=50$.
  3. Vende (abre corto) 1 futuro a $F=80$.
* En $t=T$:
  4\. Entrega el activo al vencimiento del futuro y recibe $80$.
  5\. Paga el préstamo: $50\,e^{rT}$.
* Ganancia segura: $\pi = 80-50\,e^{rT} = F - F^{*} >0$.

## Backwardation
B) Si $80<F^{*}$ → **reverse cash-and-carry**

* Hoy $t=0$:

  1. Pide prestado el activo y véndelo al contado: recibes $50$.
  2. Invierte los $50$ al rate $r$.
  3. Compra 1 futuro a $F=80$.
* En $t=T$:
  4\. Recibes el activo vía tu futuro pagando $80$.
  5\. Devuelves el activo prestado.
  6\. Cobras tu inversión: $50\,e^{rT}$.
* Ganancia segura: $\pi = 50\,e^{rT}-80 = F^{*}-F >0$.

3. Con fricciones de inventario, la paridad correcta es

$$
F = S_0\,e^{(r+u-y)T},
$$

donde $u$ = costos de guarda/seguro y $y$ = “convenience (inventario) yield”. Ajusta $F^{*}$ por $(u-y)$ antes de comparar.

Nota: en equilibrio sin fricciones no habrá arbitraje y $F=F^{*}$.

