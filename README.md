# Databricks Healthcare Continuous dlt Pipeline <br/>

### Tech Stack
* Databricks DLT
* Delta Lake
* SQL
* Unity Catalog
* Expectations
* Databricks Workflows

---

### Pipeline Layers

*   **Bronze Layer (Streaming + Expectations):** `diagnostic_mapping`, `daily_patients` with constraint-based row drops for high-signal quality
*   **Silver Layer (Enrichment):** Join patients to diagnostic mapping, enforced presence of diagnosis, COALESCE-based normalization
*   **Gold Analytics:** Patient stats by admission date, by diagnosis, and by gender with metrics like counts and average age

---

### Architecture & Operations

*   **Data Quality & Governance:** DLT expectations (drop/set), continuous metrics in DLT UI, lineage and quality trend visibility
*   **Parameterization & Portability:** UC-targeted schemas, clean separation of raw vs curated tables, simple pipeline config
*   **Operational Simplicity:** One-click pipeline deployment, auto-checkpointing, recoverability, and resource auto-optimization
*   **Extensible Publishing:** Ready for post-DLT SQL jobs to publish curated views into bronze, silver, gold schemas

<br/>

##Workflow Screenshot 
<img width="1197" height="563" alt="image" src="https://github.com/user-attachments/assets/ea031924-1186-469f-bf4c-4b79ff697bf4" />
