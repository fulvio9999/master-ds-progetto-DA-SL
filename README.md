# master-ds-progetto-DA-SL

## TODO list:

1. Introduzione

dire che ci saraà una parte di clustering:
Specificare che si procederà nell'applicare i seguenti algoritmi di clstering: gerarchico agglomerativo, kmeans, kmedoids, mixture of gaussian.
Ognuna di queste si proverà con: tutte le variabili del dataset, soltante diagonal e bottom, soltanto 2 dalla PCA.

Un'altra parte di regression.

2. Descrizione del Dataset e Analisi Esplorativa

- [ ] Descrizione delle variabili (dimensione, tipologia, eventuali correlazioni) del dataset banknote.
- [ ] Analisi Esplorativa dei Dati (EDA)
- [ ] Preprocessing
- [ ] Verificare la presenza di cluster nei dati (K>1):
    * Matrice di scatterplot con le variabili
    * Statistical method: Hopkins statistics
    * Visual method: VAT algorithm
- [ ] Commento che d'ora in avanti si faranno per ogni algoritmo, 3 diverse prove:
    - Tutte le variabili
    - Solo le variaibli diagonal e Bottom
    - Due variabili post PCA
- [ ] Calcolo della PCA da d a 2 variabili

3. Clustering

3.1. Applicazione delle Tecniche di Clustering non model-based

3.1.1. Clustering Gerarchico Agglomerativo

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [ ] Eseguire l'algoritmo
- [ ] Determinare K:
    * Direct method: elbow, siluette
    * Statistical method: GAP statistic
    * NbClust --> Calcola su diversi indici Tra cui quelli sopra
- [ ] Goodness dei risultati (cluster.stats() calcola diversi indici)
    * Intenal: silhouette width, Dunn index
    * External (solo se si ha la vera classe): adjusted rand index, meila variation index
- [ ] Commentare i risultati

3.1.2. Clustering Partizionale: K-means e K-medoids (PAM)

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [ ] Eseguire l'algoritmo
- [ ] Determinare K:
    * Direct method: elbow, siluette
    * Statistical method: GAP statistic
    * NbClust --> Calcola su diversi indici Tra cui quelli sopra
- [ ] Goodness dei risultati (cluster.stats() calcola diversi indici)
    * Intenal: silhouette width, Dunn index
    * External (solo se si ha la vera classe): adjusted rand index, meila variation index
- [ ] Commentare i risultati

3.1.3. Confronto tra clustering non Model-based

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [ ] Calcolo clValid
- [ ] Commento risultati ottenuti con clValid

3.2. Applicazione delle Tecniche di Clustering model-based

3.2.1. Clustering mixture of gaussian

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [ ] Eseguire l'algoritmo
- [ ] Determinare K: (Stesse tecniche?)
- [ ] Goodness dei risultati (Stesse tecniche?)
- [ ] Commentare i risultati

3.3. Validazione e Visualizzazione dei Risultati

- [ ] Commento di comparazione tra le diverse tecniche e tra il diverso numero di variabili usate.
- [ ] Confronto grafico 2D (usare PCA per il caso di tutte le variabili)
- [ ] Commento interpretativo dei risultati

4. Applicazione delle tecniche di mixture of regression

4.1. Mixture of regression senza variabili concomitanti

4.2. Mixture of regression con variabili concomitanti

4.3. Risultati

5. Conclusioni e Sviluppi Futuri










## OUTLINE


1. Introduzione

    Obiettivo del progetto:
    Applicare diverse tecniche di clustering al dataset banknote per identificare gruppi omogenei e confrontare i metodi.

    Contesto e motivazione:
    Riferimento agli argomenti trattati (clustering gerarchico, K-means/PAM, clustering model-based, validazione) e motivazione della scelta del dataset.

    Struttura del documento:
    Panoramica delle sezioni, con particolare attenzione alla validazione finale comparativa.

2. Descrizione del Dataset e Analisi Esplorativa

    Caratteristiche del dataset:
    Descrizione delle variabili (dimensione, tipologia, eventuali correlazioni) del dataset banknote.

    Analisi Esplorativa dei Dati (EDA):
    Statistiche descrittive e visualizzazioni (scatterplot, boxplot, ecc.) per capire la distribuzione dei dati.

    Preprocessing:
    Gestione dei dati mancanti o anomali, normalizzazione o scaling se necessario.

3. Applicazione delle Tecniche di Clustering
3.1 Clustering Gerarchico Agglomerativo

    Descrizione del metodo:
    Spiegazione della scelta del metodo, criteri di distanza e linkage.

    Implementazione in R:
    Codice e visualizzazione del dendrogramma.

3.2 Clustering Partizionale: K-means e K-medoids (PAM)

    Confronto tra K-means e PAM:
    Breve discussione su vantaggi, svantaggi e criteri per la scelta del numero ottimale di cluster (es. elbow method, silhouette analysis).

    Implementazione in R:
    Codice e visualizzazione dei risultati.

3.3 Clustering Model-Based

    Mixture of Gaussian e tecniche parsimoniose:
    Spiegazione dei modelli basati su distribuzioni gaussiane e, eventualmente, l'approccio parsimonioso o mixture of regressions.

    Implementazione in R:
    Utilizzo di pacchetti (ad es. mclust) e presentazione dei risultati.

4. Validazione e Visualizzazione dei Risultati

    Raccolta e presentazione dei risultati:
    Sintesi dei cluster ottenuti da ciascun metodo.

    Metriche di validazione:
    Calcolo e confronto di indici quali silhouette, Calinski-Harabasz, Dunn index, ecc., per valutare la bontà dei cluster.

    Visualizzazione con PCA:

        Obiettivo: Proiettare i dati in 2D per visualizzare la separazione tra i cluster ottenuti.

        Implementazione: Codice R per eseguire la PCA sul dataset originale (o sui risultati del clustering) e per creare plot in due dimensioni che evidenzino i cluster.

    Analisi comparativa:
    Discussione critica sui punti di forza e limiti di ciascun metodo, integrando le evidenze derivanti dalla visualizzazione PCA.

5. Conclusioni e Sviluppi Futuri

    Sintesi dei principali insight:
    Riassunto dei risultati e riflessioni sull'efficacia dei diversi approcci di clustering.

    Prospettive future:
    Suggerimenti per ulteriori approfondimenti o per l'applicazione di metodi aggiuntivi.

6. Appendici

    Codice Completo:
    Inclusione dei blocchi di codice R usati, commentati in dettaglio.

    Grafici e Output Supplementari:
    Visualizzazioni aggiuntive e risultati non discussi nel corpo principale.

    Bibliografia e Riferimenti:
    Elenco delle fonti e dei materiali del modulo utilizzati per l'analisi.
