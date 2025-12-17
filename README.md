```mermaid
flowchart LR

subgraph PO["Product Owner"]
    PO1["Define Team Structure\n(S1 & S2 Teams)"]
    PO2["Configure Paths\nQuarterly (S1) & 9-week (S2)"]
    PO3["Prioritize Outcomes\nCreate & Prioritize Epics & Features"]
    PO4["Monitor Progress\nDashboards"]
end

subgraph BA["Business Analyst"]
    BA1["Define Area Paths\nEDW Team S1 & S2"]
    BA2["Break Down Work\nEpics → Features → User Stories"]
    BA3["Add Acceptance Criteria\nData Rules & Source-to-Target Logic"]
end

subgraph TL["Tech Lead"]
    TL1["Review Dependencies\n& Technical Risks"]
    TL2["Create & Assign Tasks\nEstimate Effort (hrs)\nReview Capacity"]
end

subgraph DEVQA["Dev / QA Team"]
    DQ1["Onboard Team Members\nto Releases (S1 / S2)"]
    DQ2["Execute Stories\nRun Test Cases"]
    DQ3["Log Bugs & Observations"]
end

PO1 --> PO2 --> PO3
PO3 --> BA2
BA1 --> BA2 --> BA3
BA3 --> TL1 --> TL2
TL2 --> DQ1 --> DQ2 --> DQ3
PO4 -.-> PO3
