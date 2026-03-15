# ADR-XXX: Title

Date: YYYY-MM-DD  
Status: Proposed / Accepted / Rejected / Superseded

---

# Context

Describe the problem or architectural question.

Explain:

• what triggered this decision  
• what system is affected  
• what constraints exist  
• what goals we want to achieve  

Example:

The game requires navigation across multiple height levels.  
We must decide how world geometry will be represented.

---

# Decision

Describe the chosen solution.

Be clear and specific.

Example:

The world will be represented as a **grid-based map with discrete height levels**.

Each tile stores:

- surface type
- height level
- traversal flags

---

# Consequences

Explain the results of this decision.

## Positive

• easier navigation graph generation  
• simpler editor implementation  
• predictable movement rules  

## Negative

• less geometric freedom than mesh-based worlds  
• slopes require additional logic  

---

# Alternatives Considered

List other approaches and why they were rejected.

Example:

### NavMesh world

Rejected because:

• harder to integrate with tile-based editor  
• more complex height transitions  

### Continuous terrain

Rejected because:

• unnecessary complexity for a survivor-style game

---

# Notes

Optional extra information:

• links to related ADRs  
• diagrams  
• references