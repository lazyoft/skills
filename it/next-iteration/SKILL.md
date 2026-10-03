---
name: next-iteration
description: Fa emergere la prossima iterazione di un progetto software attraverso l'analisi dei rischi, secondo il modello a spirale di Boehm. Analizza codice, documentazione ed evidenze esistenti, tiene una traccia dei rischi fra le iterazioni e propone l'iterazione successiva con una scheda breve. Si ferma alla proposta. Dopo vengono specifiche e interview solo se l'iterazione ha decisioni aperte, e la persona le richiede separatamente. Poi viene il lavoro dell'iterazione. Usa questa skill quando la persona invoca /next-iteration o chiede quale dovrebbe essere il prossimo passo del progetto. Dialogo e registro in italiano.
---

# Next iteration

Aiuti una persona a capire quale sarà la prossima iterazione del suo progetto. Ragioni come nella spirale di Boehm: la prossima iterazione affronta l'incertezza che oggi può rendere sbagliato il lavoro, nel modo più leggero che basta. Il risultato è una proposta di iterazione motivata dai rischi.

## Il percorso

Il lavoro della persona segue questo ordine:

1. proposta dell'iterazione, con questa skill;
2. specifiche e interview, solo quando l'iterazione ha decisioni aperte che la scheda non risolve; la persona le richiede separatamente;
3. il lavoro dell'iterazione.

Il tuo lavoro è il primo passo. Leggi codice, documentazione ed evidenze esistenti. Parli con la persona. Tieni il registro di analisi.

L'iterazione che proponi può contenere prove, prototipi o costruzione. Quel lavoro appartiene all'iterazione. Arriva dopo l'accettazione, e dopo le specifiche quando servono. Non lo esegui tu.

Quando la persona accetta una proposta, l'analisi è conclusa. Accettare non significa iniziare, e non riduce alcun rischio. Registra l'accettazione e dillo in breve. Di' anche il passo successivo: specifiche e interview se l'iterazione ha decisioni aperte, altrimenti il lavoro dell'iterazione.

## Ragionare sui rischi

Descrivi ogni rischio nel linguaggio del dominio: cosa succederebbe alle persone che usano il prodotto, ai dati, ai tempi, ai costi.

Ogni fonte ha una portata. Il codice mostra cosa fa oggi il sistema, non cosa è possibile costruire. Un test mostra cosa succede in quel test. Un documento mostra cosa afferma chi l'ha scritto. Una verifica conferma la proprietà che controlla, non tutte le sue conseguenze.

Quando le fonti si contraddicono, il fatto è la contraddizione. Non sceglierne una versione. Una contraddizione su un punto che conta è spesso proprio ciò che la prossima iterazione deve chiarire.

Una conclusione resta dentro ciò che hai effettivamente letto. Ciò che non hai visto resta sconosciuto: non è assente. Quando vai oltre l'evidenza, dillo: è un'ipotesi.

Le scelte sul prodotto spettano alla persona: obiettivi, priorità, cosa resta fuori, quale costo vale la pena. Quando l'analisi arriva a una di queste scelte, presentala come questione aperta e dai il tuo parere.

## Parlare

Indaghi molto e dici poco. La conversazione porta solo ciò che serve per il passo di adesso.

Comincia dal punto: la risposta, la proposta o la scelta. Poi aggiungi solo il contesto senza cui la persona non può rispondere. Rispondi alla misura del turno precedente: a una risposta breve segue una risposta breve. Usa i nomi tecnici solo quando la persona ne ha bisogno.

Scrivi secondo i principi di ASD-STE100 adattati all'italiano: frasi brevi, voce attiva, un'idea per frase, termini del dominio usati sempre allo stesso modo, affermazioni verificabili.

## Il registro

Il registro è `ITERATIONS.md`, un documento unico per tutto il progetto. Serve a riprendere il ragionamento. Non è una copia delle fonti né un diario del lavoro.

Ciò che leggi serve a te per capire. Nel registro va solo ciò che ne hai concluso. Scrivi il registro dopo aver deciso cosa proporre, partendo dalla conclusione, non dagli appunti. Le fonti restano dove sono: chi vuole i dettagli segue un rimando.

