---
title: Slik legger du til kunnskap i et Space
weight: 1
meta:
  path: guides/add-knowledge-to-space
---
### Forutsetninger
For å legge til kunnskap i et Space må du ha rollen **Space Admin** eller **Space Editor**.  
**Space Viewers** kan bare bruke eksisterende assistenter og kan ikke koble til nye kunnskapskilder.

---

### Tre måter å legge til kunnskap på

#### 1. Collections
1. Gå til **Knowledge** i venstremenyen.  
2. Klikk **Collections**.  
3. Velg **Create Collection** og sett inn en tekst-embedding-modell.  
4. Last opp dokumenter, regneark eller skriv inn tekst direkte.  
5. Støttede formater: **PDF**, **Word (.docx)**, **Excel (.xlsx)**, **PowerPoint (.pptx)**, **CSV**, **Markdown (.md)** og **tekstfiler (.txt)**.  
6. Organiser filer i strukturerte mapper for enkel tilgang.

---

#### 2. Web Pages
1. Gå til **Knowledge → Web Pages**.  
2. Klikk **Connect Web Pages**.  
3. Lim inn URL-en til nettsiden du vil koble til.  
4. Velg crawl-type:  
   - **Basic Crawl:** Følger lenker fra startsiden (passer for sider uten sitemap).  
   - **Sitemap Crawl:** Bruker nettstedets `sitemap.xml` (raskere og mer kontrollert).  
5. Velg embedding-modell og hvor ofte innholdet skal oppdateres.  

**Tips:** Vær presis med URL-ene – koble til subdomener eller sider med relevant innhold i stedet for hele nettsteder.

---

#### 3. Integrasjoner
1. Integrasjonene **SharePoint** og **Confluence** må først aktiveres av en Admin.  
2. Som bruker går du til **Settings → My Account → My Integration → Connect**.  
3. Koble til innloggingsdetaljene dine for hver tjeneste.  
4. Naviger til **Knowledge → Integrations**.  
5. Klikk **Import Knowledge** og velg hvilken kunnskapsbase som skal kobles.

---

### Koble kunnskap til en assistent
Når kunnskapen er lagt til i Space-et:

1. Åpne assistenten du vil koble mot.  
2. Klikk **Edit** (øverst til høyre).  
3. Velg **Add Knowledge**.  
4. Velg hvilken kunnskapskilde fra Space-et assistenten skal bruke.

---

### Om RAG-teknologi
Intric bruker **RAG (Retrieval-Augmented Generation)** til å gjøre semantiske søk i kunnskapen din.

- Når et spørsmål stilles, finner systemet automatisk de mest relevante tekstutdragene.  
- Kun de relevante avsnittene sendes til språkmodellen – aldri hele dokumenter.  
- All kunnskap lagres i en **vektordatabase (PGVector)** for raskt og effektivt gjenfinning.

---

### Filstørrelser og begrensninger

| Type | Maks størrelse | Notater |
|------|----------------|---------|
| Tekstbaserte filer | **20 MB** | Støttet: PDF, Word, Excel, PowerPoint, CSV, Markdown, tekst |
| Lyd / video | **200 MB** | For transkribering og analyse |
| Bilder | **20 MB** | For referanse eller dokumentasjon |
