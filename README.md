# AGI Timelines and the Levels of AGI Framework, Explained

**Last updated: September 2026**

What AGI actually means, when major labs and independent forecasters expect it to arrive, and how DeepMind's Levels of AGI framework (plus a competing CHC-based scoring method) is used to measure progress toward it. Built for AI engineering leads, technical PMs, and researchers who want the concrete numbers instead of the hype cycle around each new model launch. Includes a forecast dataset, a one-page cheat sheet, and an AGI-readiness governance checklist you can use as-is.

## What's in this repo

- **[`data/agi-forecasts.csv`](data/agi-forecasts.csv)** — every publicly stated AGI timeline referenced below, one row per prediction, with source and date
- **[`CHEATSHEET.md`](CHEATSHEET.md)** — one-page reference: the three competing AGI yardsticks, DeepMind's five levels, and the jagged-intelligence pattern
- **[`checklist.md`](checklist.md)** — a 12-item AGI-readiness governance checklist for enterprise teams
- **[`embed-snippet.html`](embed-snippet.html)** — a callout box you can drop into a blog post linking back to this repo

---

## 1. What AGI Actually Means

The Turing Test is functionally obsolete — modern LLMs mimic human conversation without possessing general reasoning, so passing it proves nothing about intelligence. AGI is instead defined as a system with human-level cognitive flexibility: the ability to learn, reason, and apply knowledge across entirely novel, cross-domain problems without task-specific fine-tuning. Today's models are "narrow" by comparison — excellent at isolated tasks like code generation or text summarization, but unable to transfer that reasoning into unrelated domains the way a human would.

Because "human-level" is subjective, the field has settled on three competing ways to actually measure it:

| Yardstick | What it measures | Verdict on today's models |
|---|---|---|
| **Turing Test** (Turing, 1950) | Whether a human evaluator can tell the system apart from a person in conversation | Effectively obsolete — chatbots mimic conversation without general reasoning |
| **Levels of AGI** (DeepMind, Morris et al.) | A performance × generality matrix, from Emerging to Superhuman, decoupled from autonomy | Frontier models sit at Level 1 (Emerging), with brittle Level 2–3 flashes on narrow benchmarks |
| **CHC-Based AGI Score** (Hendrycks et al., 2025) | Ten broad human cognitive abilities averaged into one percentage | GPT-5 scores ~57–58%, up from GPT-4's 27% — real progress, but memory and cross-modal reasoning lag well behind |

**The core risk picture:** researchers most commonly cite three AGI-adjacent risks — misalignment with human values, autonomous exploitation of security vulnerabilities, and economic disruption from automating cognitive labor. These aren't hypothetical: in November 2025, Anthropic disclosed that a state-sponsored group had manipulated its Claude Code tool into carrying out roughly 80–90% of a multi-stage espionage campaign against about thirty organizations with minimal human direction, by disguising the attack as legitimate security testing. It's a narrow, early example of the security risk, not proof that current models can act as unsupervised general-purpose intruders — but it's why the security section of the [checklist](checklist.md) exists.

**Full breakdown:** [AGI Explained: What Happens When AI Matches Humans](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/agi-artificial-general-intelligence.html)

---

## 2. When Will AGI Arrive? Timelines Compared

Lab CEOs keep shortening their public AGI timelines. Frontier lab leaders (Altman, Amodei, Musk, Suleyman) generally cluster on 2026–2028. Demis Hassabis is the notable outlier among lab heads, holding a materially longer 5-to-10-year window as recently as January 2026. Independent forecasters run longer still: Metaculus's live community forecast has clustered in the late 2020s to early 2030s, while the 2023 AI Impacts survey of 2,778 published AI researchers put a 50% chance of human-level machine intelligence around 2047 — itself a 13-year compression from that same survey's 2060 median in 2022.

| Source | Type | Stated timeline | As of |
|---|---|---|---|
| Elon Musk (xAI) | Lab CEO | AI smarter than the smartest human within ~2 years | Jan 2026 |
| Dario Amodei (Anthropic) | Lab CEO, formal policy submission | "Powerful AI" (Nobel-laureate level) late 2026–2027 | Mar 2025 |
| Mustafa Suleyman (Microsoft AI) | Lab CEO | Human-level performance on most professional tasks in 12–18 months | Feb 2026 |
| Sam Altman (OpenAI) | Lab CEO | Internal system he'd call AGI by end of 2026 | Aug 2026 |
| Demis Hassabis (Google DeepMind) | Lab CEO | 5–10 years (~50% chance within 5 years) | Jan 2026 |
| Metaculus community | Live forecaster consensus | Early-to-mid 2030s (~50% odds) | 2025–2026 |
| AI Impacts / Grace et al. | Survey of 2,778 AI researchers | 2047 median (down from 2060 in 2022) | 2023 |
| Yann LeCun (AMI Labs) | Lab-affiliated skeptic | No date — argues current transformer architecture can't get there at all | Mar 2026 |

