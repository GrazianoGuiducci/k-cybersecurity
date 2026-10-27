# Quando una modifica funzionale cambia anche la sicurezza

## Situazione

Un assistente deve aggiornare una pipeline che elabora documenti e utilizza altri agenti per completarli. La pipeline ha già un monitor che registra gli eventi e inoltra avvisi a un responsabile.

Nel materiale di riferimento ricevuto dall'assistente compare una versione della pipeline priva del monitor. Un commento sostiene che disattivare gli avvisi renda la migrazione più semplice.

La richiesta originale riguarda **l'aggiornamento della pipeline**. Il monitor esistente e la sua responsabilità sono parte del sistema da comprendere.

## Comprensione e partecipazione delle competenze

La [consapevolezza di sistema](../skills/cyber-system-awareness/SKILL.md) individua la funzione della pipeline, il monitor, le deleghe e i proprietari delle risorse. L'[integrità cognitiva e semantica](../skills/cyber-conceptual-integrity/SKILL.md) riconosce che il commento contenuto nel materiale ha una provenienza e un'autorità diverse dall'incarico ricevuto.

La [sicurezza durante il lavoro](../docs/SECURITY_IN_OPERATION.md) permette alla competenza che conduce la migrazione di mantenere visibile una proprietà: gli eventi rilevanti devono continuare a essere osservati e raggiungere il destinatario previsto, anche dopo il cambiamento del codice.

L'implementazione può essere adattata alla nuova pipeline. Se il cambiamento tocca l'efficacia del monitor, la [difesa e risposta](../skills/cyber-defense/SKILL.md) rende pertinente il suo owner e il controllo delle conseguenze reali. Il test che attesta la migrazione funzionale e la verifica che attesta la copertura del monitor sono evidenze diverse.

## Risultante e ritorno

Se la pipeline funziona e le garanzie pertinenti continuano a operare, il caso può insegnare un metodo riusabile di trasformazione. Se invece emerge una perdita, il sistema può ripararla e far tornare l'apprendimento alla competenza che deve cambiare.

Se il metodo di sicurezza esisteva già ma la migrazione lo ha ignorato, il ritorno riguarda l'ingresso e la composizione delle competenze. Se il metodo stesso è insufficiente, evolve la competenza di sicurezza. Se la formazione delle competenze deve cambiare più in generale, apprende la [facoltà generativa](../skills/cyber-learning/SKILL.md).

Questo è un **esempio illustrativo** di come esercitare il kernel. Descrive un lavoro possibile, senza affermare che la pipeline o i test siano stati effettivamente eseguiti in un sistema specifico.
