# Growth Experiment Framework

## Experiment Record

### ID
GROWTH-EXP-XXX

### Question
What uncertainty are we reducing?

### Hypothesis
We believe [change] for [segment] will cause [outcome] because [reason].

### Surface / Channel
Where does the experiment run?

### Segment
Who is included/excluded?

### Baseline
Known current result, or `Unknown — baseline collection required`.

### Primary Metric
One main decision metric.

### Guardrail Metric
Protect quality, revenue, retention, reputation, deliverability, etc.

### Success Rule
Defined before launch.

### Failure Rule
Defined before launch.

### Duration / Sample Logic
Use practical duration/sample reasoning. Avoid fake statistical precision where traffic is low.

### Cost
Ad spend, engineering/design time, tooling, opportunity cost.

### Implementation
What changes?

### Instrumentation
What events/data are required?

### Result
Observed data.

### Interpretation
What did we learn?

### Decision
- Scale
- Iterate
- Stop
- Investigate
- Product change hypothesis

## Prioritization
Use ICE/RICE or a simple:
Impact × Confidence ÷ Effort

Treat scoring as prioritization aid only.

## Rules
- One experiment should answer a meaningful question.
- Do not change multiple uncontrolled things when learning matters.
- Do not call routine publishing an experiment unless there is a hypothesis.
- Do not move the success criterion after seeing results without documenting the change.
