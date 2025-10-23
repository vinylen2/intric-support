---
title: Add Knowledge to an Assistant
weight: 3
meta:
  path: guides/add-knowledge-to-assistant
---
### Step 1: Prepare Knowledge in Your Space
Choose one or more methods under **Knowledge** (left menu):

- **Collections:** Upload documents/spreadsheets/presentations.
- **Web Pages:** Connect sites (basic crawl or sitemap crawl).
- **Integrations:** Connect **SharePoint** / **Confluence** (Admin must enable first).

### Step 2: Connect Knowledge to the Assistant
1. Open your assistant → **Edit**.
2. Click **Add Knowledge**.
3. Select the relevant knowledge sources from your Space.
4. Save.

### Step 3: Test the Integration
- Ask questions that require the uploaded knowledge.
- Check that sources are referenced correctly.
- Adjust sources or settings if needed.

#### Notes on RAG
Intric uses **RAG (Retrieval-Augmented Generation)** to semantically search your knowledge.  
Only the most relevant text chunks are sent to the model (not entire documents); data is stored in a vector DB (**PGVector**) for fast retrieval.
