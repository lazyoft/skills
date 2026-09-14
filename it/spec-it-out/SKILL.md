---
name: spec-it-out
description: Intervista l'utente su una richiesta, risolvi le decisioni aperte e scrivi una specifica con requisiti verificabili e task. Usa prima di costruire una funzionalità o per rivedere una specifica esistente.
---

# Spec it out

Intervista l'utente su una richiesta. Risolvi le decisioni che lascia implicite. Scrivi il risultato in un solo documento Markdown, in italiano.
L'utente legge la specifica completa. L'intervista comprende la divisione del lavoro in task e termina con la specifica, prima dell'implementazione.

## Leggi la richiesta

La richiesta può essere testo nella conversazione, un file o un collegamento a un documento.
Leggila prima di fare domande. Se non puoi accedere al materiale, spiega cosa manca e chiedi il testo o un collegamento accessibile.

## Cerca le risposte disponibili

Colma solo le lacune che non puoi risolvere dal materiale già letto. Cerca in questo ordine:

1. La richiesta stessa.
2. I documenti che cita, senza seguire ulteriormente i loro collegamenti.
3. Le istruzioni del progetto, il README e il codice pertinente.
4. Le altre fonti disponibili, limitando la ricerca al problema nominato nella richiesta.

Cita una fonte nella domanda solo quando serve a decidere. Metti le fonti complete nella specifica.

## Conduci l'intervista

Percorri l'albero delle decisioni fino a raggiungere una comprensione condivisa.

- Apri il turno con una domanda completa e comprensibile senza rileggere la conversazione.
- Fai una domanda per turno. Rimani sullo stesso punto finché è risolto.
- Fai sempre domande aperte, mai chiuse. Non chiedere risposte sì/no né una scelta limitata alle alternative presentate. Non usare widget di scelta.
- Una risposta aperta può far emergere nuove informazioni. Usale per esplorare nuovi scenari o riaprire bivi e decisioni già discussi.
- Presenta gli scenari non confermati come ipotesi: «Se succedesse X, che cosa servirebbe all’utente?». Non darli per abituali.
- Distingui fatti del dominio, ipotesi, esempi e decisioni. Quando una scelta dipende da un’ipotesi, rendila esplicita e approfondiscila con l’utente.
- Un esempio usato per ragionare diventa un requisito solo quando l’utente lo conferma.
- Esplora il bisogno senza presupporre una soluzione. La domanda deve lasciare possibile che non serva alcuna funzione o limitazione aggiuntiva.
- Ricava i criteri dagli obiettivi e dal contesto dell’utente. Chiarisci quali contano maggiormente quando entrano in conflitto.
- Quando una decisione ha più alternative sensate, confrontale sugli stessi criteri, mostrando vantaggi, svantaggi e informazioni mancanti.
- Non raccomandare un'alternativa. Lascia la scelta all'utente e aspetta la sua risposta.
- Se la motivazione della scelta non emerge già dalla risposta o dal contesto confermato, chiedila all’utente prima di considerare risolta la decisione. Conserva la motivazione e le conseguenze accettate senza attribuire all’utente ragioni che non ha espresso o confermato.
- Evita preamboli e resoconti del processo. Aggiungi ragionamenti solo quando aiutano a decidere.
- Usa esempi concreti del dominio. Parti dall'effetto per chi usa il risultato. Entra nei dettagli tecnici quando servono.
- Risolvi prima la decisione da cui dipendono le altre. Se una risposta chiude un ramo, elimina le domande diventate inutili.
- Rispondi con i fatti quando il codice contiene già la risposta. Usa l'intervista per le decisioni dell'utente.
- Se stai per assumere una scelta non risolta, chiedila. Una delega esplicita e circoscritta può risolvere il punto.
- Se una risposta richiede di osservare o provare qualcosa, individua la verifica necessaria. Usa il risultato per proseguire l’intervista, senza sostituirlo con una supposizione.
- Se l'utente vuole fare brainstorming, discuti con lui prima di scrivere la specifica.

Esamina questi aspetti quando riguardano la richiesta:

- Dove e come compare la funzionalità.
- Cosa riusare e quali nuove dipendenze considerare.
- Quale risultato serve e cosa viene escluso.
- Come l'utente riconosce che il lavoro è riuscito.
- Vincoli su dati, compatibilità, sicurezza, riservatezza e prestazioni.
- Cosa succede quando una dipendenza manca o fallisce.
- Quali segnalazioni servono durante l'uso, se pertinenti.
- Per un'interfaccia: riferimenti visivi, schermi previsti, interazioni e libertà lasciata all'implementatore.

## Concorda la divisione in task

Prima del riepilogo, chiedi come dividere il lavoro. La divisione decide cosa può procedere insieme e cosa deve aspettare.
Spiega le conseguenze delle possibili divisioni. L'utente sceglie o ti delega la divisione con limiti espliciti.

Un task consegna una parte utilizzabile del risultato e può essere integrato come modifica autonoma.
Preferisci pochi task. Dividi solo parti realmente separabili. Una divisione per soli strati tecnici lascia ogni task in attesa degli altri.
Prima di separare due task, valuta se persone diverse potrebbero completarli come modifiche indipendenti.
Considera i file condivisi. Una lunga catena di dipendenze può indicare un unico task suddiviso artificialmente.

## Riepiloga e scrivi

Quando le decisioni sono risolte, presentale in un elenco: una riga per decisione.
L'utente corregge ciò che non corrisponde alla richiesta. Scrivi dopo la conferma del riepilogo.

Leggi [il formato della specifica](reference/spec-format.md). Scrivi un documento completo con requisiti, verifiche e task nello stesso file.
Non attribuire all'utente deduzioni che non ha espresso o confermato. Indica nella prosa le scelte lasciate all'implementatore e i loro limiti.

Rileggi prima di consegnare:

- Ogni requisito ha una verifica concreta e compare in almeno un task.
- Ogni task copre requisiti esistenti e nomina solo dipendenze reali.
- Gli identificatori sono univoci e i collegamenti fra requisiti e task sono corretti.
- Le fonti sono presenti. Le scelte della specifica corrispondono alla conversazione.

Presenta il documento completo e il suo percorso. La prova strutturale non dimostra che le decisioni siano giuste: l'utente deve poterle leggere e discutere.
