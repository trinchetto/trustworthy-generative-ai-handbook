
### Expertise Support — “Amplify experts; don’t replace them”
**Role**  
Use AI to **assemble, contrast, and draft** around expert domains; final judgment stays with qualified humans.

**Appropriate uses**
- Draft **comparative analyses** (pros/cons, risks, cost bands) from provided materials.  
- Convert expert notes into **briefs, checklists, and decision trees**.  
- Generate **RAG-style citations** to ground statements in source docs.

**Design checklist**
- Require **source packs** (docs, datasets) as input; discourage unguided open-ended claims.  
- Insert **hold points** where a human must sign off before outputs move downstream.  
- Log **assumptions and unknowns**; surface confidence bands explicitly.

**Example applications**
- Legal: assemble case excerpts with **pin cites** for counsel review.  
- Clinical operations: generate patient education drafts with **links to authoritative leaflets** for clinician edit.  
- Engineering: produce architecture decision records (ADRs) with **linked references** to RFCs and tickets.

**Failure modes & mitigations**
- *Speculative claims* → enforce “no citation → no claim.”  
- *Over-confidence* → require **confidence statements** and a “What could be wrong?” box.  
- *Scope creep into decision-making* → clearly label AI artifacts as **advisory**.

**KPIs**
- Expert editing time ↓, citation completeness ↑, post‑review defect rate ↓.
