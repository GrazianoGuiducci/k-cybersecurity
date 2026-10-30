# Bersaglio effettivo e destinatario delle operazioni

Due situazioni illustrative su riferimenti risolti e conversazioni condivise.
[English](#resolved-target-and-operation-recipient) · [Metodo](../docs/SECURITY_IN_OPERATION.md)

## Italiano

### Un percorso autorizzato raggiunge un altro repository

Un assistente lavora su un progetto autorizzato. Lo strumento ammette una
cartella del progetto, ma Git interpreta un riferimento contenuto nella
cartella e raggiunge un altro repository. L'autorizzazione sulla cartella
iniziale non chiarisce da sola il mandato sull'oggetto effettivamente aperto.

Il responsabile dell'integrazione riconosce il repository scelto dalla
risoluzione Git e il suo rapporto con l'incarico. Può così preservare un
worktree collegato legittimo oppure contenere un accesso estraneo al mandato.
La stessa domanda sul bersaglio effettivo riguarda una scrittura quando la
directory cambia attraverso un collegamento fra controllo e operazione.
Il mezzo protettivo segue il componente e la piattaforma che eseguono l'atto.

La conseguenza da osservare è quale repository o file viene raggiunto e
quali operazioni legittime rimangono possibili. Un confronto fra stringhe di
percorso o una dichiarazione del modello mostrano relazioni diverse da
un'operazione effettivamente confinata.

### Due client usano lo stesso identificatore di richiesta

Due persone aprono conversazioni distinte con un servizio. Ogni client
assegna alla prima richiesta l'identificatore `0`. Il servizio condivide una
sola istanza e correla le risposte con quel numero: la risposta alla prima
persona può arrivare alla seconda. Il documento restituito può essere
corretto e autentico, pur appartenendo a un'altra conversazione.

La competenza dell'integrazione riconosce la relazione client–sessione–richiesta
nel router e nello stato condiviso. La configurazione delle istanze e la
proprietà delle attività seguono l'API del servizio. Il riscontro comprende
più client e i destinatari realmente raggiunti; conserva anche l'accesso
legittimo alle attività che devono continuare fra sessioni autorizzate.

Il metodo del modello e il controllo del server restano distinti. Un agente
può comprendere correttamente il documento dopo che il servizio ha già
recapitato informazioni al destinatario sbagliato.

## Resolved target and operation recipient

### An authorized path reaches another repository

An assistant works on an authorized project. The tool accepts a project
folder, but Git interprets a reference inside it and reaches another
repository. Permission on the initial folder alone does not establish the
mandate for the object that is actually opened.

The integration's responsible component identifies the repository selected
by Git resolution and its relationship to the task. It can preserve a
legitimate linked worktree or contain access outside the mandate. The same
question concerns a write when a directory changes through a link between
validation and the operation. The protective mechanism follows the component
and platform that perform the action.

The observation concerns which repository or file is reached and which
legitimate operations remain available. Comparing path strings or reading a
model's declaration shows a different relation from an operation whose
boundary is exercised by the host.

### Two clients use the same request identifier

Two people open separate conversations with a service. Each client numbers
its first request `0`. A shared server instance correlates responses using
that number alone: one person's response can reach the other. The returned
document can be correct and authentic while belonging to another conversation.

The integration competence follows the client–session–request relationship
through routing and shared state. Instance construction and task ownership
follow the service API. Observation covers multiple clients and the actual
recipients, while preserving legitimate access to work that should continue
across authorized sessions.

The model's method and the server's control remain distinct. An agent can
understand a document correctly after the service has already delivered
information to the wrong recipient.

## Fonti primarie / Primary sources

- [MCP Git: gitdir e confine del repository](https://github.com/modelcontextprotocol/servers/security/advisories/GHSA-w766-5x43-whvw), 28 ottobre / October 2026.
- [MCP filesystem: directory padre e tempo della scrittura](https://github.com/modelcontextprotocol/servers/security/advisories/GHSA-53mr-w429-c597), 25 ottobre / October 2026.
- [MCP HTTP: istanze condivise e recapito fra client](https://github.com/modelcontextprotocol/typescript-sdk/security/advisories/GHSA-jm63-cq47-j5jp), 15 ottobre / October 2026.
- [MCP taskStore: attività e sessione creatrice](https://github.com/modelcontextprotocol/typescript-sdk/security/advisories/GHSA-22jm-h49p-29qw), 2 ottobre / October 2026.

Scenari illustrativi derivati da osservazioni dei manutentori: non sono test
eseguiti sul sistema del lettore o prove di capacità di un LLM. Versioni,
precondizioni e mitigazioni tecniche restano nelle fonti e nell'integrazione reale.

Illustrative scenarios derived from maintainer observations: they are not
executed tests of the reader's system or evidence of LLM capability. Versions,
preconditions, and technical mitigations belong to the sources and the actual integration.
