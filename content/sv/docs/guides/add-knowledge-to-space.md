---
title: "Så lägger du till kunskap i ett Space"
weight: 1
---

### Förutsättningar
För att lägga till kunskap i ett Space behöver du rollen **Space Admin** eller **Space Editor**.  
**Space Viewers** kan bara använda befintliga assistenter och kan inte koppla nya kunskapskällor.

---

### Tre sätt att lägga till kunskap

#### 1. Samlingar
1. Gå till **Kunskap** i vänstermenyn.  
2. Klicka på **Collections**.  
3. Välj **Create Collection** och välj en text-embeddingmodell.  
4. Ladda upp dokument, kalkylblad eller skriv in text direkt.  
5. Stödda format: **PDF**, **Word (.docx)**, **Excel (.xlsx)**, **PowerPoint (.pptx)**, **CSV**, **Markdown (.md)** och **textfiler (.txt)**.  
6. Organisera filer i strukturerade mappar för enkel åtkomst.

---

#### 2. Webbsidor
1. Gå till **Knowledge → Web Pages**.  
2. Klicka på **Connect Web Pages**.  
3. Klistra in URL:en till webbplatsen du vill koppla.  
4. Välj vilken typ av crawl som ska användas:  
   - **Basic Crawl:** Följer länkar från startsidan (bra för sajter utan sitemap).  
   - **Sitemap Crawl:** Använder sajtens `sitemap.xml` (snabbare och mer kontrollerat).  
5. Välj embeddingmodell och uppdateringsfrekvens.  

**Tips:** Var specifik med dina URL:er – koppla hellre subdomäner eller sidor med relevant information än hela webbplatser.

---

#### 3. Integrationer
1. Integrationerna **SharePoint** och **Confluence** måste först aktiveras av en admin.  
2. Gå som användare till **Settings → My Account → My Integration → Connect**.  
3. Koppla dina åtkomstuppgifter för respektive tjänst.  
4. Navigera till **Knowledge → Integrations**.  
5. Klicka på **Import Knowledge** och välj vilken kunskapsbas som ska kopplas.

---

### Koppla kunskap till en assistent
När du lagt till kunskap i ditt Space:

1. Öppna assistenten som ska använda kunskapen.  
2. Klicka på **Edit** (uppe till höger).  
3. Välj **Add Knowledge**.  
4. Ange vilken kunskapskälla från ditt Space assistenten ska använda.

---

### Om RAG-teknik
Intric använder **RAG (Retrieval-Augmented Generation)** för att göra semantiska sökningar i dina anslutna kunskapskällor.

- När en fråga ställs letar systemet automatiskt fram de mest relevanta textavsnitten.  
- Endast dessa relevanta utdrag skickas till språkmodellen – aldrig hela dokument.  
- All kunskap lagras i en **vektordatabas (PGVector)** för snabb och effektiv hämtning.

---

### Filstorlekar och begränsningar

| Typ | Maxstorlek | Kommentar |
|------|-----------|-----------|
| Textbaserade filer | **20 MB** | Stöder: PDF, Word, Excel, PowerPoint, CSV, Markdown, text |
| Ljud / Video | **200 MB** | För transkribering och analys |
| Bilder | **20 MB** | För referenser eller dokumentation |
