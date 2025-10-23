---
title: "Lägg till kunskap i en assistent"
weight: 3
---

### Steg 1: Förbered kunskap i ditt Space
Välj en eller flera metoder under **Kunskap** (vänstermenyn):

- **Samlingar:** Ladda upp dokument/kalkylblad/presentationer.
- **Webbsidor:** Koppla webbplatser (grundläggande crawl eller sitemap-crawl).
- **Integrationer:** Koppla **SharePoint** / **Confluence** (måste först aktiveras av admin).

### Steg 2: Koppla kunskapen till assistenten
1. Öppna assistenten → **Edit**.
2. Klicka på **Add Knowledge**.
3. Välj relevanta kunskapskällor från ditt Space.
4. Spara.

### Steg 3: Testa kopplingen
- Ställ frågor som kräver den uppladdade kunskapen.
- Kontrollera att källor citeras korrekt.
- Justera källor eller inställningar vid behov.

#### Om RAG
Intric använder **RAG (Retrieval-Augmented Generation)** för att göra semantiska sökningar i din kunskap.  
Endast de mest relevanta textstyckena skickas till modellen (inte hela dokument); data lagras i en vektordatabas (**PGVector**) för snabb åtkomst.
