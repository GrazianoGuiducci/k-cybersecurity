# Quando la configurazione avvia strumenti e un'approvazione riprende il lavoro

*Due situazioni illustrative per usare K-Cybersecurity durante la progettazione di agenti e workflow. Il metodo è portabile; le funzioni di protezione dipendono dall'ambiente del ricevente.*

## 1. Un file di configurazione diventa un processo

Un assistente deve esaminare una modifica proposta in un repository. Il progetto include un file di configurazione che descrive server e strumenti aggiuntivi. Una procedura automatica potrebbe attivare questi strumenti **durante il caricamento dell'ambiente**, prima che l'assistente interpreti semanticamente il contenuto dei file.

La domanda di sicurezza riguarda quindi il passaggio effettivo da *configurazione letta* a *capacità eseguita*: chi decide di avviare lo strumento, da quale revisione proviene il file e quali privilegi sono disponibili in quel momento?

La competenza di sicurezza rende pertinenti l'owner del caricamento, le impostazioni di attivazione e i privilegi dell'host. La fonte può essere utile per comprendere il progetto senza che il proprio contenuto ottenga automaticamente l'autorità di avviare programmi.

Una configurazione rimasta invariata può inoltre interagire diversamente con un host aggiornato: sorgente, strumento, contesto e conseguenza hanno proprie coordinate temporali.

## 2. Un'approvazione sospesa riprende un effetto

Un agente propone un'operazione che richiede approvazione. Il controller sospende l'azione e ne conserva un identificatore per riprendere il lavoro.

Al momento della ripresa, il sistema deve poter conoscere **quale soggetto** sta approvando, **quale operazione** era sospesa e **a quale sessione, checkpoint e owner** appartiene la richiesta. La sola disponibilità di un identificatore, di un token o della stessa appartenenza a un progetto non garantisce tale legame.

La normalizzazione dei riferimenti e l'attribuzione dell'autorità hanno senso nel controller che riprende l'effetto. L'agente potrebbe aver formulato una proposta coerente e il sistema potrebbe comunque attribuire impropriamente il consenso: comportamento del modello, verifica dell'host e azione risultante restano fatti distinti.

## Quale apprendimento continua

Questi casi ampliano il punto di osservazione della sicurezza:

- **Prima dell'interpretazione:** un file o una risorsa può attivare strumenti mentre viene caricata
- **Nel momento dell'effetto:** sorgenti e deleghe possono cambiare indipendentemente
- **Dopo una sospensione:** la ripresa deve conservare il legame fra approvatore, incarico e azione
- **Nell'apprendimento:** la protezione esercitata dal controller e la scelta formulata dall'agente sono osservazioni con portate differenti

La pertinenza segue il lavoro effettivo. Un assistente impegnato a scrivere un riassunto non ha bisogno di trasformare ogni frase in una scansione di configurazioni; un sistema che avvia tool, esegue CI o riprende azioni sospese rende queste relazioni materiali.

Le osservazioni pubbliche che hanno reso visibili questi due tipi di passaggio includono gli advisory dei rispettivi manutentori [Anthropic/claude-code-action (20 maggio 2026)](https://github.com/anthropics/claude-code-action/security/advisories/GHSA-8q5r-mmjf-575q) e [n8n/Agent resume (30 settembre 2026)](https://github.com/n8n-io/n8n/security/advisories/GHSA-p3pg-xw4f-m72c). Descrivono prodotti e versioni specifiche; **nessun incidente o componente vulnerabile in MAIOS è implicato da questi esempi**.

Il [metodo generale](../docs/SECURITY_IN_OPERATION.md) porta questa discriminazione nelle competenze pertinenti e il [caso della fonte e della delega](fonte-delega-ed-effetto.md) mostra un'altra trasformazione utile.

---

# When configuration activates tools and approval resumes work — English

*Two illustrative cases for agent and workflow development. The method is portable; actual safeguards depend on the receiving environment.*

## 1. Configuration becomes execution

An assistant examines a proposed repository change. A project configuration describes extra tools or servers. The host might activate them **while loading the environment**, before the assistant has interpreted the file's content.

The useful question is when a configuration becomes an executable capability: which host chooses to start it, which revision supplied the configuration, and which privileges are available? The file can inform the project without acquiring authorization to launch programs merely by being read.

## 2. Suspended approval resumes an effect

An agent proposes an operation requiring approval. Its controller suspends the action and later receives a request to resume it.

The controller needs a valid relationship between **approving actor, suspended operation, session, checkpoint and authority owner**. A run identifier, token, or shared project membership is not by itself evidence of that relationship. Reference normalization and authorization belong at the actual point of resumption.

A model can make a reasonable proposal while the host incorrectly attributes approval. Keep the model's decision, the host's enforcement and the eventual effect separate.

## Learning that carries forward

Security may become relevant before interpretation, at the effect boundary, after resumption, and when observing the receiving agent's understanding. The actual work determines which distinction matters. This is situated operating knowledge, not an assertion that a monitor, tool sandbox or approval service has already been installed.

Maintainer advisories that motivated these examples: [Anthropic/claude-code-action, May 20, 2026](https://github.com/anthropics/claude-code-action/security/advisories/GHSA-8q5r-mmjf-575q) and [n8n Agent resume, September 30, 2026](https://github.com/n8n-io/n8n/security/advisories/GHSA-p3pg-xw4f-m72c). Their findings concern the named products, not a confirmed MAIOS vulnerability.

See [security during work](../docs/SECURITY_IN_OPERATION.md) and [source, delegation and effect](fonte-delega-ed-effetto.md).
