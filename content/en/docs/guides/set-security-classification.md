---
title: Set Security Classification
weight: 1
meta:
  path: guides/set-security-classification
---
### Step 1: Create a Security Classification
1. Click **Admin** (top-right).
2. Open **Security Settings**.
3. Create classification levels (e.g., *High Security Classification*, *Standard Security Classification*).

### Step 2: Map AI Models
1. Go to **Models** (left menu).
2. Assign which models belong to each classification.
   - Example: *High Security* → only Swedish/EU models such as **Llama 3.3 SWE**.
3. Save your settings.

### Step 3: Assign to a Space
1. In each Space, the **Space Admin** selects the appropriate classification.
2. Users in that Space can only pick models allowed by that classification.
