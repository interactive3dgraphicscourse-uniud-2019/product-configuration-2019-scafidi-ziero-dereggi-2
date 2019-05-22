# JOURNAL del progetto di Interactive 3D Graphics:
Scafidi Roberto Antonino - Ziero Samuele - De Reggi Paolo

Progetto per il secondo parziale del corso di Interactive 3D Graphics (2018/2019) con consegna entro 17/06/2019.

Team:
Scafidi Roberto Antonino - 123125,
Ziero Samuele - 107201,
De Reggi Paolo - 123783.

## Idea generale e decisioni di design

L'idea generale del progetto è stata quella di sviluppare una scena interattiva costituita da elementi animati automaticamente ed elementi comandati dall'utente. Abbiamo pensato dunque a una scena ispirata alla cinematografia del Far West (da cui la citazione del titolo "Per un pugno di boxes" in riferimento al quasi omonimo film), costituita da un ambiente di campagna con una ferrovia, il cui treno è azionabile dall'utente attraverso i tasti W e S della tastiera. L'animazione prevede l'accelerazione e decelerazione del treno, seguita poi dai vari elementi della scena che arricchiscono l'ambiente.

## Progressi del progetto

**PARTENZA:**
Siamo partiti con lo sviluppo dell'idea di design attraverso il disegno grafico a mano. Siamo riusciti a coincidere le varie idee per un fine comune, costruendo un mockup su carta per poi svilupparne uno attraverso mezzi elettronici.
![Prima bozza](Screenshot/bozza.png)
**PASSI DI SVILUPPO**
- Abbiamo costruito dei placeholder nella scena, inserendo dei cubi neri all'interno del ground per definire gli spazi e renderci conto di come sarebbero stati posizionati i vari elementi nella scena.
- Il passo successivo è stato quello di ricolorare gli elementi cosi da renderci conto in modo preciso cosa andava fatto. In questo modo abbiamo costituito gli elementi base: mulino, casa, treno.
- Sostituzione dei primi placeholder con oggetti 3D. Il primo passo è stato inserire l'oggetto mulino con il suo blocco di rotazione. Dopo aver studiato i moti di rotazione che avremmo voluto ottenere, sono state implementate le prime cinematiche anche se i movimenti al momento non risultano fluidi abbastanza.
![Primi step](Screenshot/placeholder.png)
- Creazione di una legge oraria per il mulino che viene predisposto di un tempo per cui si muove inizialmente accelerando verso destra per poi decellerare e continuare per il verso opposto. Viene dunque creata una rototraslazione in quanto anche le pale procedono la loro rotazione per seguire il vento.
- Ottimizzazione della funzione cinematica cosi da consentire un movimento fluido e naturale.
- Inizio di attribuzione delle texture agli elementi mulino e applicazione della texture per il ground. In questo modo è stato più semplice immaginare il proseguimento della creazione degli altri oggetti.
- Costruzione della ferrovia e quindi della traiettoria che dovrà seguire il treno. E' stato pensato attraverso la creazione di elementi "traversina" che costituiscono il supporto per la rotaia.
![Treno beta](Screenshot/trenino_beta.png)
- Avendo quindi costruito la traiettoria per il treno è stata implementata la funzione per intercettare il pulsante da tastiera cosi da poter gestire l'aumento o la diminuzione della velocità del treno. 
- Modifica dei valori della traiettoria della ferrovia (inizialmente circolare), per l'alternativa ellittica, considerata più adatta al paesaggio.
- Costruzione della casa, della bandiera e dell'omino. 
![Casa omino e bandiera](Screenshot/casa.png)
- Costruzione della locomotiva e inserimento della legge oraria che permette al treno di muoversi all'interno della ferrovia. 
- Aggiunta elementi nuvole attraverso la combinazione di cubi posti in alto.
![Nuvole](Screenshot/nuvole.png)
- Sistemazione animazione della bandiera e dell'omino con inserimento dei vincoli per il movimento ristretto a un campo d'azione.
- Creazione del vagone e aggiunta blocchi di contenuto al suo interno.
- Costruzione dei vincoli per il treno e il vagone, cosi da permettere un movimento (senza possibilità di deragliare) naturale.
- Creazione cespugli, alberi, cactus e inserimento texture 
- Sviluppo del movimento sincronizzato dell'omino al passaggio del treno. Applicazione movimento alle nuvole e restrizione legge oraria della bandiera
- Cambio di struttura delle rotaie cosi da da rendere realistica la scena inserendo le traversine sotto la rotaia stessa.
- Sistemazione delle texture e resizing della immagini in potenza di 2 cosi da ottimizzare la visualizzazione della scena.
- Inserimento limiti sull'accelerazione del treno che inizialmente andava in crescita esponenziale.
- Aggiunta fumo dal caminetto del treno e implementazione attivazione unicamente nel momento in cui il treno si muove.
![Nuvole](Screenshot/treno.png)
- Aggiunta una splashscreen che permette all'utente di apprendere le nozioni base di come muoversi nella scena.
- Aggiunta heigthmap alla scena che consente di visualizzare un ground differente alla scena.
- Aggiunta una funzione per gestire dinamicamente le altezze degli oggetti sul piano al variare della heightmap.
- Ottimizzazione heigthmap per evitare la riduzione dei fps.
- Correzione bug finali, inserimento commenti e ottimizzazione codice.


## Scelte di implementazione

Abbiamo deciso di implementare una splash-screen per dare le indicazioni all'utente dei comandi utilizzabili, attraverso una schermata in stile "The Simpson" che si dissolve attraverso uno zoom-in cosi da creare un ambiente più immersivo.

Abbiamo deciso di costruire il movimento del treno in modo che l'accelerazione sia limitata ad una soglia massima, e permettere, dopo il rilascio del tasto, una decelerazione costante fino all'arresto del treno stesso.

Abbiamo deciso di sviluppare l'animazione del omino in modo tale da attivarsi automaticamente solo nel momento in cui il treno passa in prossimità della sua figura.

## Problemi riscontrati e soluzioni

Per la risoluzione dei problemi abbiamo adottato il metodo Divide et Impera, suddividendo i problemi in sottoproblemi di minore complessita, cosi da suddividerci i compiti e riuscire a raggiungere un risultato nel minor tempo possibile.

I principali problemi sono stati quelli in merito alla creazione delle leggi orarie per i movimenti degli oggetti 3D, ma siamo riusciti ad ottenere il risultato che ci aspettavamo attraverso modifiche in produzione e test sulla visibilità.

Abbiamo inoltre riscontrato una inefficienza nella produzione di texture, che ci ha portato al resizing di tutte le immagini utilizzate, cosi da permettere una visualizzazione più immediata della scena, e che non comporti una attesa di caricamento eccessiva.

Abbiamo riscontrato un grosso problema per quanto riguarda l'implementazione della heigthmap; Abbiamo notato che per l'inserimento della stessa, anche al piccolo aumentare del numero di cubi che andavano a inserirsi nel ground, si denotava un abbassamento considerevole del frame rate per secondo. La soluzione è stata dunque quella di studiare la creazione di cubi al variare della gradazione di grigio e quindi costruire una heigthmap leggera ed efficiente.
