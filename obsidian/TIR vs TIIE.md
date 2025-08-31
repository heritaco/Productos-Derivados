Sí. La **tasa de referencia de Banxico** (tasa objetivo O/N) **ancla** y **desencadena** a la **TIIE**. La causalidad operativa es: política monetaria → fondeo overnight → cotizaciones interbancarias → TIIE por plazo. No al revés.

# Ensayo técnico breve

## 1) Taxonomía mínima

* **Tasa objetivo O/N**: meta operativa de Banxico para el costo del fondeo interbancario a 1 día. Instrumentada con operaciones de mercado abierto y un corredor de liquidez.
* **TIIE $n$**: tasa fija “representativa” a $n\in\{28,91,182\}$ días, calculada por Banxico a partir de cotizaciones bancarias. Sintetiza expectativas del O/N futuro más una prima por plazo y liquidez.
* **TIIE de Fondeo**: indicador del fondeo efectivo O/N. Fluctúa alrededor de la tasa objetivo.

## 2) Mecanismo causal

Sea $r_{d}$ la tasa O/N esperada para el día $d$ y $n$ el tenor de la TIIE. Ignorando redondeos y festividades,

$$
\text{TIIE}_{n}
\;\approx\;
\frac{360}{n}\!\Bigg[\prod_{d=1}^{n}\Big(1+\tfrac{\mathbb{E}_t[r_{d}]}{360}\Big)-1\Bigg]
\;+\;\Pi_n,
$$

donde $\Pi_n$ es la **prima por plazo** (liquidez, riesgo, microestructura). Usando log-linealización:

$$
\text{TIIE}_{n}\;\approx\;\frac{1}{n}\sum_{d=1}^{n}\mathbb{E}_t[r_{d}] \;+\; \Pi_n.
$$

Un ajuste de la **tasa objetivo** cambia $\mathbb{E}_t[r_d]$ en el tramo relevante del horizonte y, por ende, **re-precifica** la TIIE. El tamaño de la respuesta depende de:

1. Magnitud y sorpresa del movimiento de Banxico.
2. Señal de trayectoria futura (forward guidance).
3. Liquidez y condiciones de balance bancario ($\Pi_n$).

## 3) Regla de decisión y expectativas

Banxico sigue una regla de reacción implícita tipo-Taylor:

$$
r^{\star}_t \approx r^{\text{neutral}} + \phi_\pi(\pi_t-\pi^{\text{objetivo}}) + \phi_y\,\text{brecha}_t.
$$

El mercado transforma esta función de reacción en **trayectorias esperadas** del O/N. Por hipótesis de expectativas (Fisher-Wicksell) con prima de plazo:

$$
\text{TIIE}_{n} = \frac{1}{n}\sum_{k=1}^{n}\mathbb{E}_t[r_{t+k}^{\text{O/N}}] + \text{TermPremium}_n.
$$

Por eso, un alza “temporal” del objetivo suele mover más a **TIIE-28** que a **TIIE-182**; si el mercado anticipa recortes posteriores, la curva se empina menos o incluso se **aplana**.

## 4) Microestructura operativa

* **Corredor**: la ventanilla permanente y las operaciones de liquidez crean un rango alrededor del objetivo. Cuanto más **tenso** el fondeo, mayor el spread $(\text{TIIE de Fondeo} - \text{objetivo})$.
* **Fixing TIIE**: bancos cotizan tasas fijas a $n$ días; Banxico depura y publica el fixing. En estrés, $\Pi_n$ aumenta por demanda de balance y riesgo de liquidez.

## 5) Derivados y transmisión

La TIIE es el **activo subyacente** de gran parte del mercado de tasas en MXN:

* **IRS TIIE**: el pagador fijo recibe flotante ligado a TIIE (o TIIE de Fondeo). Precio del swap $\Rightarrow$ promedio descontado de TIIE futuras.

  $$
  \text{ParSwap}_T \approx \frac{\sum_{i} \Delta_i \,\mathbb{E}_t[\text{TIIE}_{i}]\,DF_i}{\sum_{i} \Delta_i\,DF_i}.
  $$
