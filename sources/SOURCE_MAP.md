# Fonti e sapere raggiungibile

## Sorgente della direzione

Il [manifesto](../MANIFESTO.md) conserva la formulazione originale di Graziano
Guiducci del 27 ottobre 2026 e la visione che orienta il kernel. Il nucleo
è formato nel programma MAIOS e nel campo di competenze D-ND. Il sapere
essenziale per operare è nei corpi locali, senza dipendenze da accessi privati.

## Risorse tecniche e concettuali

Consultate durante la prima formazione, 27 ottobre 2026. Le sorgenti mobili
vanno raggiunte nella versione pertinente quando un loro dettaglio cambia
una decisione o un'implementazione.

| Fonte primaria | Sapere che può cambiare il lavoro |
| --- | --- |
| [Cloudflare security-audit-skill](https://github.com/cloudflare/security-audit-skill) | Ricerca e comprensione di violazioni dei confini di fiducia; verifica legata alla sorgente e al risultato |
| [Claude Security, guida ufficiale](https://academy.claude.com/tutorials/getting-started-with-claude-security) | Esempio di servizio che collega repository, comprensione delle minacce, rilievi e proposte di intervento |
| [Anthropic security review](https://github.com/anthropics/claude-code-security-review) | Esempio di revisione AI delle modifiche e integrazione nel lavoro di sviluppo |
| [Gitleaks](https://github.com/gitleaks/gitleaks) e [Betterleaks](https://github.com/betterleaks/betterleaks) | Individuazione di segreti in file e storia Git; scansione e uso attivo delle credenziali sono operazioni differenti |
| [Google OSV-Scanner](https://github.com/google/osv-scanner) | Conoscenza di vulnerabilità nelle dipendenze e modalità di consultazione dei dati |
| [Trivy](https://github.com/aquasecurity/trivy) | Analisi di immagini, dipendenze, segreti e configurazioni |
| [OWASP Agentic Top 10](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) | Rischi delle applicazioni agentiche, inclusa la contaminazione di memoria e contesto |
| [OWASP Agent Control Standard](https://genai.owasp.org/resource/agent-control-standard-acs/) | Relazione fra piattaforme agentiche, osservabilità e controlli durante l'esecuzione |
| [NIST AI 600-1](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) | Integrità dell'informazione, confabulazione e relazione umano-AI |

Sono risorse e possibilità di apprendimento. Nessuna singola implementazione
esaurisce il campo del kernel. L'acquisizione del saper fare comprende
copertura, condizioni, effetti e modo in cui il risultato cambia la situazione.

## Risoluzione del bersaglio e identità del destinatario

Fonti primarie rilette il 30 ottobre 2026, con eventi del 2, 15, 25 e 28 ottobre.
L'[esempio bilingue](../examples/bersaglio-e-destinatario.md) collega i casi al metodo:

- [MCP Git: riferimento gitdir e repository effettivo](https://github.com/modelcontextprotocol/servers/security/advisories/GHSA-w766-5x43-whvw).
- [MCP filesystem: directory padre fra controllo e operazione](https://github.com/modelcontextprotocol/servers/security/advisories/GHSA-53mr-w429-c597).
- [MCP HTTP: istanze condivise e recapito fra client](https://github.com/modelcontextprotocol/typescript-sdk/security/advisories/GHSA-jm63-cq47-j5jp).
- [MCP taskStore: attività e sessione creatrice](https://github.com/modelcontextprotocol/typescript-sdk/security/advisories/GHSA-22jm-h49p-29qw).

Le condizioni del maintainer appartengono ai package citati. L'applicabilità
in un ricevente si comprende da versione, configurazione e mezzo effettivi.

## Altri kernel e nuovi apporti

La formazione riusa relazioni funzionali già sviluppate nei kernel MAIOS:
ingresso situato, sapere operativo, composizione, continuità, incarnazione ed
evoluzione. Il contenuto di un altro dominio resta alla sua sorgente.

Una fonte o un'implementazione nuova può cambiare la domanda e il metodo.
L'apprendimento raggiunge la competenza che dovrà usare quella differenza.
La mappa rimane aperta a risorse e relazioni ancora non rappresentate.
