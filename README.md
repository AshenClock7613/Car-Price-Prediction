# Car-Price-Prediction

Questo repository contiene un'analisi di machine learning volta a predire il prezzo di vendita delle automobili. Utilizzando il dataset [Car Price Prediction da Kaggle](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data), il progetto esplora diverse tecniche di preprocessing dei dati, addestra e ottimizza due modelli di regressione (RandomForest e Kernel Ridge) e ne valuta le performance.

## 📝 Descrizione del Progetto

L'obiettivo principale è sviluppare un modello di regressione accurato per stimare il prezzo delle auto basandosi su un'ampia gamma di caratteristiche, come marca, dimensioni, potenza del motore e consumi.

Il notebook allegato (`PrML.ipynb`) documenta l'intero processo, dall'analisi esplorativa dei dati (EDA) e pulizia, fino alla valutazione finale dei modelli, includendo anche un'analisi con PCA per la riduzione della dimensionalità.

## 📊 Workflow del Progetto

Il progetto è strutturato nelle seguenti fasi:

1.  **Caricamento e Pulizia dei Dati**:
    *   Importazione del dataset `CarPrice_Assignment.csv` con pandas.
    *   Correzione di errori di battitura e standardizzazione dei nomi dei marchi nella colonna `CarName`.
    *   Conversione di colonne testuali (es. `doornumber`) in formati numerici.

2.  **Analisi Esplorativa dei Dati (EDA)**:
    *   Visualizzazione della distribuzione della variabile target (`price`) per comprenderne le caratteristiche.
    *   Analisi della frequenza dei marchi automobilistici per identificare le categorie con pochi campioni.

3.  **Feature Engineering e Preprocessing**:
    *   Raggruppamento dei marchi meno frequenti in una categoria unica "Other" per migliorare la generalizzazione del modello.
    *   Codifica delle variabili categoriche (es. `fueltype`, `carbody`) tramite `OrdinalEncoder`.
    *   Standardizzazione delle feature numeriche con `StandardScaler` per normalizzarle.

4.  **Addestramento e Ottimizzazione dei Modelli**:
    *   Suddivisione del dataset in set di addestramento e di test.
    *   Implementazione e confronto di due modelli di regressione:
        *   **RandomForestRegressor**: Un modello d'insieme potente, ottimo per catturare relazioni complesse.
        *   **KernelRidge**: Un modello che utilizza il "kernel trick" per gestire relazioni non lineari.
    *   Utilizzo di **GridSearchCV** per trovare i migliori iperparametri per entrambi i modelli e ottimizzarne le performance.

5.  **Analisi con PCA**:
    *   Applicazione dell'Analisi delle Componenti Principali (PCA) per ridurre la dimensionalità e visualizzare i dati in 2D.
    *   Valutazione delle performance dei modelli sui dati trasformati con PCA.

## 📈 Risultati

I modelli sono stati valutati utilizzando le metriche R² Score e Mean Squared Error (MSE). I risultati finali mostrano un'ottima capacità predittiva, con il modello **Kernel Ridge** che, dopo l'ottimizzazione, ha ottenuto performance leggermente superiori.

Le visualizzazioni finali, che includono le curve di predizione sui dati di test, confermano la bontà dell'adattamento dei modelli.

## 🚀 Come Eseguire il Progetto

Per replicare questa analisi, segui questi passaggi:

1.  Clona il repository:
    ```bash
    git clone https://github.com/AshenClock7613/Car-Price-Prediction.git
    ```

2.  Installa le dipendenze necessarie. È consigliato utilizzare un ambiente virtuale.
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn jupyter
    ```

3.  Scarica il dataset da [Kaggle](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data) e inseriscilo nella cartella principale del progetto.

4.  Apri ed esegui il notebook `PrML.ipynb` con Jupyter.
