# ⚡ n8n Multi-Branch Lead Routing & Data Orchestration System

An end-to-end automated lead processing pipeline built in **n8n** that integrates form intake, database logging, conditional filtering, multi-path email notifications, and stream merging.

![n8n Workflow Canvas](workflow-canvas.png)

---

## 🛠️ Architecture & Workflow Logic

1. **Intake Trigger (`On form submission`):** Captures incoming lead data parameters (e.g., Name, Email, Occupation).
2. **Database Logging (`Append or update row in sheet`):** Dynamically updates and appends records in **Google Sheets** for real-time record keeping.
3. **Conditional Filter (`Filter`):** Strips unqualified leads based on user parameters before running downstream operations.
4. **Dynamic Branching (`Switch`):** Splits lead execution paths into segmented streams (e.g., Engineer vs. Doctor leads).
5. **Targeted Messaging (`Gmail`):** Dispatches customized notification emails tailored to the lead segment.
6. **Stream Merging (`Merge`):** Re-joins execution branches into a single unified output stream.
7. **Post-Processing (`Gmail`):** Triggers final consolidated confirmation alerts.

---

## 🚀 How to Import & Use

1. Clone or download this repository.
2. In your n8n dashboard, click **Workflows** → **Import from File**.
3. Select `lead-routing-workflow.json`.
4. Connect your own credentials for **Google Sheets** and **Gmail**.
5. Activate the workflow!

---

## 🧰 Tech Stack
* **Orchestration:** n8n (Self-Hosted / Community)
* **Integrations:** Google Sheets API, Gmail API
* **Data Handling:** Webhooks, JSON Payload Mapping, Conditional Rules Engine
