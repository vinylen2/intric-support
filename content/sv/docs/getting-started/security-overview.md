---
title: "Säkerhetsöversikt"
weight: 2
---

### Datolagring och plats
- **All data lagras i Sverige** hos **GleSYS AB** (certifierade enligt ISO/IEC 27001).
- Möjlighet att använda **egen molnmiljö** eller **on-premises** installation.
- Full kontroll över **dataplacering** och **åtkomst**.

### Användning av amerikanska modeller (valfritt)
- Om du väljer amerikanska modeller (t.ex. ChatGPT, Claude) skickas endast **begränsade, relevanta textutdrag** via **RAG (Retrieval-Augmented Generation)** – **aldrig hela dokument**.
- Data behandlas därefter enligt modellleverantörens villkor.
- Organisationer kan **begränsa användningen** till enbart **EU-/svenska modeller**.

### Hantering av personuppgifter
- Ingen opålitlig ”automatisk PII-filtrering”. Intric fokuserar istället på **säkra grundinställningar**:
  - Datalagring i Sverige.
  - **Tillåtelselista för modeller** (administratörer kan låsa till EU-/svenska modeller).
  - **Isolerade Spaces** med tydliga regler och åtkomstkontroll.
- Minskar risken även om filtreringstekniker skulle fallera.

### Kryptering och plattformsäkerhet
- **Under överföring:** TLS **1.2/1.3** för all trafik (även interna API:er).
- **I vila:** **AES-256**-kryptering för lagrad data.
- **Hemligheter:** API-nycklar **hashas med SHA-256** och lagras aldrig i klartext.
- **Confidential Computing (NVIDIA):** Stöds för Intric-hostade open-source-modeller – data förblir krypterad **även under bearbetning**.

### Backup och återställning
- **Dagliga fullständiga säkerhetskopior** av instansen.
- Kopiorna lagras separat hos GleSYS.
- **Retention: 14 dagar** för kontinuitet och skydd.

### Åtkomstkontroll och autentisering
- **RBAC** både på **organisationsnivå** och **Space-nivå**:
  - Organisation: **Admin / Creator / User**
  - Space: **Space Admin / Space Editor / Space Viewer**
- **SSO** via Microsoft **Entra ID** / **Active Directory**; **MFA** används ofta som krav.

### Informationssäkerhetsarbete
- Säkerhetsramverk i linje med **ISO/IEC 27001**.
- **Säker utvecklingsprocess (SDLC)**, separata **test-** och **produktionsmiljöer**.
- **CTO** har det övergripande ansvaret för informationssäkerheten.
- **Regelbundna penetrationstester** och kontinuerlig övervakning.

### Loggning, spårbarhet och transparens
- **Avancerad loggning** med konfigurerbar lagringstid (t.ex. **30 / 90 dagar**).
- Full insyn i **vad som skickas till modellerna** för maximal spårbarhet.
- Administratörer styr loggningsinställningarna.

### Juridik och regelefterlevnad
- **Personuppgiftsbiträdesavtal (PUB-avtal)** enligt **SKR:s mall** (Sveriges Kommuner och Regioner).
- Säkerställer **GDPR-efterlevnad** och tydliga ansvarsförhållanden.

### Policys för datalagring
- Administratörer kan ange **lagringstid per assistent**:
  - Automatisk borttagning av meddelanden efter vald tidsperiod.
  - Styrs i assistentens vy **Edit**.

### Rekommenderade arbetssätt
- Använd **EU-/svenska modeller** (t.ex. **Llama 3.3 SWE**, **Gemma 3 SWE**) för känsliga data.
- Definiera **säkerhetsklassning** och applicera den via modellernas tillåtelselista.
- Utnyttja **Spaces** för att isolera projekt/avdelningar och datadomäner.
- Aktivera **relevant loggning** för spårbarhet.
- **Utbilda användare** om skillnaderna mellan EU- och USA-baserade modeller.
