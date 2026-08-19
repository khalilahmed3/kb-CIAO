# KB Ciao! — Manuale Operativo

Knowledge base del sistema di cassa **Ciao!** (Salmoiraghi & Viganò), convertita dal manuale operativo Word in Markdown navigabile e ricercabile.

## Struttura

```
kb-ciao/
├── docs/
│   ├── index.md                 ← home page della KB
│   ├── 01-sistema-di-cassa.../
│   │   ├── index.md             ← contenuto della sezione
│   │   └── img/                 ← screenshot della sezione
│   ├── 02-operazioni-di-apertura.../
│   └── ... (18 sezioni totali)
├── mkdocs.yml                   ← configurazione sito/navigazione
├── requirements.txt
└── .github/workflows/deploy.yml ← pubblica automaticamente su GitHub Pages
```

## Uso con VS Code (anteprima locale)

1. Installa Python (3.9+) se non presente.
2. Apri il terminale integrato di VS Code nella cartella del repo e installa MkDocs:
   ```bash
   pip install -r requirements.txt
   ```
3. Avvia il server di anteprima live:
   ```bash
   mkdocs serve
   ```
   Apri `http://127.0.0.1:8000` nel browser: la pagina si aggiorna automaticamente a ogni salvataggio.
4. Per modificare un contenuto, apri direttamente il file `.md` della sezione in `docs/` — nessun bisogno di Word. Consigliata l'estensione **Markdown All in One** per l'editing e l'estensione **markdownlint** per la coerenza dello stile.

Se preferisci non installare nulla, i file `.md` sono comunque leggibili nativamente con l'anteprima integrata di VS Code (`Ctrl+Shift+V` / `Cmd+Shift+V`), o direttamente su GitHub.

## Pubblicazione online (GitHub Pages)

Il workflow incluso in `.github/workflows/deploy.yml` builda e pubblica automaticamente il sito su GitHub Pages a ogni push su `main`. Basta:

1. Creare il repository su GitHub e fare push di questa cartella.
2. In **Settings → Pages**, impostare come sorgente il branch `gh-pages` (creato automaticamente dal workflow al primo run).

In alternativa, pubblicazione manuale da locale:
```bash
mkdocs gh-deploy
```

## Contribuire

- Ogni sezione del manuale è un file `docs/NN-nome-sezione/index.md`.
- Le immagini di ciascuna sezione sono in `img/` accanto al file, con path relativi (`./img/nomefile.png`).
- Per proporre una correzione o aggiungere una procedura: crea un branch, modifica il `.md`, apri una Pull Request. La cronologia Git tiene traccia di tutte le versioni, eliminando la necessità di file tipo "manuale_v2_copy.docx".
- Alcuni artefatti minori derivanti dalla conversione automatica dal Word originale (didascalie generiche delle immagini, spaziature) possono essere rifiniti progressivamente via PR.

## Origine

Contenuto convertito dal manuale operativo Word originale (`Manuale_operativo_ciao_.docx`). Le 18 sezioni ricalcano fedelmente l'indice del documento sorgente.
