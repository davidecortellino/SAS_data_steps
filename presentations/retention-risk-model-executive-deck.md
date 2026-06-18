# Retention Risk Model: Performance, Monitoring, and Business Value

## Slide 1 — Title
**Retention Risk Model: Performance, Monitoring, and Business Value**  
Inactivation model overview for Marketing leadership

**Presenter:** Davide Cortellino  
**Audience:** VP of Marketing  
**Purpose:** Explain the business value of the inactivation model and the monitoring framework used to govern performance over time.

---

## Slide 2 — Executive summary
- We developed an **inactivation prediction model** to identify contacts at risk of becoming inactive.
- The model helps Marketing **prioritize retention actions** toward the contacts most likely to disengage.
- Because outcomes mature over time, we built a **monitoring framework** to validate model quality continuously.
- The framework measures:
  - overall resolved performance
  - performance by inactivity stage
  - early-warning trajectory signals before final outcomes are known
- This provides both **business prioritization value** and **governance control**.

**Speaker notes**
- The key message is that this is not just a model; it is an operational decision-support asset with built-in monitoring.
- Emphasize that monitoring is necessary because customer inactivity outcomes do not resolve immediately.

---

## Slide 3 — Business problem
- Customer inactivity is a gradual process rather than a single event.
- Marketing needs to identify at-risk contacts **early enough to intervene**.
- Without prioritization, interventions can be:
  - too late
  - too broad
  - less efficient
- The model provides a structured way to focus on the highest-risk contacts first.

**Speaker notes**
- Frame the problem in business terms: retention efficiency, intervention timing, and better use of outreach capacity.

---

## Slide 4 — What the model does
- The model scores each eligible contact with a **probability of becoming inactive** within the observation horizon.
- Each scoring batch represents a **snapshot in time**.
- The same contact can appear in multiple batches as status evolves.
- This creates a historical view of risk that supports:
  - ongoing prioritization
  - trend analysis
  - performance monitoring by cohort

**Suggested visual**
- Simple timeline showing one contact rescored across multiple dates with changing risk level.

**Speaker notes**
- Explain that risk is dynamic and that repeated scoring is intentional.
- This is valuable because customer behavior changes over time.

---

## Slide 5 — Why monitoring is different here
- Final outcomes are **not immediately available** for every prediction.
- A contact can:
  - reactivate before reaching 12 months of inactivity, or
  - continue progressing until the inactivity threshold is reached
- This means model evaluation must happen in two ways:
  1. **Final performance on resolved cases**
  2. **Early-warning monitoring on unresolved cases**

**Speaker notes**
- This slide explains why standard one-time model evaluation is not enough.
- It sets up the logic for the monitoring framework.

---

## Slide 6 — Monitoring framework
### 1. Resolved-outcome performance
Measures final model quality only on contacts whose outcome is already known.

### 2. Segmented performance
Measures performance separately by inactivity stage:
- 0–3 months
- 3–6 months
- 6–9 months
- 9–12 months

### 3. Trajectory monitoring
Checks whether still-open predictions are evolving as expected before final outcomes are known.

**Suggested visual**
- Three-layer diagram: Final truth / Segment lens / Early warning.

**Speaker notes**
- This is the core governance architecture of the model.
- It gives both confidence in final performance and early warning before deterioration becomes visible in mature outcomes.

---

## Slide 7 — Key metrics used
### Ranking quality
- **AUC**: how well the model separates higher-risk from lower-risk contacts
- **KS**: how strongly the model differentiates positive and negative outcomes
- **Lift**: how concentrated inactive outcomes are among the highest-risk contacts

### Classification quality
- **Precision**: among predicted inactive contacts, how many actually became inactive
- **Sensitivity / Recall**: how many truly inactive contacts were correctly identified
- **F1 score**: balance between precision and recall

### Monitoring context
- **n_contacts**: number of resolved cases behind the metric
- **actual_churn_rate**: observed inactive outcome rate in the evaluated sample

**Speaker notes**
- Keep the language practical, not mathematical.
- The goal is to show that the model is measured from both ranking and operational decision perspectives.

---

## Slide 8 — How performance is reported
### Overall performance page
Tracks final KPI trends over time:
- AUC
- KS
- Lift
- F1 score

### Segment performance page
Shows whether model quality differs by inactivity stage.

### Early-warning page
Shows whether current predictions remain on track before final outcomes are available.

**Suggested visual**
- Dashboard mockup with three sections.

**Speaker notes**
- Position this as a management report rather than a technical model artifact.
- Each page answers a different business question.

---

## Slide 9 — Business decisions enabled
- Prioritize retention actions toward the highest-risk contacts
- Improve intervention efficiency by focusing on the most actionable population
- Detect whether model performance weakens over time
- Identify whether deterioration starts in specific inactivity segments
- Support retraining or review decisions with evidence rather than intuition

**Speaker notes**
- This is where the value becomes concrete: better targeting, governance, and confidence in action.

---

## Slide 10 — Risks and controls
### Main risks
- Early KPI snapshots can be unstable when few outcomes are resolved
- Performance may differ across inactivity stages
- Customer behavior can shift over time

### Controls built into the framework
- minimum resolved sample thresholds
- alerting logic
- historical trend monitoring
- segmented analysis
- early-warning trajectory validation

**Speaker notes**
- Reassure leadership that the framework is designed to avoid overreacting to immature or noisy signals.

---

## Slide 11 — Current recommendation
- Continue operating the model with regular monitoring
- Review overall and segment-level KPIs at each reporting cycle
- Use trajectory metrics as early-warning indicators, not as final judgment
- Build a business-facing dashboard for recurring leadership review

**Speaker notes**
- End with a practical recommendation: keep using the model, but govern it through regular monitoring.

---

## Slide 12 — Appendix: plain-English metric glossary
- **AUC:** ability to rank higher-risk contacts above lower-risk contacts
- **KS:** separation strength between inactive and non-inactive outcomes
- **Lift:** how much better the top-risk group performs versus the average population
- **Precision:** how accurate positive flags are
- **Sensitivity:** how many true inactive contacts the model captures
- **F1 score:** balance between capture and accuracy
- **On-track / off-track:** whether unresolved predictions are evolving as expected

**Speaker notes**
- Use only if the audience asks for definitions.
