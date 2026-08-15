# Digital Financial Inclusion and Fraud Exposure in Italy

Progetto di gruppo per il corso di Data Science Lab. Il lavoro analizza i dati
del questionario IACOFI 2023 per studiare l'inclusione/esclusione finanziaria
digitale della popolazione adulta italiana, seguendo il percorso concettuale:
**accesso → adozione/uso → esposizione a frodi → protezione tramite
consapevolezza della sicurezza**.

**Autori:** Davide Cavallo, Lorenzo Anteghini, Nicola Mereghetti, Andrei Covali.

**Report finale:** [`report_finale/report_finale.pdf`](report_finale/report_finale.pdf)

## Research question e codice di riferimento

| RQ | Tema | Notebook |
|----|------|----------|
| RQ1a | Accesso a Internet (chi resta escluso, per età/istruzione/...) | `RQ1_internet_access/RQ1_Internet_Access_Analysis.ipynb` |
| RQ1b | Adozione (QP8) e frequenza d'uso (QP9) di servizi finanziari online tra chi ha Internet | `RQ1_adoption_qp8_qp9/qp8+qp9.ipynb` |
| RQ2 | Attività digitale ed esposizione a frodi finanziarie riportate | `RQ3_fraud_exposure/RQ3.ipynb` |
| RQ3 | Ruolo protettivo della consapevolezza sulla sicurezza digitale | `RQ4_security_awareness/RQ4_security_awareness.ipynb` |

> Nota: i numeri delle RQ nel report finale (RQ1a, RQ1b, RQ2, RQ3) non
> corrispondono 1-a-1 ai nomi delle cartelle di codice (`RQ3_fraud_exposure`,
> `RQ4_security_awareness`), che riflettono invece l'organizzazione di lavoro
> originaria del team. Il contenuto analitico è lo stesso: `RQ3_fraud_exposure`
> corrisponde a RQ2 del report (frodi), `RQ4_security_awareness` corrisponde
> a RQ3 del report (consapevolezza).

Tutte le analisi confluiscono in un unico report finale
(`report_finale/report_finale.pdf`), che integra i quattro filoni in un
framework unico di inclusione finanziaria digitale.

## Struttura della repository

```
.
├── data/                         # dataset grezzo e codebook (input comune a tutte le RQ)
│   ├── Database_ENG.dta
│   └── Data-description-2023.pdf
├── RQ1_internet_access/
│   └── RQ1_Internet_Access_Analysis.ipynb
├── RQ1_adoption_qp8_qp9/
│   └── qp8+qp9.ipynb
├── RQ3_fraud_exposure/
│   └── RQ3.ipynb
├── RQ4_security_awareness/
│   └── RQ4_security_awareness.ipynb
└── report_finale/
    └── report_finale.pdf
```

## Dati

Il dataset comune a tutte le analisi è `data/Database_ENG.dta` (indagine IACOFI
2023), descritto in `data/Data-description-2023.pdf`. Ogni notebook lo carica
con `pandas.read_stata` e costruisce da lì le variabili necessarie alla
propria RQ.

> **Nota:** i notebook sono stati sviluppati originariamente su Google Colab
> con il dataset su Google Drive (`drive.mount(...)`, path del tipo
> `/content/drive/MyDrive/DSLAB_PROJECT/...`). Per eseguirli in locale o su
> Jupyter, basta rimuovere/commentare la cella di mount di Drive e far
> puntare il path del dataset a `../data/Database_ENG.dta`.

## Requisiti

```
numpy
pandas
scipy
patsy
statsmodels
matplotlib
seaborn
pyreadstat
openpyxl
jupyter
```

Installazione:
```bash
python -m pip install numpy pandas scipy patsy statsmodels matplotlib seaborn pyreadstat openpyxl jupyter
```
