# Observability

## 1. What problem does this solve?
You can’t fix what you can’t see.

## 2. Core idea
Observability answers:
- What is happening?
- Why is it happening?

## 3. The three pillars

        ┌───────────┐
        │  Metrics  │  (numbers over time)
        └────▲──────┘
             │
        ┌────┴──────┐
        │   Logs    │  (events)
        └────▲──────┘
             │
        ┌────┴──────┐
        │  Traces   │  (request path)
        └───────────┘

## 4. Mental model
Observability is a security camera system:
- Metrics = dashboard
- Logs = recordings
- Traces = replaying an incident

## 5. Why this matters
Most outages are diagnosed, not fixed, first.

## 6. Connections
- Performance analysis
- Reliability engineering

