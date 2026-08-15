# Inclusione ed Esclusione Finanziaria Digitale in Italia (indagine IACOFI 2023)

Progetto di gruppo per il corso di Data Science Lab. Il lavoro analizza i dati
del questionario IACOFI 2023 per studiare l'inclusione/esclusione finanziaria
digitale della popolazione adulta italiana, articolato in quattro research
question (RQ), ciascuna curata da un membro/sottogruppo del team.

## Research question e file di riferimento

| RQ | Tema | Codice | Report finale |
|----|------|--------|-----------------|
| RQ1a | Accesso a Internet (chi resta escluso, per età/istruzione/...) | `RQ1_internet_access/RQ1_Internet_Access_Analysis.ipynb` | `report_finale/report_RQ1_accesso_adozione.pdf` |
| RQ1b | Adozione (QP8) e frequenza d'uso (QP9) di servizi finanziari online tra chi ha Internet | `RQ1_adoption_qp8_qp9/qp8+qp9.ipynb` | `report_finale/report_RQ1_accesso_adozione.pdf` |
| RQ3 | Esposizione a frodi digitali | `RQ3_fraud_exposure/RQ3.ipynb` | `report_finale/report_RQ3_frodi_digitali.pdf` |
| RQ4 | Consapevolezza dei rischi di sicurezza digitale | `RQ4_security_awareness/RQ4_security_awareness.ipynb` | `report_finale/report_RQ4_security_awareness.docx` |

RQ1a e RQ1b sono state riunite in un unico report accademico finale
(`report_RQ1_accesso_adozione.pdf`).

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
    ├── report_RQ1_accesso_adozione.pdf
    ├── report_RQ3_frodi_digitali.pdf
    └── report_RQ4_security_awareness.docx
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
