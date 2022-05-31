# Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni.




## Dipartimenti
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
area_di_distudio: VARCHAR(200), NOTNULL
città: VARCHAR(100), NULL
nome: VARCHAR(100), NULL

## Corsi_di_laurea
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
area_specialistica: VARCHAR(200), NOTNULL

## Corsi
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
branca: VARCHAR(200), NOTNULL
data: DATETIME NULL

## Insegnanti
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
nome: VARCHAR(100), NOTNULL
cognome: VARCHAR(100), NULL
Materia: VARCHAR(200), NOTNULL


## Appelli
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
data: DATE, NOTNULL
ora: TIME, NOTNULL
materia: VARCHAR(200), NOTNULL
crediti: TINYINT
voto: TINYINT

## Studenti
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
nome: VARCHAR(100), NOTNULL
cognome: VARCHAR(100), NOTNULL

## Voti
id: SMALLINT/ PRIMARY_KEY, UNIQUE, AUTO_INCREMENT, NOTNULL, INDEX
materia: VARCHAR(200), NOTNULL
voto: TINYINT