* **FRA / F-TIIE**: tasa forward implícita entre $t_1$ y $t_2$:

  $$
  1+F(t_1,t_2)\frac{\delta}{360}=\frac{P(t,t_1)}{P(t,t_2)},\quad F\approx\text{TIIE forward}.
  $$
* **Bonos flotantes**: cupones indexados a TIIE trasladan cambios de política a costos de financiamiento corporativo y bancario.

La **señal de Banxico** recorre la cadena: objetivo $\to$ O/N $\to$ TIIE $\to$ IRS/FRA $\to$ crédito y precios de activos.

## 6) Ejemplo numérico estilizado

Objetivo sube **50 pb** hoy, y el mercado internaliza: **+50 pb** por 1 mes, **+25 pb** meses 2–3, sin cambios después. Aproximando:

$$
\text{TIIE}_{28}\uparrow \approx 50\text{ pb} + \Pi_{28}\text{ (casi 1:1)}.
$$

$$
\text{TIIE}_{91}\uparrow \approx \frac{50+25+25}{3} \approx 33\text{ pb} + \Pi_{91}.
$$

$$
\text{TIIE}_{182}\uparrow \approx \text{promedio menor}\;+\;\Pi_{182}.
$$

Si, además, sube la aversión a la liquidez, $\Pi_n$ crece y **amplifica** el movimiento en los plazos más largos.

## 7) Qué **no** es TIR aquí

“TIR” en finanzas corporativas = **tasa interna de retorno** de un proyecto. No determina TIIE. Para evitar ambigüedad, usa **“tasa objetivo”** o **“tasa de referencia de Banxico”** cuando hables de política monetaria.

## 8) Diagnóstico rápido de causalidad

* **Corto plazo**: $\Delta \text{TIIE}_{28}\approx \Delta \text{objetivo}$ si el movimiento es sorpresivo.
* **Curva completa**: depende de la **trayectoria esperada** del objetivo.
* **Desalineaciones**: si TIIE sube más que el objetivo sin anuncio, típicamente es $\uparrow \Pi_n$ (escasez de liquidez, riesgo idiosincrático, quarter-end).

## 9) Síntesis formal

$$
\boxed{\text{TIIE}_{n}\;=\;\underbrace{\frac{1}{n}\sum_{d=1}^{n}\mathbb{E}_t[r^{\text{O/N}}_{t+d}]}_{\text{política monetaria y expectativas}}\;+\;\underbrace{\Pi_n}_{\text{prima por plazo/liquidez}}}
$$

La **tasa objetivo** de Banxico determina $r^{\text{O/N}}$ hoy y condiciona sus trayectorias esperadas. La **TIIE** es la proyección anualizada de ese camino, perturbada por una prima de plazo. En términos de sistema: el objetivo es el **control**, la TIIE es el **estado agregado** observado, y los derivados son **funciones de salida** que arbitran la información intertemporal.

> Wicksell apuntó que el nivel de la tasa de interés es un problema de “desviaciones persistentes” respecto a un ancla real; la técnica moderna lo reescribe como expectativas racionales más primas por riesgo.

**Conclusión**: la TIIE **no** guía a Banxico. Banxico guía a la TIIE a través de expectativas, operación de liquidez y primas de plazo. Para análisis y cobertura, modela $\mathbb{E}_t[r^{\text{O/N}}]$ y $\Pi_n$; todo lo demás es contabilidad de descuento.

La **Tasa de Interés de Referencia (TIR)** emitida por **Banxico** y la **Tasa de Interés Interbancaria de Equilibrio (TIIE)** son dos tasas de interés clave en el sistema financiero mexicano, pero operan en contextos y con mecanismos diferentes. A continuación, se expone un análisis comparativo detallado:

### 1. **Tasa de Interés de Referencia de Banxico (TIR)**

#### Definición y Función:

La **Tasa de Interés de Referencia (TIR)**, también conocida como **Tasa Objetivo de Banxico**, es la tasa de interés que el **Banco de México (Banxico)** establece como referencia para la política monetaria del país. Banxico la utiliza para **influir en las condiciones generales de liquidez** del sistema financiero, con el fin de alcanzar su objetivo primario: la **estabilidad de precios**, que se traduce en un control de la inflación. En términos generales, el **nivel de la TIR** tiene un impacto directo sobre otras tasas de interés, como las de los créditos y los depósitos, tanto en el mercado interbancario como en el comercial.

