I passaggi per la creazione di un DB sono:
- ==Analisi dei requisiti==
- ==Progettazione concettuale==
- ==Progettazione logica==
- ==Progettazione fisica==

Ci sono ovviamente vari problemi, tipo ==questioni temporali== (range di date) che sono ==difficili da rappresentare== in E/R
Dobbiamo quindi mettere un ==vincolo stretto== nell'analisi dei requisiti

Es:
Se nel DB di uno studente viene inserita anche la data di nascita, se si ritiene che tale proprietà è utile, va data la motivazione nei requisiti

Inoltre bisogna sempre avere un ==attributo identificatore==:
- ho un insieme di attributi utilizzabile come identificatore? uso quello
- non ho un attributo identificarore? ==ne creo uno fittizio== (ID)

Creare ID fittizi ==può creare inonsistenze== (creare due volte lo stesso elemento con diversi ID)

### CONDIZIONE DI ESISTENZA
Si dice che se un entità è in relazione con un'altra:
- min("rami uscenti da A")=0 (ci possono essere ==oggetti senza associazioni==)
- max("ramu uscenti da A")=n

ciò indica la cardinalità(min, max) che rappresenta il numero di associazioni tra le due entità