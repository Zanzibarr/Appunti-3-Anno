# COS'E' UN PROBLEMA DI OTTIMIZZAZIONE
Quando abbiamo un insieme di decisioni da prendere collegate tra di loro con la possibilità di calcolare una misura quantificabile per valutare la mia decisione.
Ovviamente lo scopo è cercare la miglior decisione secondo la misura quantificabile.
Scopo del corso è trovare strumenti per poter risolvere problemi di ottimizzazione.

## MODELLAZIONE
Si passa da problema reale a modello matematico tramite la ==fase di modellazione==, creando un'astrazione del mondo reale attraverso la matematica.
Trovato il modello matematico, attraverso determinati algoritmi, bisogna determinare una soluzione, che poi viene interpreteata per essere implementata nel mondo reale.

Il corso si concentrerà principalmente sulla parte di modellazione.

## MODELLO MATEMATICO
Il modello matematico è strutturato da una ==serie di variabili== e da una ==funzione obiettivo==, che dalle variabili iniziali, determina il problema.
Oltre alla funzione obiettivo abbiamo anche dei ==vincoli==.
$$
\begin{cases}
min~f(x_1, ..., x_n)\qquad funzione~obiettivo\\\\
g_1(x_1, ..., x_n) \ge0\qquad\quad vincolo~1 \\\\
g_2(x_1, ..., x_n) \ge0\qquad\quad vincolo~2
\end{cases}
$$
Esempio dello zaino (vedi slides iniziali)
$$
\begin{cases}
max~4x_1+2x_2+10x_3+x_4+2x_5 \\\\
12x_1+x_2+4x_3+x_4+2x_5\le15 \\\\
x_1, ..., x_5\in\{0,1\}\qquad 0/1=non~preso/preso
\end{cases}
$$
Questi strumenti servono in svariate applicazioni in ogni campo, per ==supportare delle decisioni==, per un ==risparmio economico energetico==, quindi migliorare la qualità della vita.

### ESEMPI
#### Commesso viaggiatore
Trovare il percorso di minor lunghezza complessiva che visiti tutte le città una volta sola per poi tornare alla città di partenza.
Problema comune per compagnie di shipping (es Amazon, UPS, ecc)
#### Bin Packing
Dato un insieme di oggetti e un numero B, determinare il minimo numero di contenitori di una capacità B che possono contenere gli oggetti.
#### Graph Coloring
#### Cammino Minimo

## Come risolvere il problema?
In tutta generalità un arbitrario problema di ottimizzazione è ==indecidibile== (quando un algoritmo risolverebbe un'istanza in un tempo indeterminato)
Casi trattabili si ottengono restringendo i tipi di vincoli che si possono usare
Questo però riduce anche la loro applicabilità (risoluzioni così specifiche che ==nessun problema è formulabile==)
Dobbiamo trovare il miglior compromesso:
- ==programmazione lineare intera== è il miglior compromesso tra applicabilità ed efficienza (ci sono comunque problemi non modellabili in questo modo)

## PROGRAMMAZIONE LINEARE INTERA
- Funzinoe obiettivo e vincoli sono ==funzioni lineari==
- alcune o tutte le variabili devono assumere ==valori interi==
- è sufficientemente generale e riesce a modellare una grande varietà di problemi (per esempio tutti quelli visti in precedenza)
Questo paradigma è sviluppato da decenni, è quindi una tecnologia matura e affidabile