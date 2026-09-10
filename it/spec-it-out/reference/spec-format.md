# Formato della specifica

La specifica è un solo documento Markdown. L'utente legge tutte le sezioni. Non ci sono appendici riservate agli agenti.

## Scrittura

Applica questi principi di ASD-STE100, adattati all'italiano:

1. Un'idea per frase. Usa frasi brevi e separa le istruzioni con il punto.
2. Usa la voce attiva. Scrivi «L'app mostra il file mancante».
3. Usa l'imperativo per le verifiche. Scrivi «Apri il progetto e controlla le immagini», senza ripetere «il verificatore».
4. Descrivi comportamenti osservabili. Usa quantità note o concordate, senza inventare valori per rendere una frase misurabile.
5. Elimina aggettivi come «robusto» e «critico» quando non spiegano un comportamento.

Usa la stessa parola per lo stesso concetto. Spiega i termini tecnici necessari alla decisione.
Punta a venti parole per istruzione e venticinque per descrizione. Conserva le condizioni che cambiano il significato.
Il dizionario dello standard è materiale di riferimento, non un motivo per bloccare la specifica.

## Sezioni

Usa queste sezioni, nell'ordine del modello sotto. Il problema descrive cosa non funziona oggi.
Il risultato descrive ciò che sarà possibile. Le esclusioni conservano ciò che avete deciso di lasciare fuori.
L'approccio spiega come le parti si collegano. Usa un diagramma quando rende il percorso più comprensibile.

Ogni requisito ha un blocco `R<n>`: comportamento e motivo, seguiti da `Check:` con una verifica concreta.
Per le decisioni che incidono sul risultato, conserva nella prosa del requisito le ragioni della scelta e le conseguenze accettate.
Indica chi ha deciso o quale delega è stata esercitata.
Ogni task ha un blocco `T<n>` con `Ask:`, `Covers:` e `Depends:`.

- `Ask:` dice cosa costruire.
- `Covers:` nomina i requisiti del task. Il task eredita il loro testo e le loro verifiche, senza reinterpretarli.
- `Depends:` indica i task che devono essere completati prima. `Depends: none` indica assenza di dipendenze.

La dipendenza si scrive sul task che aspetta. `Depends: T1` nel task T2 significa che T2 aspetta T1.
Ogni requisito deve essere coperto. Usa identificatori univoci e mantienili stabili nelle revisioni.
Un task integra una parte utilizzabile. Preferisci pochi task e separa solo modifiche realmente indipendenti.

Non aggiungere una versione del formato, un glossario, un'appendice tecnica o una sezione di domande aperte.
Risolvi le decisioni nell'intervista. Registra le deleghe e i loro limiti nella prosa del requisito pertinente.
Un criterio di verifica descrive una prova da svolgere. Costruire uno strumento permanente per quella prova resta una scelta da discutere entro la delega.

Se avete valutato e scartato ipotesi o alternative, raccoglile dopo le fonti nell’appendice «Ipotesi valutate e scartate».
Per ciascuna, indica cosa avete valutato e perché l’avete scartata.

## Modello

```markdown
# Titolo

## Problema
Cosa non funziona oggi.

## Risultato
Cosa sarà possibile quando il lavoro è completo.

## Esclusioni
Cosa abbiamo deciso di lasciare fuori.

## Approccio
Come le parti si collegano.

## Requisiti

### R1: Titolo del requisito
Cosa deve essere vero e perché.
Check: Come verificare il comportamento.

## Task

### T1: Titolo del task
Ask: Cosa costruire.
Covers: R1
Depends: none

## Fonti
- Materiale della richiesta e riferimenti consultati.
```
