03/10/2022
# ENTITA'
Un'entità rappresenta un ==oggetto o concetto== del ==mondo reale==

# (aggiungo disegno)
![[Pasted image 20221006123445.png]]

La chiave primaria (univoca) identifica attraverso il suo valore un'unica istanza di un'entità
- singola: attributo univoco
- multipla: attributo composto

Es:
STUDENTE
MATRICOLA | COGNOME | NOME
------ | ------ | ------
001 | Pitagorico | Archimede
002 | De Paperis | Pico

ESAMI
CODICE | DENOMINAZIONE
------ | ------
001 | Analisi 1
002 | Fondamenti di Informatica
003 | Fisica 1

ESAMI SOSTENUTI
MATRICOLA | CODICE ESAME | DATA | VOTO
------ | ------ | ------ | ------
001 | 001 | 15/02/2020 | 30L
001 | 003 | 12/06/2020 | 30
002 | 001 | 14/06/2020 | 29
002 | 002 | 19/06/2020 | 30
001 | 002 | 01/07/2020 | 28

Nei database studente e esami, matricola e codice sono visti come attributi univoci, mentre nel database degli esami sostenuti, entrambe si uniscono per formare un attributo composto.

# (aggiungo disegno)

## DECOMPOSIZIONE DELLE ASSOCIAZIONI "MOLTI A MOLTI"
Un'associazione del tipo "molti a molti" ==non è implementabile== tramite un DBMS, dobbiamo ==decomporla in una serie di associazioni di tipo "uno a molti"== interponendo un'==entità di congiunzione==

Es:
# (aggiungo disegno)

# POSTGRESQL
Un sistema di ==gestione di database relazionali==
Nasce nel 1985 come Postgre, ma nel 1986 prende il nome modierno per evidenziare il supporto al linguaggio SQL.
Il punto di forza è la sua ==programmabilità==: può definire le ==User Defined Functions== (UDF)