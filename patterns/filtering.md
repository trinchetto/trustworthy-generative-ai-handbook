
### Filtering — “Smaller, truer, and traceable”
**Why it’s safe**  
Outputs are a **subset or summary of known inputs**; you can verify them. Filtering augments human analysis without inventing facts.

**Patterns that preserve traceability**
- **Simple Filter** — *“Keep/remove Y from X.”*  
- **Semantic Filter** — *“Explain what you’re removing and why; then return the filtered set with original IDs.”*  
- **Summarize & Cite** — *“Summarize key points; after each sentence, cite record IDs or exact quotations.”*

**Design checklist**
- Always preserve **identifiers** (row IDs, line numbers, message URLs).  
- Separate **explanation** (what was removed/kept and rationale) from **result set**.  
- Bound **recall vs. precision** (e.g., “Prefer precision for legal risk”).  
- Include **coverage metrics** (e.g., % of items retained, categories removed).

**Example applications**
- Customer feedback triage with **themes + supporting review IDs**.  
- Security log reduction with **retained event IDs and rule rationales**.  
- Policy extraction: **sections + line numbers** from lengthy docs.

**Failure modes & mitigations**
- *Over-aggressive filtering* → run with two thresholds (strict/loose) and compare deltas.  
- *Loss of traceability* → reject outputs missing IDs; require a second pass to reattach.  
- *Hidden bias in semantic filters* → expose criteria text back to users for audit.

**KPIs**
- Analyst review time ↓, verification time ↓, % outputs with valid citations ↑.