The debate got sharply more contentious after OpenAI's August 2025 GPT-5 launch, which critics on X and Reddit labeled an "AGI bait-and-switch" after heavy pre-launch AGI messaging met a model many testers saw as incremental. A year later the pattern repeated at higher volume: the first week of September 2026 alone brought four frontier releases — GPT-6 Astra, Claude Fable 5.1 and Mythos 5.1, Gemini 3.8, and Muse Spark 1.3 — each triggering the same split reaction between genuine benchmark gains and disputes over whether those evaluation setups reflect real-world use. OpenAI's own GPT-6 Astra launch post reports a 99.9% score on ARC-AGI-3 and 97.6% on FrontierMath Tier 4, alongside a comparatively middling 57.2% on Humanity's Last Exam with tools — the same jaggedness playing out inside a single model.

**Full breakdown:** [When Will AGI Arrive? Timelines Compared](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/agi-timeline-predictions.html)

---

## 3. The Levels of AGI Framework (DeepMind)

DeepMind researchers (Morris et al.) argued binary AGI definitions were useless for tracking real progress, and proposed a matrix based on two axes instead: **performance** (how well a system executes a task versus a human baseline) and **generality** (how many unrelated cognitive tasks it can handle without fine-tuning). A chess engine has superhuman performance and zero generality; an early LLM has high generality and relatively low performance. True AGI requires moving up on both axes at once.

| Level | Name | Threshold | 2026 status |
|---|---|---|---|
| 1 | Emerging | Equals or slightly exceeds an unskilled human across a wide variety of tasks | **Frontier models sit here** |
| 2 | Competent | At least the 50th percentile of skilled adults | Occasional flashes on narrow benchmarks |
| 3 | Expert | 90th percentile of skilled professionals | Occasional flashes on narrow benchmarks |
| 4 | Virtuoso | 99th percentile of human capability | Not yet reached |
| 5 | Superhuman | Outperforms 100% of humans on 100% of cognitive tasks | Not yet reached |

As of September 2026, the frontier generation (GPT-6 Astra, Claude Opus 5, Claude Fable 5.1, Gemini 3.8) is still classified as Level 1: Emerging, despite occasional Level 2–3 flashes — Google DeepMind and OpenAI models reached gold-medal level at the 2025 International Mathematical Olympiad, and Gemini separately reached gold-medal level at the 2025 ICPC World Finals. This uneven capability profile is called **jagged intelligence**: a model can out-reason a specialist on one problem and fail a simple logic puzzle in the same session. Separately, METR's research tracking how long a task frontier models can complete autonomously with 50% reliability found that "time horizon" has roughly doubled every seven months since 2019 — fast-growing autonomy even as overall reliability stays uneven.

A competing framework, the CHC-based AGI score (Hendrycks et al., 2025), scores systems across ten broad human cognitive abilities and averages them into one percentage instead of using discrete levels — it reports GPT-5 at roughly 57–58%, up from GPT-4's 27%. Critics note a simple average can flatter an uneven system, letting a strong math or knowledge score offset a near-zero long-term-memory score — exactly the failure mode DeepMind's dual-axis design was built to prevent. The two are best read as complementary: DeepMind's levels dominate policy and risk conversations, while the CHC score gives a trackable year-over-year number.

**Full breakdown:** [Levels of AGI: DeepMind's Framework Explained](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/levels-of-agi-framework.html)

---

## Quick reference assets

- **[`data/agi-forecasts.csv`](data/agi-forecasts.csv)** — structured dataset of every timeline prediction cited above (source, role, prediction, date given), with column notes in [`data/README.md`](data/README.md)
- **[`CHEATSHEET.md`](CHEATSHEET.md)** — print-friendly one-pager: the three yardsticks, the five DeepMind levels, and the jagged-intelligence pattern, all on one page
- **[`checklist.md`](checklist.md)** — a 12-item governance checklist for enterprises preparing security, oversight, and architecture for rising model autonomy, grouped into pre-deployment, monitoring, and organizational readiness

## Sources & deeper reading

- [AGI Explained: What Happens When AI Matches Humans](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/agi-artificial-general-intelligence.html)
- [When Will AGI Arrive? Timelines Compared](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/agi-timeline-predictions.html)
- [Levels of AGI: DeepMind's Framework Explained](https://aidevdayindia.org/blogs/agi-artificial-general-intelligence/levels-of-agi-framework.html)
- [Levels of AGI: Operationalizing Progress on the Path to AGI (Morris et al., DeepMind)](https://arxiv.org/abs/2311.02462)
- [A Definition of AGI (Hendrycks et al., 2025)](https://arxiv.org/abs/2510.18212)
- [METR: Measuring AI Ability to Complete Long Tasks](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/)
- [Metaculus: Date of Artificial General Intelligence](https://www.metaculus.com/questions/5121/date-of-artificial-general-intelligence/)
- [AI Impacts: 2023 Expert Survey on Progress in AI](https://arxiv.org/html/2401.02843v3)

## Contributing / corrections

Lab timelines and benchmark scores move fast and this dataset will drift out of date between updates. If you spot a stale figure, a superseded prediction, or a source that's been updated, open an issue or PR with the corrected value and a link to the primary source — self-reported lab benchmarks are noted as such in the dataset and should stay that way unless independently replicated.

**Update cadence:** quarterly, or sooner after a major lab timeline revision.

## About the author

Ayush Bisht is a Content Engineer and AI Tools Specialist at AgileWow, covering AI architecture, agent systems, model evaluation, and AI security. More writing at [aidevdayindia.org](https://aidevdayindia.org/).
