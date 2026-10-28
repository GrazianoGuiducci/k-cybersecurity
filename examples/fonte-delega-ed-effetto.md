# Una fonte valida e una delega che cambia — esempio di sicurezza durante l'azione

*Esempio illustrativo e adattabile: descrive un metodo, non un incidente né un test svolto nel sistema del lettore.*

## Situazione

Un gruppo chiede a un assistente di aggiornare un piccolo flusso di elaborazione. Il lavoro usa un documento con istruzioni sui dati da trasformare; l'incarico dell'assistente deriva dalla persona o dal servizio che governa il progetto. Un secondo agente effettua parte della trasformazione e un monitor registra gli eventi.

Il documento ha una versione identificabile. La delega all'assistente ha un proprio owner e può cambiare indipendentemente dal documento.

## Primo movimento — il documento cambia

L'assistente legge la fonte, prepara la trasformazione e delega una parte del lavoro. Mentre il secondo agente opera, il contenuto del documento viene aggiornato.

Una verifica compiuta **prima** della delega descrive correttamente il documento di allora. Se il risultato viene applicato dopo l'aggiornamento, quel controllo iniziale potrebbe essere insufficiente per l'effetto corrente.

Quando l'identità della fonte è materialmente necessaria, la competenza comprende come legare la trasformazione alla revisione effettivamente accettata dall'owner **nel punto di applicazione**. Se la revisione cambia prima dell'effetto, il lavoro può essere ricomposto dalla fonte aggiornata. Se il cambiamento arriva dopo un commit già concluso, costituisce un evento successivo.

Un semplice confronto seguito da una scrittura separata può ancora lasciare una finestra temporale. Il ricevente sceglie i mezzi pertinenti al proprio ambiente per conservare la relazione fra verifica e applicazione: per esempio versionamento condizionale o transazioni quando realmente disponibili.

## Secondo movimento — il documento resta identico, la delega cambia

Questa volta il documento e la sua impronta restano uguali, ma l'owner revoca l'autorizzazione ad applicare la trasformazione durante il lavoro.

La fonte può rimanere **valida come informazione**. Il diritto di produrre l'effetto appartiene invece alla delega corrente e alla sua autorità effettiva. Se l'azione dipende da quella delega, la competenza deve poter raggiungere l'owner pertinente al momento dell'effetto, secondo il contratto tecnico del sistema.

Una modifica di permessi relativa a un progetto differente può essere irrilevante: sospendere tutto per ogni cambiamento amministrativo perderebbe lavoro legittimo. Un'etichetta `internal_operator` contenuta nel documento resta una dichiarazione della fonte, non una concessione di privilegi.

## Terzo movimento — che cosa dimostra il monitor

Il monitor può registrare correttamente il completamento di una trasformazione compiuta con dati ormai superati o con autorizzazione revocata. L'integrità del registro attesta determinate proprietà della **registrazione**, e non stabilisce da sola che l'operazione fosse autorizzata o corretta.

Il sistema mantiene distinguibili la proposta dell'agente, l'effetto applicato dal controller, la conferma dell'audit e l'eventuale recupero. Se l'effetto è avvenuto e la conferma del monitor rimane pendente, il seguito parte da tale condizione, evitando di ripetere alla cieca l'effetto già compiuto.

Separare monitor e componente delegato può preservare eventi anche quando cambia il codice del worker. La forza di questa separazione dipende da permessi, processi, configurazione e altri meccanismi **effettivamente esercitati** nel ricevente.

## Quarto movimento — che cosa ha capito l'agente

Un controller può negare un'azione non autorizzata anche quando l'agente l'aveva proposta. È un successo del controllo tecnico con una **proposta agente impropria**, non una dimostrazione che il modello abbia riconosciuto autonomamente la perdita.

Per imparare sul ricevente si può osservare, in un caso nuovo, quali informazioni ha scelto di acquisire, quale azione ha proposto, quali informazioni il controller aveva realmente e quale effetto si è verificato. Anche il blocco improprio di lavoro benigno è una conseguenza da comprendere.

Quando due spiegazioni producono la stessa traccia ordinaria, quella sola traccia può non identificarle. Una seconda osservazione pertinente o una condizione differente può separarle; un intervento deliberato e una rilettura dello stesso registro hanno fonti di prova distinte.

## Che cosa può continuare come competenza

- **Consapevolezza di sistema:** riconoscere quali proprietà della fonte, della delega, del monitor e dei processi possono cambiare indipendentemente
- **Integrità cognitiva:** distinguere documento, istruzione incorporata, autorizzazione e conclusioni della propria osservazione
- **Difesa:** conservare le garanzie durante modifiche e deleghe, attribuire audit, effetto e recupero ai loro owner
- **Formazione:** far ritornare la differenza nella competenza che opererà su un caso successivo

La [guida del metodo di sicurezza](../docs/SECURITY_IN_OPERATION.md) e le [competenze](../COMPETENCES.md) rendono raggiungibile questo sapere. Ogni incarnazione deve comprendere i propri mezzi e il mandato realmente affidato. Questo esempio non dichiara che K-Cybersecurity installi transazioni, monitor, difese automatiche o un controller specifico.

---

# When a valid source and a changing delegation meet — English

*Illustrative, adaptable example; it is neither a security-incident report nor a test of the reader's environment.*

A team asks an assistant to update a data-processing workflow. The source document has a revision, while the authority to apply the change belongs to a separate owner. Another agent performs part of the task and a monitor records events.

**The source changes during delegation.** A check performed before the worker ran describes the earlier source. If the change is applied after the document changed, the receiver needs a relation between the accepted revision and the actual effect. A read followed by an unrelated write may still leave a race; use a suitable owner-supported conditional update or transaction where available. A change after a completed commit belongs to a later event.

**The authority changes without changing the source.** The document is still informative, but the permission to act may have been revoked. The receiver must distinguish source freshness from current authority for the exact effect. An unrelated administrative change need not interrupt legitimate work, and an `internal_operator` label inside the document is not an authorization.

**The monitor produces a valid record.** A faithful audit entry does not, by itself, establish that the recorded action was justified. Keep the agent's proposal, the host's applied effect, the audit acknowledgement and any recovery separate. Monitoring reliability depends on the actual process, permissions and event path.

**The host blocks a bad proposal.** Host enforcement succeeded, but the agent may still have made a bad decision. To understand the receiver's capability, observe what it chose to learn, what it proposed, and what the host actually permitted, including benign work it unnecessarily paused. Two implementations can yield the same ordinary trace and diverge under another relevant condition; a counterfactual intervention is different from re-reading the same evidence.

This knowledge becomes useful in system awareness, conceptual integrity, defense and learning. The [security-in-operation method](../docs/SECURITY_IN_OPERATION.md) is available to the receiver; a real deployment must supply and verify its own source owner, permissions, controller and monitor.
