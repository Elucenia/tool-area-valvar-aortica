<!-- ELUCENIA technical documentation · area-valvar-aortica · it · no clinical/professional/rights approval -->

# Area valvolare aortica (equazione di continuità)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/area-valvar-aortica)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Diametro del tratto di efflusso ventricolare sinistro

`dvsve`

cm · intervallo: 1,2–3,5

### Integrale velocità-tempo (VTI) del tratto di efflusso ventricolare sinistro

`vtivsve`

cm · intervallo: 5–50

### Integrale velocità-tempo della valvola aortica (VTI)

`vtiao`

cm · intervallo: 10–250

### Velocità aortica massima (facoltativa)

`vmax`

m/s · facoltativo · intervallo: 0,5–8

### Superficie corporea (facoltativa)

`sc`

m² · facoltativo · intervallo: 0,8–3

## Edizione del metodo

EACVI/ASE 2017: continuità mediante VTI; DVI; Bernoulli semplificato 4 v²

## Formula documentata

Area del tratto di efflusso VS = π × (diametro ÷ 2)²

Area valvolare aortica = area del tratto di efflusso VS × VTI del tratto di efflusso VS ÷ VTI aortico

Indice adimensionale (DVI) = VTI del tratto di efflusso VS ÷ VTI aortico

Gradiente massimo (Bernoulli semplificato) = 4 × V²

## Limiti e popolazione

La valutazione della stenosi aortica nelle raccomandazioni EACVI/ASE 2017 è integrata: gradiente, flusso, frazione di eiezione e qualità della valutazione del tratto di efflusso ventricolare devono essere considerati insieme. Le situazioni di basso flusso o basso gradiente richiedono la valutazione specifica prevista dal documento. I valori calcolati da soli non riproducono l’algoritmo completo.

## Riferimenti

- [Baumgartner H et al. Recommendations on the echocardiographic assessment of aortic valve stenosis (EACVI/ASE). J Am Soc Echocardiogr, 2017.](https://doi.org/10.1016/j.echo.2017.02.009)

- [Otto CM et al. 2020 ACC/AHA Guideline for the Management of Patients With Valvular Heart Disease. Circulation, 2021.](https://doi.org/10.1161/CIR.0000000000000923)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Stenosi aortica importante per area

| Dettagli del risultato | |
| --- | --- |
| Area del TSVI | 3,14 cm² |
| Indice adimensionale (DVI) | 0,25 |
| Gradiente massimo (4V²) | 64 mmHg |


### 2

Stenosi aortica moderata per area

| Dettagli del risultato | |
| --- | --- |
| Area del TSVI | 3,80 cm² |
| Indice adimensionale (DVI) | 0,37 |

