---
title: Sikkerhetsoversikt
weight: 2
meta:
  path: getting-started/security-overview
---
### Datelagring og datasuverenitet
- **All data lagres i Sverige** hos **GleSYS AB** (sertifisert etter ISO/IEC 27001).
- Mulighet til å bruke **egen sky** eller **lokal installasjon**.
- Full kontroll på **hvor data ligger** og **hvem som har tilgang**.

### Bruk av amerikanske modeller (valgfritt)
- Hvis du velger amerikanske modeller (f.eks. ChatGPT, Claude) sendes kun **begrenset, relevant tekst** via **RAG (Retrieval-Augmented Generation)** – **aldri hele dokumenter**.
- Data behandles da under vilkårene til modellleverandøren.
- Organisasjoner kan **begrense bruken** til **EU- eller norsk-svenske modeller**.

### Håndtering av persondata
- Intric baserer seg ikke på usikker «automatisk PII-filtrering». I stedet prioriteres **sikre standardinnstillinger**:
  - Data lagres i Sverige.
  - **Tillatt modell-liste** (administratorer kan begrense til EU-/svenske modeller).
  - **Isolerte Spaces** med tydelige regler og tilgangskontroll.
- Reduserer risiko selv om filtrering skulle svikte.

### Kryptering og plattformsikkerhet
- **Under transport:** TLS **1.2/1.3** for all trafikk (inkludert interne API-er).
- **I ro:** **AES-256**-kryptering for lagrede data.
- **Hemmeligheter:** API-nøkler **hashes med SHA-256**, aldri lagret i klartekst.
- **Konfidensiell databehandling (NVIDIA):** Støttes for Intric-hostede open source-modeller – data forblir kryptert **selv under prosessering**.

### Backup og gjenoppretting
- **Daglige fullstendige sikkerhetskopier** av instansen.
- Lagring separat hos GleSYS.
- **Bevaringstid: 14 dager** for kontinuitet og beskyttelse.

### Tilgangskontroll og autentisering
- **RBAC** på både **organisasjons-** og **Space-nivå**:
  - Organisasjon: **Admin / Creator / User**
  - Space: **Space Admin / Space Editor / Space Viewer**
- **SSO** via Microsoft **Entra ID** / **Active Directory**; **MFA** er som regel påkrevd.

### Informasjonssikkerhetsstyring
- Sikkerhetsrammeverk i tråd med **ISO/IEC 27001**.
- **Sikker utviklingslivssyklus (SDLC)**, adskilte **test-** og **produksjonsmiljøer**.
- **CTO** har det overordnede ansvaret for informasjonssikkerhet.
- **Regelmessige penetrasjonstester** og kontinuerlig overvåking.

### Logging, revisjon og transparens
- **Avansert logging** med konfigurerbar lagringstid (f.eks. **30 / 90 dager**).
- Full innsikt i **hva som sendes til modellene**, for maksimal sporbarhet.
- Administratorer styrer logginnstillingene.

### Juridisk og etterlevelse
- **Databehandleravtale (DPA)** basert på malen fra **Kommunesektorens organisasjon (KS)**.
- Sikrer **GDPR-etterlevelse** og tydelig ansvarsdeling.

### Retningslinjer for datalagring
- Administratorer kan sette **beholding per assistent**:
  - Automatisk sletting av meldinger etter en definert periode.
  - Konfigureres i assistentens **Edit**-visning.

### Anbefalte tiltak
- For sensitive data, bruk **EU-/svenske modeller** (f.eks. **Llama 3.3 SWE**, **Gemma 3 SWE**).
- Definer **sikkerhetsklassifiseringer** og håndhev dem med modell-tillatelseslister.
- Bruk **Spaces** for å isolere prosjekter, avdelinger og datadomener.
- Aktiver **relevant logging** for revisjon.
- **Informer brukerne** om forskjellene mellom EU- og amerikanske modellalternativ.
