
# Ejercicio 4 — Normal estándar vía aceptación–rechazo

## (a) Densidad de ∣Z∣|Z|

Sea Z∼N(0,1)Z\sim\mathcal N(0,1). Para x>0x>0:

P(∣Z∣≤x)=P(−x≤Z≤x)=Φ(x)−Φ(−x)=2Φ(x)−1.P(|Z|\le x)=P(-x\le Z\le x)=\Phi(x)-\Phi(-x)=2\Phi(x)-1.

Derivando:

f∣Z∣(x)=ddx [2Φ(x)−1]=2ϕ(x)=2π e−x2/2,x>0.f_{|Z|}(x)=\frac{d}{dx}\,[2\Phi(x)-1]=2\phi(x) =\boxed{\sqrt{\frac{2}{\pi}}\,e^{-x^{2}/2}},\quad x>0.

## (b) Asignando signo recupera N(0,1)N(0,1)

Sea S∼Unif{+1,−1}S\sim\text{Unif}\{+1,-1\} independiente de ∣Z∣|Z|. Para z∈Rz\in\mathbb R:

fS∣Z∣(z)=12f∣Z∣(∣z∣)+12f∣Z∣(∣z∣)=f∣Z∣(∣z∣)=ϕ(z),f_{S|Z|}(z)=\tfrac12 f_{|Z|}(|z|)+\tfrac12 f_{|Z|}(|z|)=f_{|Z|}(|z|)=\phi(z),

luego S ∣Z∣∼N(0,1)\boxed{S\,|Z|\sim \mathcal N(0,1)}.

## (c) A–R con X∼Exp(1)X\sim\mathrm{Exp}(1)

Propuesta g(x)=e−xg(x)=e^{-x} en x>0x>0 y objetivo f(x)=f∣Z∣(x)f(x)=f_{|Z|}(x).

f(x)g(x)=2π e−x2/2e−x=2π e−(x−1)22 e1/2.\frac{f(x)}{g(x)}=\sqrt{\frac{2}{\pi}}\,\frac{e^{-x^2/2}}{e^{-x}} =\sqrt{\frac{2}{\pi}}\,e^{-\frac{(x-1)^2}{2}}\,e^{1/2}.

El máximo es en x=1x=1, así

c=2eπ,f(x)c g(x)=e−(x−1)22.\boxed{c=\sqrt{\frac{2e}{\pi}}},\qquad \frac{f(x)}{c\,g(x)}=e^{-\frac{(x-1)^2}{2}}.

**Regla:** genera Y∼Exp(1)Y\sim\mathrm{Exp}(1), U∼U(0,1)U\sim U(0,1); acepta ∣Z∣=Y|Z|=Y si

U≤exp⁡ ⁣(−(Y−1)22).\boxed{U\le \exp\!\Big(-\tfrac{(Y-1)^2}{2}\Big)}.

Luego toma Z=S∣Z∣Z=S|Z| con S∼Unif{±1}S\sim\text{Unif}\{\pm1\}.  
Prob. de aceptación =1/c=π/(2e)=1/c=\boxed{\sqrt{\pi/(2e)}}.

## (d) Identidad con exponenciales i.i.d.

Si V1,V2Exp(1)V_1,V_2\overset{iid}{\sim}\mathrm{Exp}(1),

P ⁣[V1≥(V2−1)22]=∫0∞P ⁣[V1≥(y−1)22]e−y dy=∫0∞e−(y−1)22 e−y dy=∫0∞exp⁡ ⁣(−y2+12) dy=e−1/2 ⁣∫0∞e−y2/2 dy=π2e.\begin{aligned} P\!\left[V_1\ge \frac{(V_2-1)^2}{2}\right] &=\int_0^\infty P\!\left[V_1\ge \tfrac{(y-1)^2}{2}\right] e^{-y}\,dy =\int_0^\infty e^{-\frac{(y-1)^2}{2}}\,e^{-y}\,dy\\ &=\int_0^\infty \exp\!\Big(-\tfrac{y^2+1}{2}\Big)\,dy =e^{-1/2}\!\int_0^\infty e^{-y^2/2}\,dy =\boxed{\sqrt{\frac{\pi}{2e}}}. \end{aligned}

Coincide con la prob. de aceptación de (c).
