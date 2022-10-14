11/10/2022

# SPAZIO VETTORIALE DI SEGNALI A ENERGIA FINITA

### PRODOTTO INTERNO
$$<x(t),y(t)>=\int_{-\infty}^{\infty}x(t)y(t)dt$$
### NORMA
$$||x(t)||=\sqrt{<x(t),y(t)>}=\sqrt{E_x}$$
$E_x$ energia del segnale

### BASE ORTONORMALE
Una base ortonormale di uno spazio vettoriale è un insieme di vettori (segnali) $x_1(t),...,x_n(t)$ t.c. $$<x_i(t),x_j(t)>=0,\quad i\neq j,\quad\forall i,j$$$$||x_i(t)||=1, \forall i$$ e inoltre deve valere che il generico segnale $y(t)\in V$ sia scrivibile come
$$
\begin{cases}
y(t)=\sum_{n=1}^N\alpha_nx_n(t)\\\\
\alpha_i=<y(t),x_i(t)>
\end{cases}
$$
I vettori sono ortogonali in quanto il ==prodotto interno (scalare) da 0==, sono normali in quanto il ==modulo di ogni vettore è 1==

$\underline{Es:}$
$$\int_{-\infty}^{\infty}x(t)y(t)dt=0$$
questo caso si verifica
- se i due segnali hanno ==sostegni diversi== (se sono non nulli in momenti diversi, il prodotto dei segnali sarà sempre nullo); in questo caso i segnali hanno ==supporto disgiunto==
  ![[Segnali a supporto disgiunto.png]]
- se l'area del prodotto dei due segnali è nulla![[Segnali ortogonali per prodotto.png]]

## SOTTOSPAZIO GENERATO DA UN INSIEME DI N SEGNALI A ENERGIA FINITA
Dati n segnali $s_1(t),...,s_n(t)$, il sottospazio generato da questi segnali è l'insieme dei vettori (compresi quelli ottenuti da operazioni tra vettori):
$$s(t)=\sum_{n=1}^N\alpha_ns_n(t),\qquad\alpha_n\in\mathbb{R},\quad \forall n$$
I vettori ==non sono per forza ortonormali==
Perchè si tratti di un sottospazio vettoriale bisogna che sia ==chiuso per le operazioni di somma e prodotto==
$$x(t)+y(t)=\sum_n\alpha_ns_n(t)+\sum_n\beta_ns_n(t)=\sum_n(\alpha_n+\beta_n)s_n(t)$$

Partendo da segnali che generano un sottospazio, posso descrivere il sottospazio con una base ortonormale di dimensione $I\leq N,~\phi_1(t),...,\phi_I(t)$
$$x(t)\iff x=[x1,...,x_I]$$
$$x(t)=\sum_{i=1}^Ix_i\phi_i(t)$$

## PRODOTTO INTERNO NEI DUE SPAZI
$<x(t),y(t)>$ con $x(t)$ e $y(t)$ nel sottospazio $\{\phi_1(t),...,\phi_I(t)\}$
$$x_i=<x(t),\phi_i(t)>$$
$$y_i=<y(t),\phi_i(t)>$$
----
$$<x(t),y(t)>=<\sum_{i=1}^Ix_i\phi_i(t),\sum_{i=1}^Iy_i\phi_i(t)>=\sum_{i=1}^I\sum_{j=1}^I<x_i\phi_i(t),y_j\phi_j(t)>$$$=^{*0}\sum_{i=1}^I\sum_{j=1}^Ix_iy_j<\phi_i(t),\phi_j(t)>=^{*1}\sum_{i=1}^Ix_iy_i<\phi_i(t),\phi_i(t)>=^{*2}\sum_{i=1}^Ix_iy_i$$
$$=<\underline{x},\underline{y}>$$
prodotto interno nello spazio euclideo.

\*0: per linearità
\*1: ortogonalità dei segnali della base
\*2: normalizzazione dei segnali della base

----

## ENERGIA
$$E_x=<x(t),x(t)>=\sum_{i=1}^Ix_i^2$$
## NORMA
$$||x(t)||=\sqrt{E_x}=\sqrt{\sum_{i=1}^Ix_i^2}=||\underline{x}||$$
## DISTANZA
$$d^2(x(t),y(t))=||x(t)-y(t)||^2=\int_{-\infty}^{\infty}[x(t)-y(t)]^2dt$$$$x(t)-y(t)=\sum x_i\phi_i(t)-\sum y_i\phi_i(t)=\sum(x_i-y_i)\phi_i(t)\to \underline{x}-\underline{y}$$$$d^2(x(t),y(t))=...=||\underline{x}-\underline{y}||^2=d^2(\underline{x},\underline{y})$$