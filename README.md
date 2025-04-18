# master-ds-progetto-DA-SL

## TODO list:

### 1. Introduzione

Clustering:

Specificare che si procederà nell'applicare i seguenti algoritmi di clstering: gerarchico agglomerativo, kmeans, kmedoids, mixture of gaussian.
Ognuna di queste si proverà con: tutte le variabili del dataset, soltante diagonal e bottom, soltanto 2 dalla PCA.

Regression.

### 2. Descrizione del Dataset e Analisi Esplorativa

- [ ] Descrizione delle variabili (dimensione, tipologia, eventuali correlazioni) del dataset banknote.
- [ ] Analisi Esplorativa dei Dati (EDA)
- [ ] Preprocessing
- [x] Verificare la presenza di cluster nei dati (K>1):
    * Matrice di scatterplot con le variabili
    * Statistical method: Hopkins statistics
    * Visual method: VAT algorithm
- [x] Calcolo della PCA da d a 2 variabili
- [x] Commento che d'ora in avanti si faranno per ogni algoritmo, 3 diverse prove:
    - Tutte le variabili
    - Solo le variaibli diagonal e Bottom
    - Due variabili post PCA

### 3. Clustering

#### 3.1. Clustering Gerarchico Agglomerativo

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:


- [x] Eseguire l'algoritmo
- [x] Determinare K:
    * Direct method: elbow, siluette
    * Statistical method: GAP statistic
    * NbClust --> Calcola su diversi indici Tra cui quelli sopra
- [x] Goodness dei risultati (cluster.stats() calcola diversi indici)
    * Intenal: silhouette width, Dunn index
- [x] Commentare i risultati;

#### 3.2. Clustering Partizionale: K-means e K-medoids (PAM)

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [x] Determinare K:
    * Direct method: elbow, siluette
    * Statistical method: GAP statistic
    * NbClust --> Calcola su diversi indici Tra cui quelli sopra
- [x] Eseguire l'algoritmo
- [ ] Goodness dei risultati (cluster.stats() calcola diversi indici)
    * Intenal: silhouette width, Dunn index
- [ ] Commentare i risultati

##### 3.3. Confronto tra clustering non Model-based

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibli dopo PCA"]:

- [ ] Calcolo clValid
- [ ] Commento risultati ottenuti con clValid

#### 3.4. Clustering model-based: mixture of gaussian

For all: ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibili dopo PCA"]:

- [x] Eseguire l'algoritmo con Mclust (internamente cerca la versione parsimoniosa)
- [x] Determinare K: usare BIC e ICL
- [x] Commentare i risultati
- [x] Fare il tutto usando solo le variabili dopo PCA

#### 3.5. Validazione e Visualizzazione dei Risultati

- [ ] Commento di comparazione tra le diverse tecniche e tra il diverso numero di variabili usate.
- [ ] Confronto grafico 2D (usare PCA per il caso di tutte le variabili)
- [ ] Commento interpretativo dei risultati, vedere le caratteristiche dei diversi cluster trovati (es statistiche descrittive ecc)
- [x] External: adjusted rand index, meila variation index, Accuracy, Confusion matrix, ecc. Fare prima sul tutto il dataset e poi dividere il dataset e fare solo su test set:
      - Per l'intero dataset e per il train/test:
         - Per ogni tecnica di clustering
            - Per ogni ["Tutte le variabili", "variaibli diagonal e Bottom", "variaibili dopo PCA"]:
               Calcolare ciascuna di queste misure: [Adjusted Rand index, Meila, Accuracy, Recall, Specifity, Confusion Matrix, AUC]

### 5. Conclusioni e Sviluppi Futuri










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
