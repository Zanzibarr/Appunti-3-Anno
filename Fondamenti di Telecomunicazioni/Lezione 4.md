06/10/2022

# ENERGIA DI UN SEGNALE
Per un segnale a tempo continuo:
$$E_x=\int_{-\infty}^{\infty}x^2(t)dt$$
Per un segnale a tempo discreto:
$$E_x=\sum_{n=-\infty}^{\infty}x^2(nT)$$
Energia consumata da una resistenza in un circuito:
$$E=\int_{-\infty}^{\infty}v(t)i(t)dt=\int_{-\infty}^{\infty}\frac{v^2(t)}{R}dt=\frac{1}{R}\int_{-\infty}^{\infty}v^2(t)dt=\frac{1}{R}E_v$$
Con $E_v$ l'energia del segnale $v(t)$

## POTENZA MEDIA DI UN SEGNALE
In un intervallo di tempo $[0,T]$

Sia $x(t)$ un ==segnale a tempo continuo==
$$P_x=\frac{1}{T}\int_0^Tx^2(t)dt$$

# SEGNALI CON SUPPORTO FINITO
SUPPORTO: ==insieme di punti== $\in$ D (=tempo) in cui il segnale è ==non nullo== $x(t)\neq0$
$$S=\{~t:x(t)\neq0~\}$$

# AMPLIFICAZIONE/ATTENUAZIONE
Sia $x(t)=As(t)$
$$E_x=\int_{-\infty}^{\infty}x^2(t)dt=\int_{-\infty}^{\infty}A^2s^2(t)dt=A^2\int_{-\infty}^{\infty}s^2(t)dt=A^2E_s$$

Spesso ci servirà trovare il ==rapporto tra potenze/energie== del segnale utile e disturbo per valutare la ==performance della trasmissione==

# DECIBEL dB
Consideriamo un rapporto tra le energie di due segnali $x(t), y(t)$
$$\frac{E_x}{E_y}~è~un~\underline{rapporto~adimensionale}$$
Ma misurata in $dB$:
$$(\frac{E_x}{E_y})_{dB}=10\log(\frac{E_x}{E_y})=10(\log(E_x)-\log(E_y))$$
è una ==rappresentazione in scala logaritmica== per poter ==passare da rapporto a differenza==

$dB$: legato al rapporto di energie e potenze
Se avrò $dB$ negativi, allora l'argomento del logaritmo sarà $\in [0,1]$

## SEGNALI A SUPPORTO FINITO
Per segnali a supporto finito si ha che $E_x=TP_x$, $E_y=TP_y$:
$$\frac{E_x}{E_y}=\frac{TP_x}{TP_y}=\frac{P_x}{P_y}$$

## POTENZA NEL MONDO LOGARITMICO
$$(P_x)_W\to(P_x)_{dBW}=10\log_{10}(P_x)_W$$

## SCALAMENTO DEL SEGNALE
Sia $x(t)=As(t)\to E_x=A^2E_s$
$$\frac{E_x}{E_s}=A^2\to(\frac{E_x}{E_s})_{dB}=(A^2)_{dB}=10\log_{10}(A^2)=20\log_{10}(A)$$
