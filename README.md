# Osservatorio Collaudolab — dati aperti sui robot tagliaerba

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21918355.svg)](https://doi.org/10.5281/zenodo.21918355)
[![Licenza: CC BY 4.0](https://img.shields.io/badge/licenza-CC%20BY%204.0-informational.svg)](https://creativecommons.org/licenses/by/4.0/deed.it)

Dati grezzi delle rilevazioni pubblicate su
**[collaudolab.com/osservatorio](https://www.collaudolab.com/osservatorio)**.

Ogni rilevazione è una misura sul catalogo di robot tagliaerba che seguiamo,
con **campione, metodo e data dichiarati**. Qui stanno i file; l'analisi che li
accompagna sta sul sito, linkata da ciascuna sezione.

## Licenza

I dati in `dati/` sono pubblicati con licenza
**[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.it)**: puoi
riusarli, rielaborarli e ridistribuirli, anche a fini commerciali, **citando
Collaudolab e linkando la pagina della rilevazione**.

Il testo delle rilevazioni sul sito non rientra nella licenza.

## Rilevazioni

### `dati/garanzie-robot-tagliaerba.csv`

Quanto durano davvero le garanzie dei robot tagliaerba venduti in Italia,
separando quello che i produttori **pubblicizzano** da quello che l'acquirente
ottiene **senza dover fare nulla**.

- **Pagina:** <https://www.collaudolab.com/osservatorio/garanzie-robot-tagliaerba>
- **Campione:** 136 modelli di 10 marche a catalogo
- **Rilevazione:** 13 agosto 2026
- **Righe:** 10, una per marca

| Colonna | Contenuto |
|---|---|
| `marca` | Marca del robot |
| `modelli_a_catalogo` | Quanti suoi modelli sono nel catalogo Collaudolab |
| `mesi_senza_condizioni` | Mesi coperti senza alcuna azione dell'acquirente. Mai sotto 24 |
| `mesi_pubblicizzati` | Massimo che il produttore pubblicizza |
| `scarto_mesi` | Differenza fra i due, cioè quanto della promessa è condizionato |
| `condizioni` | Cosa serve fare per ottenere il massimo pubblicizzato |
| `fonte` | Pagina del produttore da cui viene il dato |
| `verificato_il` | Data della lettura (ISO 8601) |

**Il risultato in una riga:** 8 marche su 10 non concedono un solo mese oltre i
24 previsti dalla legge italiana, e le coperture pubblicizzate fino a 6 anni
richiedono tutte una registrazione a termine o tagliandi di manutenzione a
pagamento.

## Metodo, in breve

- **Il pavimento è la legge.** In Italia ogni acquisto di un consumatore porta
  con sé 24 mesi di garanzia legale di conformità (Codice del Consumo, artt.
  128-135, riscritti dal D.Lgs. 170/2021), dovuti dal venditore e
  inderogabili. `mesi_senza_condizioni` non scende mai sotto quella soglia,
  qualunque cosa dichiari il produttore.
- **Sopra il pavimento contano solo le coperture incondizionate.** Un'estensione
  che richiede una registrazione entro un termine, un tagliando a pagamento o il
  passaggio da un centro autorizzato non è una copertura che l'acquirente ha: è
  una che potrebbe ottenere. La distinzione è l'oggetto della rilevazione.
- **Solo fonti del produttore.** Mai un rivenditore. La colonna `fonte` dice
  sempre da dove viene il dato, e `verificato_il` quando è stato letto.
- **Quello che non si può verificare resta dichiarato come tale.** Mammotion
  comunica "fino a 3 anni" senza pubblicare i termini: è trattato come
  condizionato, che è la lettura prudente, e la cosa è scritta sia qui sia in
  pagina.

## Come si aggiorna

I file **non si modificano a mano**. Sono generati dalla stessa sorgente che
disegna la tabella pubblicata sul sito, così il file scaricabile e la pagina che
lo racconta non possono raccontare due cose diverse.

Ogni riesecuzione di una rilevazione produce una versione nuova, pubblicata come
release. Le versioni precedenti restano: un dato osservato è un fatto datato, e
non si riscrive a posteriori.

## Come citare

> Collaudolab, «Le garanzie dei robot tagliaerba: quanto coprono davvero»,
> rilevazione agosto 2026,
> <https://www.collaudolab.com/osservatorio/garanzie-robot-tagliaerba>
> (DOI: 10.5281/zenodo.21918355)

Il file `CITATION.cff` in questo repository fa comparire il pulsante
**"Cite this repository"** in cima alla pagina GitHub, con la citazione già
formattata in BibTeX e APA.

### Quale dei due DOI

Zenodo ne conia due, e servono a cose diverse:

| DOI | Cosa identifica | Quando usarlo |
|---|---|---|
| [`10.5281/zenodo.21918355`](https://doi.org/10.5281/zenodo.21918355) | Il deposito nel suo insieme | **Quasi sempre.** Risolve all'edizione più recente, quindi una citazione resta valida quando la rilevazione viene rieseguita |
| [`10.5281/zenodo.21918356`](https://doi.org/10.5281/zenodo.21918356) | La sola versione `v2026.08.13` | Quando serve inchiodare l'analisi ai numeri di quel giorno, per esempio in un lavoro che li rielabora |

Nel dubbio, il primo.

## Contatti

Per domande sul metodo, segnalazioni di errori o riuso in un'elaborazione più
ampia: <https://www.collaudolab.com/contatti>

Le segnalazioni di errore sono benvenute come issue. Se un produttore ha
cambiato le proprie condizioni, il modo più rapido per farlo correggere è
aprire una issue con il link alla pagina aggiornata.
