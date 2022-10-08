03/10/2022
# ENTITA'
Un'entità rappresenta un ==oggetto o concetto== del ==mondo reale==

![[ERD-Auto_Studente_Fattura.png]]

La chiave primaria (univoca) identifica attraverso il suo valore un'unica istanza di un'entità
- singola: attributo univoco
- multipla: attributo composto

Es:
![[Tabelle Lezione 3 DB.png]]

Nei database studente e esami, matricola e codice sono visti come attributi univoci, mentre nel database degli esami sostenuti, entrambe si uniscono per formare un attributo composto.

![[ERD_Studente-(1,n)-Esame-(n,1)-Tipi Esame.png]]

## DECOMPOSIZIONE DELLE ASSOCIAZIONI "MOLTI A MOLTI"
Un'associazione del tipo "molti a molti" ==non è implementabile== tramite un DBMS, dobbiamo ==decomporla in una serie di associazioni di tipo "uno a molti"== interponendo un'==entità di congiunzione==

Es:
![[Decomposizione ERD.png]]

# POSTGRESQL
Un sistema di ==gestione di database relazionali==
Nasce nel 1985 come Postgre, ma nel 1986 prende il nome modierno per evidenziare il supporto al linguaggio SQL.
Il punto di forza è la sua ==programmabilità==: può definire le ==User Defined Functions== (UDF)