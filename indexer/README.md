# Indicizzatore

Agente Rust da eseguire sui file server Linux con accesso in sola lettura alle cartelle locali. Una scansione completa per area aggiorna il catalogo centrale. Le scansioni incomplete conservano l'ultimo indice valido. Un worker separato dalla scansione estrae le miniature incorporate nei CDR e renderizza la prima pagina dei PDF nuovi o modificati.
