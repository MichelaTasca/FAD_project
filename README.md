# FAD_project
# Analisi dei Dati e Predizione degli Outcome - Austin Animal Center

Questo progetto presenta un'analisi esplorativa e statistica approfondita (EDA) sui dati relativi agli esiti (outcome) degli animali del rifugio **Austin Animal Center**. L'obiettivo è comprendere quali fattori influenzino l'adozione e prevedere il destino degli animali ospitati tramite modelli di Machine Learning.

## 📌 Indice
1. [Acquisizione e Comprensione del Dataset](#1-acquisizione-e-comprensione-del-dataset)
2. [Pulizia e Pre-Processing](#2-pulizia-e-pre-processing)
3. [Analisi Esplorativa (EDA)](#3-analisi-esplorativa)
4. [Inferenza Statistica](#4-inferenza-statistica)
5. [Modellazione e Predizione](#5-modellazione-e-predizione)
6. [Tecnologie Utilizzate](#-tecnologie-utilizzate)

---

## 1. Acquisizione e Comprensione del Dataset
Il dataset è stato acquisito tramite `kagglehub` e contiene le registrazioni di oltre 78.000 animali. 
Gli attributi principali includono:
- **Dati anagrafici**: Specie, razza, colore, data di nascita, sesso e stato di sterilizzazione.
- **Dati di uscita**: Data dell'esito, tipologia di esito (adozione, trasferimento, eutanasia, ecc.) e sottotipologia.

**Domande di ricerca:**
- Vengono adottati più cani o gatti?
- L'età influenza la probabilità di adozione?
- Qual è l'impatto della sterilizzazione sull'esito finale?

## 2. Pulizia e Pre-Processing
Il dataset originale presentava diverse sfide trattate nel notebook:
- **Gestione Valori Mancanti**: Creazione di feature binarie (es. `has_name`) e imputazione di valori "Unknown" per sesso e sottotipologia.
- **Correzione Inconsistenze**: Eliminazione di colonne ridondanti e conversione delle date per calcolare l'età precisa al momento dell'uscita.
- **Feature Engineering**: 
    - Raggruppamento delle oltre 2.000 razze in 23 macro-aree basate su taglia e attitudine (es. Cani da guardia, Retriever, Razze Nordiche).
    - Consolidamento dei colori in 11 categorie dominanti.

## 3. Analisi Esplorativa
L'analisi rivela che:
- Circa il **43%** degli animali ha meno di un anno al momento dell'esito.
- I cani e i gatti rappresentano la stragrande maggioranza della popolazione, seguiti da pipistrelli e procioni (spesso associati a rischi di rabbia).

## 4. Inferenza Statistica
Vengono eseguiti test per validare le ipotesi di ricerca, analizzando le correlazioni tra:
- Specie vs Adozione
- Età vs Adozione
- Periodo temporale vs Adozione

## 5. Modellazione e Predizione
Il progetto include una sezione dedicata alla predizione tramite:
- **Regressione Logistica** per l'analisi statistica degli impatti.
- **Machine Learning**: Utilizzo di algoritmi di classificazione come **Decision Tree** e **K-Nearest Neighbors (KNN)**, ottimizzati tramite `GridSearchCV` per massimizzare l'accuratezza della predizione dell'outcome.

---

## Tecnologie Utilizzate
- **Linguaggio**: Python
- **Librerie Principali**:
  - Analisi dati: `pandas`, `numpy`
  - Visualizzazione: `matplotlib`, `seaborn`
  - Statistica: `scipy`, `statsmodels`
  - Machine Learning: `scikit-learn`

---
*Progetto realizzato per l'esame di Fondamenti di Analisi Dati (2025/26), prof. Antonino Furnari*
*Michela Tasca e Chiara Chessari*
