13/10/2022

Per la progettazione di una base di dati non bastano solo le descrizioni sugli attributi, ma anche le ==descrizioni su come usare i vari dati==.

$\underline{Es.}$
Di un impiegato ci interessa:
- nome
- cognome
- età
- matricola
Un impiegato può essere assunto in una sola azienda
Azienda:
- nome
- nome della sede
- indirizzo della sede
In un'azienda ci sono minimo 5 impiegati

![[ER Dipendente Azienda 1.png]]

Quando ho un'entità legata ad un associazione con una cardinalità massima di 1, l'attributo dell'associazione ==potrebbe essere dato anche all'entità in questione==.
Si tratta di un ==problema di logica== più che di implementazione: l'attributo è legato di più all'attributo o all'associazione?

In generale, in quanto gli schemi E/R non sono molto flessibili, quando si introducono date, il processo per creare il database ==diventa più complesso==.

Posso aggiungere un'entità comune per aiutare l'utente a non sbagliare nell'inserimento dei dati:

![[ER Dipendente Azienda 2.png]]


Azienda diventa quindi un'==entità debole==: ha bisogno di un'altra entità per essere completa.
L'esistenza di entità deboli ==non deve snaturare le entità== (non abusare delle entità deboli)

In questo esempio, se un impiegato cambia azienda in cui lavora per poi tornare nell'azienda iniziale (se un impiegato potesse lavorare in più aziende), siccome l'attributo non è discriminante, non potrei avere più associazioni uguali ma con solo attributi diversi... devo usare un diagramma di un diverso tipo con un'entità intermedia (vedi esempio con l'incarico in $\underline{Lezione 3(P)}$)

Per quanto riguarda attributi identificativi visti sotto forma di relazioni, la cardinalità ==deve essere sempre (1,1)== in quanto l'identificativo deve esserci, e deve essere univoco.

![[ER Dipendente Azienda 3.png]]