# AGI-Readiness Governance Checklist

Twelve concrete checks for engineering and security teams preparing for rising model autonomy, grouped into three phases. This isn't a prediction of when AGI arrives — it's what to have in place regardless of which forecast in `data/agi-forecasts.csv` turns out to be right.

## Phase 1 — Pre-deployment

1. **Classify every AI-touching workflow by autonomy level.** Note which systems can only suggest actions versus which can execute them unsupervised. Autonomy, not raw intelligence, is what drives blast radius.
2. **Map your attack surface against agentic misuse.** Standard prompt-injection defenses assume a human is in the loop somewhere. Assume a sufficiently capable model can probe for exploits on its own and design controls accordingly.
3. **Define a scope-adherence test for any agent with tool access.** Before granting a model file, network, or deployment access, test whether it stays inside its authorized task boundary under adversarial framing (e.g., a request disguised as "legitimate testing").
4. **Set an internal capability-tier threshold that triggers a review.** Tie it to a public framework (DeepMind Level, or a lab's own Preparedness/Frontier Safety tier) so the trigger isn't a subjective judgment call made under deadline pressure.

## Phase 2 — Monitoring

5. **Deploy independent oversight ("guardian agent") processes for autonomous execution**, separate from the system being monitored, so a single compromised agent can't also disable its own oversight.
6. **Log and review agentic actions, not just outputs.** For agents with tool access, the action sequence matters as much as the final answer — that's where misuse shows up first.
7. **Track jagged-intelligence failure modes specific to your use case.** A model that's expert-level on one benchmark can fail basic reasoning on an adjacent task; don't assume a strong eval score generalizes to your actual workload without testing the adjacent cases.
8. **Re-run your risk assessment on every frontier model upgrade**, not on a fixed schedule. Capability jumps between model generations have outpaced quarterly review cycles more than once in 2025–2026.

## Phase 3 — Organizational readiness

9. **Assign explicit ownership for AI governance decisions**, distinct from the team shipping AI features, so deployment speed and risk review aren't adjudicated by the same incentives.
10. **Build an incident response plan for AI-assisted attacks specifically**, not just generic security incidents — the attacker's use of the AI agent changes what your response playbook needs to cover.
11. **Treat lab-reported benchmark and safety numbers as self-reported until independently replicated.** Plan around a range, not a single headline figure.
12. **Revisit your governance framework quarterly**, aligned with the update cadence of the underlying capability landscape — see the [main README](README.md) for the data this checklist is built on.

---
Built from patterns discussed in the [main README](README.md#1-what-agi-actually-means) and its source articles. Not legal or compliance advice — adapt to your organization's actual risk posture.
