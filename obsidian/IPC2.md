# TIIE

La TIIE es hoy la referencia central del costo del dinero en pesos a un día, es el precio base del dinero que usan bancos y empresas para fijar intereses de créditos, bonos, etc. Se estima con operaciones de reporte mayorista a un día liquidadas en INDEVAL, con colateral gubernamental o equivalente, y participantes bancarios y casas de bolsa. Con esa base transaccional Banxico reporta una tasa diaria representativa y, además, **índices de composición** que acumulan los factores diarios en días hábiles o naturales y versiones “compuestas por adelantado” útiles para contratos que requieren capitalización explícita, el resultado refleja lo que realmente ocurrió en el mercado (Banco de México, s. f.-a; s. f.-b).

En el CME, el futuro permite negociar la tasa compuesta; por convención se cotiza **Índice = 100 − 100R**, por ejemplo, hoy la tasa está en 8.0126% y su precio en el CME para el futuro de TIEU25 que termina el 30 de septiembre de 2025 es de 92.28. 

![[Pasted image 20250912232943.png]]

La Reserva Federal (Fed) considera iniciar recortes en la tasa de interés porque el mercado laboral muestra signos de enfriamiento, con creación de empleo revisada a la baja y un desempleo en leve ascenso, lo cual reduce presiones salariales y de demanda agregada (Reuters, 2025a); además, la inflación, aunque aún por encima del 2 %, evidencia cierta moderación y expectativas ancladas, lo que permite espacio de maniobra sin erosionar credibilidad (YCharts, 2025); al mismo tiempo, la tasa de política actual se mantiene en terreno restrictivo, por encima de la neutral, generando riesgo de una desaceleración excesiva (YCharts, 2025); sumado a ello, la economía estadounidense enfrenta señales de estancamiento y menor crecimiento, mientras el entorno global incrementa vulnerabilidades (Reuters, 2025b); finalmente, organismos como el FMI han señalado que la Fed dispone de margen para flexibilizar su postura monetaria, dado el deterioro en la dinámica laboral (Reuters, 2025c), y el propio Powell ha reconocido riesgos al empleo como argumento para abrir la puerta a recortes (Reuters, 2025d).

Si la Reserva Federal inicia recortes y el peso se mantiene estable, el mercado suele anticipar que la tasa **R** baje; entonces el precio de la TIIE sube. La ganancia o pérdida aproximada por contrato es $\Delta \text{P\&L} \approx 50{,}000 \times \Delta \text{Índice}$ MXN (Reuters, 2025; Banco de México, 2023; CME Group, 2025a, 2025b). El proceso se podría llegar a ver de la siguiente manera:
**1. Llega nueva información.** Por ejemplo, señales de inflación a la baja en EE. UU. y una guía de la Fed hacia **recortes consecutivos** (Reuters, 2025).
**2. Bajan las tasas de muy corto plazo en USD.** Se abarata el fondeo en dólares y el mercado desplaza a la baja la trayectoria esperada.
**3. Se relajan las condiciones financieras globales.** Menor aversión al riesgo y, a menudo, un USD más débil reducen la presión inflacionaria importada en México.
**4. Banxico evalúa el cuadro local.** Si inflación y tipo de cambio cooperan, el mercado anticipa recortes locales con **rezago** respecto a la Fed. Ese **sendero esperado** es lo que importa para los derivados.
**5. Desciende la F-TIIE esperada del trimestre.** La F-TIIE compuesta del periodo, $R$, baja si cada “gota” diaria es ligeramente menor.
**6. Sube el precio del Futuro.** Por convención, **menos R ⇒ más Índice**, porque Índice = 100 − R. un cambio de −25 pb en $R$ implica $+\!0.25$ puntos de índice.

Como ejemplo, supongamos que el mercado espera una tasa compuesta anualizada **$R = 10.00\%$**. El futuro cotiza cerca de **$100 − 10.00 = 90.00$**. Si, tras guías de recortes, el consenso pasa a **$R = 9.75\%$**, el precio sería **90.25**. La variación aproximada por contrato largo:

$$
\Delta \text{P\&L} \approx (90.25 - 90.00)\times 50{,}000 = \textbf{12{,}500 MXN}.
$$

Es cierto que esto no siempre es cierto, puede ser por distintas razones, como:
**Desacople local.** Un repunte de inflación mexicana o una depreciación del peso puede llevar a Banxico a demorar o recortar menos; $R$ baja menos y el futuro sube menos o corrige.
**Factores técnicos.** Primas a plazo, oferta de papel, reposicionamientos o efectos de calendario. La metodología de composición extiende la última tasa publicada en fines de semana y feriados, lo que introduce pequeñas diferencias entre meses y trimestres y un **basis** entre lo que quieres cubrir y lo que liquida el contrato (CME Group, 2025a, 2025b).












Se observa un **basis positivo en precio**: el **futuro** $F=92.28$ está **por encima** del “fair” $F^*=92.16$.  La **tasa mensual de mercado** es **menor** que la del modelo en ≈ **12 pb**, porque el mercado descuenta una **F-TIIE promedio más baja** para el mes que la que supone la fair, es decir, una senda restante de tasas **más suave**. 
Por lo que se espera que el precio de las tasas bajen en promedio. En futuros de tasa con convención **Índice = 100 − 100·R**, **precio más alto es por una tasa implícita más baja**. 

Se puede decir que le mercado esta vendiendo una tasa de
* **Implícita de mercado**: $R_{\text{mkt}}=(100-92.28)/100=\mathbf{7.72\%}$.
Mientras nosotros calculamos hoy una tasa de 
* **Modelo**: $R_{\text{mod}}=(100-92.16)/100=\mathbf{7.84\%}$.

