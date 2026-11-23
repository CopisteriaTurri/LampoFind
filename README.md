# LampoFind

LampoFind è un progetto self-hosted per cercare e aprire rapidamente file di rete da Windows e Linux. L'obiettivo è trovare un file per nome o percorso, riconoscerlo da una miniatura e aprire l'originale sulla condivisione SMB.

## Struttura

| Componente | Tecnologia prevista | Compito |
| --- | --- | --- |
| [server/](server/) | Django e SQLite | API autenticata, catalogo, gruppi e permessi per area, archivio delle anteprime. |
| [indexer/](indexer/) | Rust | Scansione periodica delle cartelle locali dei file server e generazione delle anteprime CDR e PDF. |
| [desktop/](desktop/) | Tauri | Ricerca per nome e percorso, anteprime e apertura degli originali su Windows e Linux. |

Ogni indicizzatore legge le cartelle montate in sola lettura e invia metadati e anteprime al server centrale. Il client ricerca attraverso l'API e usa la condivisione SMB per aprire gli originali con le credenziali della postazione.

Il repository contiene lo scheletro iniziale. L'indicizzazione, l'API e il client sono ancora da implementare.

## Licenza

LampoFind è distribuito secondo i termini della GNU Affero General Public License versione 3 o, a scelta del destinatario, qualsiasi versione successiva (`AGPL-3.0-or-later`). Il testo completo è in [LICENSE](LICENSE).
