## VARIABILI ALEATORIE CONTINUE
Per le variabili aleatorie continue, lo spazio degli eventi è
$$n:\ohm\to\mathbb{R}\qquad n\in\mathbb{R}$$
### FUNZIONE DI DISTRIBUZIONE
$$F_n(a)=P(n\leq a)$$
$$P(n\in (A,B])=P(n\leq B~\cap~n>A)=F_n(B)-F_n(A)$$
### DENSITA' DI PROBABILITA'
$$f_n(a)=\frac{dF_n(a)}{da}$$
$$\int_A^Bf_n(a)da=F_n(B)-F_n(A)=P(n\in (A,B])$$
$$\int_{-\infty}^{\infty}f_n(a)da=1$$
Da notare che calcolare $P(n=A)=\int_A^Af_n(a)da$ non ha senso

### ASPETTAZIONE
$$E(n)=\int_{-\infty}^{\infty}af_n(a)da=m_n$$
($f_n$ densità di probabilità)

## POTENZA STATISTICA DI UNA V. ALEATORIA
$$E(n^2)=\int a^2f_n(a)da$$
### VARIANZA
$$E((n-m_n)^2)=\int(a-m_n)^2F_n(a)da$$
### GAUSSIANA
Usata per modellare fenomeni fisici (es disturbo nei circuiti)
$$f_n(a)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2}(\frac{a-m}{\sigma})}$$
m media, $\sigma$ deviazione standard

## GAUSSIANA STANDARD
$$n\sim N(0,1)\qquad con~media~0~e~varianza~1$$
### FUNZIONE DI DISTRIBUZIONE
$$\Phi(a)=P(n\leq a)$$
### FUNZIONE DI DISTRIBUZIONE COMPLEMENTARE
$$Q=1-\Phi(a)$$
## GAUSSIANA NON STANDARD
$$n\sim N(m, \sigma^2)\qquad con~m\neq0~e~\sigma^2\neq1$$
### FUNZIONE DI DISTRIBUZIONE COMPLEMENTARE
$$P(n>A)=\int_A^{\infty}\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2}(\frac{\sigma-m}{\sigma})^2}da$$
$$b=(\frac{a-m}{\sigma})^2\quad db=\frac{da}{\sigma}\quad a=\sigma b+m$$
$$P(n>A)=\int_{\frac{A-m}{\sigma}}^{\infty}\frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}b^2}db=Q(\frac{A-m}{\sigma})$$
## SOMMA DI GAUSSIANE INDIPENDENTI
$$n_1\sim N(m_1, \sigma_1^2)\quad n_2\sim N(m_2,\sigma_2^2)$$
$$y=n_1+n_2\sim N(m_1+m_2,\sigma_1^2+\sigma_2^2)$$

----
# SEGNALI
Un segnale è una funzione del tempo $\qquad s(t)\in\mathbb{R}\quad t:tempo$
Ad esempio una trasmissione su un canale analogico/continuo avviene per mezzo di segnali.

Il ==tempo== può essere considerato ==continuo== o ==discreto==
- I segnali a tempo continuo vengono indicati con $y(t)$
- I segnali a tempo discreto vengono indicati con $s(KT)$ con ==T quanto temporale== (tempo che intercorre ==tra due osservazioni sequenziali==)

I valori assunti dai segnali possono essere:
- continui: il segnale assume valori $\in \mathbb{R}$/sottoinsiemi
- discreti: il segnale assume valori discreti (approssimati)

I ==segnali analogici== sono ==segnali continui== con ==valori continui==
I ==segnali digitali== sono ==segnali discreti== con ==valori discreti==

Es:
$$
rect(t)=
\begin{cases}
0\qquad t<-\frac{1}{2}\lor t>1 \\\\
1\qquad t\in[-\frac{1}{2};\frac{1}{2}]
\end{cases}
$$
![[rect(t).png]]
$$
triang(t)=
\begin{cases}
0\qquad t<-1\lor t>1 \\\\
1-|t|\qquad t\in[-1;1]
\end{cases}
$$
![[triang(t).png]]
## RITARDO DI UN SEGNALE
Un ritardo di un segnale avviene quando l'intero segnale è trasposto di un tempo $t_0$:
$$s(t)=y(t-t_0)$$
## SCALAMENTO DI UN SEGNALE
Amplificare o diminuire l'ampiezza di un segnale:$$s(t)\to As(t)$$Scalo il grafico di s(t) di un fattore A

## SCALAMENTO DEL TEMPO
Dilatare o comprimere nel tempo il segnale:$$s(t)\to s(Bt)$$Dilato il grafico di s(t) di un fattore B

# CANALE ELEMENTARE
![[Canale elementare.png]]
$$R(t)=AS_{TX}(t-t_0)$$ versione ritardata e scalata del segnale inviato