#### Mecanismo de Determinación:

La TIR se establece mediante el **Comité de Política Monetaria (CPM)** de Banxico, el cual se reúne periódicamente (normalmente cada mes) para decidir sobre las políticas monetarias a seguir. La decisión de ajustar la tasa se toma en función de diversos factores macroeconómicos, tales como:

* La inflación (objetivo primario).
* El crecimiento económico.
* La estabilidad financiera global y local.

El **cambio en la TIR** tiene un **impacto directo sobre el costo del dinero**, ya que afecta las tasas de interés en los mercados de crédito y deuda a corto plazo.

#### Propósito:

La TIR se utiliza principalmente como **herramienta de política monetaria** para controlar la inflación y regular la economía en términos de crecimiento y estabilidad financiera. A través de la manipulación de esta tasa, Banxico puede influir sobre la cantidad de crédito disponible, la tasa de ahorro, y la actividad económica en general.

### 2. **Tasa de Interés Interbancaria de Equilibrio (TIIE)**

#### Definición y Función:

La **TIIE** es una tasa de interés promedio a la que los bancos comerciales se prestan dinero entre sí en el mercado interbancario a plazos de 28, 91, 182 o 360 días, y se considera un indicador de las condiciones de liquidez en el sistema financiero mexicano.

La TIIE es calculada **diariamente** por la **Asociación de Bancos de México (ABM)** a partir de las tasas a las que los bancos transan en el mercado interbancario. Este cálculo no es una simple tasa promedio, sino que se toma en cuenta el **nivel de oferta y demanda de dinero** en el mercado interbancario, lo que le da una representación más dinámica y directa de las condiciones de liquidez en el sistema.

#### Mecanismo de Determinación:

La TIIE se basa en las **tasas de interés de las operaciones de crédito entre bancos**, especialmente en aquellas realizadas con **valores del gobierno y operaciones de repos**, y se calcula mediante un promedio ponderado de las tasas a las que los bancos se prestan dinero entre sí.

Aunque la **TIIE** no es una tasa fijada por un banco central como la **TIR**, sí está influenciada por las expectativas del mercado sobre las decisiones de política monetaria de Banxico. En otras palabras, si el mercado espera que Banxico suba o baje la TIR, es probable que la TIIE también se ajuste, ya que refleja las expectativas sobre el costo del dinero en el futuro cercano.

#### Propósito:

La TIIE refleja las condiciones de **liquidez y riesgo percibido** en el sistema financiero mexicano y se utiliza como **referencia para las tasas de interés de los créditos** a las empresas y consumidores en el país. Muchas instituciones financieras la utilizan como base para fijar tasas de interés en productos financieros como créditos personales, hipotecas y préstamos corporativos.

### Diferencias Clave:

1. **Origen y Propósito:**

   * **TIR (Banxico):** Establecida por Banxico para controlar la política monetaria y mantener la inflación bajo control.
   * **TIIE (Mercado Interbancario):** Determinada por el mercado interbancario con base en las transacciones entre bancos, y refleja las expectativas del mercado sobre el costo del dinero.

2. **Mecanismo de Determinación:**

   * **TIR (Banxico):** Decidida por Banxico en reuniones periódicas basadas en las condiciones económicas generales.
   * **TIIE (Mercado Interbancario):** Calculada por la ABM como un promedio ponderado de las tasas de interés a las que los bancos se prestan dinero.

3. **Impacto:**

   * **TIR (Banxico):** Afecta las decisiones de política monetaria, influye directamente sobre las tasas de interés interbancarias y las de los productos financieros en general.
   * **TIIE (Mercado Interbancario):** Es una tasa de referencia para los préstamos entre bancos y, por lo tanto, afecta a las tasas de interés en los productos de crédito de las instituciones financieras.

En resumen, aunque ambas tasas están interrelacionadas y Banxico tiene influencia indirecta sobre la TIIE, la **TIR** es una herramienta de política monetaria directa, mientras que la **TIIE** es un indicador del mercado interbancario, representando las condiciones de liquidez y el costo del dinero en un nivel más específico.