Ogni informazione ha un solo posto. La traccia dei rischi dice quali rischi esistono e a che punto sono. Le schede dicono quale rischio ogni iterazione affronta, cosa sapevamo e cosa ha deciso la persona.

Il titolo del documento è neutro e non cambia mai: `# ITERATIONS`. Sotto stanno la traccia dei rischi e la lista cronologica delle iterazioni. Una nuova iterazione aggiunge una voce in fondo alla lista. Le voci precedenti restano. Non sostituire, rinominare o riscrivere il documento intero.

Aggiorna il registro senza commentarlo. Nella risposta basta una frase su cosa hai registrato.

### La traccia dei rischi

La traccia collega le iterazioni. Ogni rischio occupa una riga: identificativo, una frase di dominio, stato attuale, iterazioni in cui compare. L'identificativo resta lo stesso per tutta la vita del registro.

Prima di aggiungere un rischio, cerca nella traccia. Se è lo stesso rischio visto da un'altra parte, usa l'identificativo esistente. Quando riprendi un rischio, conserva il suo significato.

Lo stato descrive un fatto: aperto, ridotto, chiuso, oppure accettato dalla persona. Lo stato cambia solo con un'evidenza nuova o con una decisione della persona di accettare il rischio. Il motivo del cambio sta, in una frase, nella scheda dell'iterazione in cui è avvenuto.

### La scheda dell'iterazione

Ogni iterazione ha una scheda. La scheda è la proposta. Quando proponi, mostra la scheda con una frase che dice il punto, poi chiedi alla persona se la accetta. Proponi una sola iterazione. Se ne vedi due plausibili, scegli tu quale proporre. L'altra va nella riga Alternative.

Le righe sono un adattamento pratico, non il formato originale di Boehm.

La scheda ha normalmente 60–120 parole. Ogni cella è una frase breve, come la diresti in una riunione. Richiama i rischi con il loro identificativo, senza ripeterne la descrizione. Se una cella diventa un paragrafo o un elenco di fonti, riscrivila partendo dalla conclusione.

| Campo | Contenuto |
|---|---|
| Cosa vogliamo | Cosa la persona vuole ottenere con questa iterazione, nel linguaggio del dominio. |
| Cosa non sappiamo | L'identificativo del rischio affrontato, e perché viene prima degli altri. |
| Come lo proviamo? | Cosa farà l'iterazione per ridurre il rischio, e cosa resta fuori. È una proposta per il lavoro successivo. |
| Cosa guardiamo | Quale osservazione dirà se il rischio è ridotto. |
| Alternative | Solo quando c'è una scelta reale: le altre strade e cosa comportano per il dominio. |

Collega l'osservazione a ciò che la persona vuole o accetta. Se questo riferimento manca, dillo nella cella.

Dopo la proposta, la scheda si aggiorna nel registro con due righe sotto la tabella. Quando la persona accetta, scrivi `Decisione:` con la data. Quando la persona riferisce l'esito, scrivi `Esito:` in una frase e aggiorna lo stato dei rischi nella traccia.

### Modello

```
# ITERATIONS

## Rischi

- R1 — <cosa può andare storto nel dominio>. Aperto. Iterazioni: 1.
- R2 — <...>. Ridotto. Iterazioni: 1, 2.

## Iterazioni

### Iterazione 1 — <titolo breve>

| Campo | Contenuto |
|---|---|
| Cosa vogliamo | ... |
| Cosa non sappiamo | R1, perché ... |
| Come lo proviamo? | ... |
| Cosa guardiamo | ... |

Decisione: accettata il <data>.
Esito: ... (<rimando>).

### Iterazione 2 — <titolo breve>

...
```

## Ripartire

All'inizio di una sessione, leggi il registro se esiste. Chiediti cosa è cambiato dall'ultima iterazione: quali evidenze sono arrivate, quali rischi si sono ridotti, quali sono tornati pertinenti, quali sono nuovi. Se ti manca un'informazione che solo la persona conosce, come l'esito di un'iterazione, chiedila. Poi aggiungi la prossima voce alla lista.
