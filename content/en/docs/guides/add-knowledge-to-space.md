---
title: How to Add Knowledge to a Space
weight: 1
meta:
  path: guides/add-knowledge-to-space
---
### Prerequisites
To add knowledge to a Space, you need to have the **Space Admin** or **Space Editor** role.  
**Space Viewers** can only use existing assistants and cannot connect new knowledge sources.

---

### Three Ways to Add Knowledge

#### 1. Collections
1. Go to **Knowledge** in the left menu.  
2. Click **Collections**.  
3. Select **Create Collection** and choose a text embedding model.  
4. Upload documents, spreadsheets, or type text directly.  
5. Supported formats: **PDF**, **Word (.docx)**, **Excel (.xlsx)**, **PowerPoint (.pptx)**, **CSV**, **Markdown (.md)**, and **text files (.txt)**.  
6. Organize files into structured folders for easy access.

---

#### 2. Web Pages
1. Go to **Knowledge → Web Pages**.  
2. Click **Connect Web Pages**.  
3. Paste the URL of the website you want to connect.  
4. Choose a crawl type:  
   - **Basic Crawl:** Follows links from the starting page (good for sites without a sitemap).  
   - **Sitemap Crawl:** Uses the site’s `sitemap.xml` (faster and more controlled).  
5. Select an embedding model and update frequency.  

**Tip:** Be specific with your URLs — connect subdomains or pages containing relevant information rather than entire websites.

---

#### 3. Integrations
1. **SharePoint** and **Confluence** integrations must first be enabled by an Admin.  
2. As a user, go to **Settings → My Account → My Integration → Connect**.  
3. Connect your access credentials for each service.  
4. Navigate to **Knowledge → Integrations**.  
5. Click **Import Knowledge** and choose which knowledge base to connect.

---

### Connecting Knowledge to an Assistant
After adding knowledge to your Space:

1. Open the assistant you want to connect the knowledge to.  
2. Click **Edit** (upper-right corner).  
3. Select **Add Knowledge**.  
4. Choose which knowledge source from your Space the assistant should use.

---

### About RAG Technology
Intric uses **RAG (Retrieval-Augmented Generation)** to perform semantic searches across your connected knowledge.

- When a question is asked, the system automatically finds the most relevant text segments.  
- Only those relevant excerpts are sent to the language model — never entire documents.  
- All knowledge is stored in a **vector database (PGVector)** for fast and efficient retrieval.

---

### File Sizes and Limitations

| Type | Max Size | Notes |
|------|-----------|-------|
| Text-based files | **20 MB** | Supported: PDF, Word, Excel, PowerPoint, CSV, Markdown, text |
| Audio / Video | **200 MB** | For transcription and analysis |
| Images | **20 MB** | For reference or documentation |
