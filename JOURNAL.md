# JOURNAL del progetto di Interactive 3D Graphics:
Scafidi Roberto Antonino - Ziero Samuele - De Reggi Paolo

Progetto per il secondo parziale del corso di Interactive 3D Graphics (2018/2019) con consegna entro 17/06/2019.

Team:
Scafidi Roberto Antonino - 123125,
Ziero Samuele - 107201,
De Reggi Paolo - 123783.

## Idea generale e decisioni di design
L'idea di base è stata quella di progettare una pagina web per la pubblicizzazione di un coltello da sopravvivenza. Abbiamo costruito il sito in modo tale da presentare all'utente una pagina di un sito di e-commerce che permette l'acquisto del coltello sopra-descritto. La pagina sarà caratterizzata da una struttura a colonne in cui la prima sarà usata per la modifica dei materiali, la seconda mostrerà l'oggetto tridimensionale e la terza permetterà la possibilità di cambiare sfondo (cubemap). Infine nella parte sottostante abbiamo deciso di inserire una descrizione dell'oggetto e il finto pulsante per l'acquisto.

## Progressi del progetto

**PARTENZA:**

![Prima bozza](Screenshot/bozza.png)
**PASSI DI SVILUPPO**
- Abbiamo scelto il modello a cui fare riferimento per il resto del progetto;
FOTO SKETCHFAB
- Abbiamo deciso il tipo di struttura da applicare al sito e quindi come sarebbe dovuta essere la "forma" del sito;
FOTO BOZZA SITO
- Abbiamo iniziato a implementare il sito, fino a decidere di riprogettare la pagina utilizzando un bootstrap per riuscire a lavorare in modo più efficiente in merito alla gestione delle larghezze della pagina e quindi renderla più responsive possibile;

## Scelte di implementazione
Abbiamo deciso di implementare la pagina web attraverso una struttura con bootstrap, cosi da gestire in modo ottimale gli spazi della schermata html.

## Problemi riscontrati e soluzioni
- Abbiamo riscontrato inizialmente un problema di caricamento dell'oggetto 3D nella pagina in quanto il formato era sbagliato per threejs, risolvendo attraverso la scelta di un modello più appropriata;