* **Nivel vigente** (spot TIIE 28d ≈ 8.01%): como ya corrieron 12 días a \~8.01% y faltan 18, para que el promedio del mes sea 7.72% el tramo pendiente debe ir cerca de **7.49%**. Señal: **suavización** de la F-TIIE en lo que resta del mes.

Cabe resaltar que esto es una **expectativa de promedio mensual**, no una garantía de recorte puntual de política. El 7.72% incorpora carry y los días ya realizados; puede lograrse con leve descenso sostenido o con oscilaciones alrededor de \~7.5–7.6%. Si la base fuese negativa (precio < fair), la lectura sería la inversa: **alza** implícita del promedio.






## Bibliografía

Banco de México. (2023, junio 2). *Transición de las TIIE a plazos a la TIIE de fondeo*. [https://www.banxico.org.mx/publicaciones-y-prensa/miscelaneos/%7BDD5668BD-09DA-8AEB-1A34-C53EB4DFB8C6%7D.pdf](https://www.banxico.org.mx/publicaciones-y-prensa/miscelaneos/%7BDD5668BD-09DA-8AEB-1A34-C53EB4DFB8C6%7D.pdf)

Banco de México. (s. f.-a). *Overnight TIIE funding rate methodology* \[PDF]. [https://www.banxico.org.mx/markets/d/%7B1FDD2772-9F1C-FDA3-FBBC-AC641FE94CD2%7D.pdf](https://www.banxico.org.mx/markets/d/%7B1FDD2772-9F1C-FDA3-FBBC-AC641FE94CD2%7D.pdf)

Banco de México. (s. f.-b). *Índices de TIIE de Fondeo y TIIE de Fondeo compuesta* (cuadro CA766). [https://www.banxico.org.mx/SieInternet/consultarDirectorioInternetAction.do?accion=consultarCuadroAnalitico\&idCuadro=CA766\&locale=es\&sector=18](https://www.banxico.org.mx/SieInternet/consultarDirectorioInternetAction.do?accion=consultarCuadroAnalitico&idCuadro=CA766&locale=es&sector=18)

CME Group. (2025a). *A new era for Mexican rates: Inside three-month F-TIIE contracts*. [https://www.cmegroup.com/articles/2025/new-quarterly-contracts-for-mexican-funding-tiie-futures.html](https://www.cmegroup.com/articles/2025/new-quarterly-contracts-for-mexican-funding-tiie-futures.html)

CME Group. (2025b). *Three-Month F-TIIE overview*. [https://www.cmegroup.com/markets/interest-rates/stirs/three-month-f-tiie.html](https://www.cmegroup.com/markets/interest-rates/stirs/three-month-f-tiie.html)

CME Group. (2025c). *Chapter 474: Mexican Funding TIIE (Quarterly Contracts)*. [https://www.cmegroup.com/rulebook/CME/V/450/474.pdf](https://www.cmegroup.com/rulebook/CME/V/450/474.pdf)

CME Group. (2025d). *Mexican Funding TIIE (Monthly Contracts) overview*. [https://www.cmegroup.com/markets/interest-rates/stirs/mexican-monthly-f-tiie.html](https://www.cmegroup.com/markets/interest-rates/stirs/mexican-monthly-f-tiie.html)

Reuters. (2025, septiembre 12). *Morgan Stanley prevé cuatro recortes consecutivos desde la próxima semana*. [https://www.reuters.com/business/morgan-stanley-expects-three-us-interest-rate-cuts-this-year-2025-09-12](https://www.reuters.com/business/morgan-stanley-expects-three-us-interest-rate-cuts-this-year-2025-09-12)

Reuters. (2025a, septiembre 12). *Fed’s fear meter may be pointing to stagnation rather than stagflation*. Recuperado de [https://www.reuters.com/business/feds-fear-meter-may-be-pointing-stagnation-rather-than-stagflation-2025-09-12/](https://www.reuters.com/business/feds-fear-meter-may-be-pointing-stagnation-rather-than-stagflation-2025-09-12/)

Reuters. (2025b, septiembre 12). *Fed’s fear meter may be pointing to stagnation rather than stagflation*. Recuperado de [https://www.reuters.com/business/feds-fear-meter-may-be-pointing-stagnation-rather-than-stagflation-2025-09-12/](https://www.reuters.com/business/feds-fear-meter-may-be-pointing-stagnation-rather-than-stagflation-2025-09-12/)

Reuters. (2025c, septiembre 11). *IMF says Fed has scope to lower interest rates*. Recuperado de [https://www.reuters.com/markets/us/imf-says-fed-has-scope-lower-interest-rates-2025-09-11/](https://www.reuters.com/markets/us/imf-says-fed-has-scope-lower-interest-rates-2025-09-11/)

Reuters. (2025d, agosto 22). *Powell, citing jobs risk, opens door to cuts but doesn’t commit*. Recuperado de [https://www.reuters.com/markets/wealth/powell-citing-jobs-risk-opens-door-cuts-doesnt-commit-2025-08-22/](https://www.reuters.com/markets/wealth/powell-citing-jobs-risk-opens-door-cuts-doesnt-commit-2025-08-22/)

YCharts. (2025). *6 reasons leading to Fed rate cuts*. Recuperado de [https://get.ycharts.com/resources/blog/6-reasons-leading-to-fed-rate-cuts/](https://get.ycharts.com/resources/blog/6-reasons-leading-to-fed-rate-cuts/)
