# How ideas were designed to move

Before we chose a tool, we set up an initial flow a submitted idea would follow, so the tool could support it. I drew the original diagram; this is a redraw without internal names or the open questions that sat beside it.

```mermaid
flowchart LR
  S["Idea is submitted"] --> C1{"Checklist I: does it have all the information needed to protect it?"}
  C1 -- yes --> C2{"Checklist II: what type of protection is relevant?"}
  C2 --> P["Details for protection"]
  C1 -- no --> F1(("Feedback?")):::open --> R["Idea is ready to be submitted again"]:::open
  S --> C3{"Checklist III: requirements"}
  C3 -- no --> F2(("Feedback?")):::open --> R
  C3 -- yes --> A["Competes for an award in a particular category"]
  A --> R1{"Rubric I: innovation awards"}
  R1 --> W["Winners in each category"]
  R1 --> E["Move to evaluation funnel"]
  E -- to determine pilots --> R2{"Rubric II: evaluation funnel (define)"}
  R2 --> CR["Concept resume"]
  R2 -- needs refinement --> F3(("Feedback?")):::open --> I["Iteration"]:::open --> E
  classDef open stroke-dasharray: 4 3
```

Steps with a question mark or a dashed outline were drawn that way in the original.
