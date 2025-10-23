---
title: Legg til kunnskap i en assistent
weight: 3
meta:
  path: guides/add-knowledge-to-assistant
---
### Trinn 1: Forbered kunnskap i Space-et ditt
Velg én eller flere metoder under **Knowledge** (venstremeny):

- **Collections:** Last opp dokumenter, regneark og presentasjoner.
- **Web Pages:** Koble til nettsteder (grunnleggende crawl eller sitemap-crawl).
- **Integrations:** Koble til **SharePoint** / **Confluence** (må aktiveres av Admin først).

### Trinn 2: Koble kunnskap til assistenten
1. Åpne assistenten → **Edit**.
2. Klikk **Add Knowledge**.
3. Velg relevante kunnskapskilder fra Space-et ditt.
4. Lagre.

### Trinn 3: Test integrasjonen
- Still spørsmål som krever den opplastede kunnskapen.
- Kontroller at kildene refereres riktig.
- Juster kilder eller innstillinger ved behov.

#### Merknad om RAG
Intric bruker **RAG (Retrieval-Augmented Generation)** for å søke semantisk i kunnskapsbasen din.  
Bare de mest relevante tekstbitene sendes til modellen (ikke hele dokumenter); data lagres i en vektordatabase (**PGVector**) for raskt oppslag.
