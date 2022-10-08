## CAMPIONAMENTO DI UN SEGNALE
Dato un segnale a tempo continuo $s(t)$, la sua versione campionata con un periodo di campionamento T $x(nT)$ ==trasforma il segnale da tempo continuo a tempo discreto a valori discreti==

![[Campionamento.png]]
campionamento = provocare una ==perdita della qualità del segnale==

## INTERPOLAZIONE
Fisicamente non posso fare avvenire variazioni immediate del segnale (far "esplodere" il segnale)
L'interpolazione ci permette di ==passare da segnali a tempo discreto a un segnale a tempo continuo==:$$s(t)=\sum_{n=-\infty}^{\infty}x(nT)h(t-nT)$$con $h(t)$ risposta impulsiva dellìintermpolatore (segnale a tempo continuo)
![[interpolazione.png]]

## HOLDER
$$h(t)=rect(\frac{t-T/2}{T})$$
risolvendo:
$$
h(t)=
\begin{cases}
1\qquad0<t<T\\\\
0\qquad altrove
\end{cases}
$$
(guardo $\underline{Lezione~2}$ rect(t) per riferimento grafico)

Applicando l'holder a un segnale $x(nT)$:
![[Holder su un segnale discreto.png]]