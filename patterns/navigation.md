
### Navigation — “Take me to the truth, don’t generate it”
**Why it’s lower-risk**  
Navigation leverages **existing, validated systems** (databases, dashboards, EMRs, CRMs) and has the model **guide** users to where information lives instead of fabricating answers. If guidance is wrong, users see it’s missing and harm is limited; if text is fabricated, harm can be high.

**Core patterns**
- **Direct Navigation Pattern** — *“Tell me where I can find X. Here are the available locations and what each contains.”*  
- **Navigate Instead Pattern** — *“Whenever I ask about X, don’t answer — point me to the most likely location.”*

**Design checklist**
- Enumerate navigable **locations** (screen IDs, endpoints, table names) and describe what each contains.  
- Return **one best guess + alternatives**, with short rationales.  
- Include **access-awareness** (don’t route to data the user shouldn’t see).  
- Prefer **deep links** or precise click-paths over prose.

**Example applications**
- Healthcare apps: route to **Appointments → Upcoming** rather than inventing dates.  
- Finance tools: route to **Accounts → Statements (YYYY‑MM)** instead of synthesizing balances.  
- DevOps portals: route to **Service X → Runbooks** for incident playbooks.

**Failure modes & mitigations**
- *Wrong screen suggested* → present top‑3 candidates, include “Why” and a quick **“Not here → try next”** control.  
- *Sensitive area routing* → enforce policy checks before returning a location hint.  
- *Ambiguous user intent* → ask for one clarifying attribute (e.g., date range) then re-route.

**KPIs**
- Task time-to-complete ↓, mis-navigation rate ↓, successful deep-link open rate ↑.
