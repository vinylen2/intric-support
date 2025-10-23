---
title: Sett sikkerhetsklassifisering
weight: 1
meta:
  path: guides/set-security-classification
---
### Trinn 1: Opprett en sikkerhetsklassifisering
1. Klikk **Admin** (oppe til høyre).  
2. Åpne **Security Settings**.  
3. Opprett klassifiseringsnivåer (f.eks. *Høy sikkerhetsklassifisering*, *Standard sikkerhetsklassifisering*).

### Trinn 2: Knytt AI-modeller til klassifiseringene
1. Gå til **Models** (venstremeny).  
2. Velg hvilke modeller som skal høre til hver klassifisering.  
   - Eksempel: *Høy sikkerhet* → kun nordiske/EU-modeller som **Llama 3.3 SWE**.  
3. Lagre innstillingene.

### Trinn 3: Tilordne til et Space
1. I hvert Space velger **Space Admin** riktig klassifisering.  
2. Brukere i Space-et kan kun velge modeller som er tillatt av den klassifiseringen.
