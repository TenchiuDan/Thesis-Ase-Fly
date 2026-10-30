# Modeling and Simulation of Adaptive Behavior in Intelligent Agents

ASE bachelor’s thesis project. The working question and simulation environment remain open while feasibility is compared.

## Project status

- **Code draft due:** approximately 14 February 2027
- **Core code and experiments complete by:** 24 January 2027
- **Coordinator approval:** both an adaptive agent in a simulated environment and a simulated stock-trading agent are acceptable.
- **Technical requirements:** no additional university requirements were specified.
- **Development preference:** Python in VS Code.
- **Scope rule:** choose one environment before implementation; do not build both directions in parallel.

Profitability is not a promised outcome for the trading option. If selected, evaluate net returns after transaction costs and include held-out data and suitable risk metrics.

## Roadmap

| When | Focus | Deliverable |
|---|---|---|
| 30 Oct–1 Nov | Inspect repository and plan the smallest setup | Python availability and version recorded; initial project brief and coordinator questions |
| 2–8 Nov | Compare both candidate environments | Short feasibility comparison; no parallel full implementations |
| By 15 Nov | Choose one environment | Decision based on interest, adaptation experiment clarity, evaluation fairness, and implementation effort |
| 16 Nov–6 Dec | Build a minimal deterministic simulation (light availability) | Seeded environment and scripted baseline |
| 7–20 Dec | Add the simplest suitable learning baseline | Repeatable training run and episode metrics |
| 21 Dec–10 Jan | Add one controlled change in task conditions | Adaptation comparison; research question and metrics fixed by 10 Jan |
| 11–24 Jan | Evaluate and freeze core code | Repeated seeded trials, tests, summary results, and plots; code complete by 24 Jan |
| 25 Jan–11 Feb | Exams | No critical development scheduled |
| 12–14 Feb | Assemble code draft | Clean run instructions, results, limitations, and shareable draft |

Availability is reduced through mid-December and during exams from 25 January to 11 February. Plan short, self-contained tasks in the reduced-availability periods.

## MVP principles

- One small, reproducible software simulation with seeded resets.
- A transparent fixed or scripted baseline and one simple learning baseline.
- One controlled environment change to operationalise adaptation.
- Clear metrics, repeated seeds, tests, saved results, and a single documented way to rerun the main experiment.
- Start with tabular methods for a small discrete task. Add a larger ML/RL dependency only if the selected environment requires it.
- Keep multi-agent or colony behavior as an extension unless the research question and supervisor feedback make it necessary.

### Metrics to define before evaluation

For a general simulation, consider episodic reward, success rate, post-change performance, recovery time, and variability across seeds. State each calculation and evaluation window in the experiment notes.

For a trading simulation, use chronological training, validation, and held-out evaluation periods; include transaction costs; compare with buy-and-hold and a simple fixed rule; report net return, drawdown, and volatility. Treat results as evidence about the chosen data and simulator, not as a claim of general profitability.

## Immediate next steps

1. Confirm the repository location and record the existing Python version and operating system.
2. Draft a one-page brief with candidate research questions and coordinator questions, including expected evidence for the code draft.
3. Compare the two options by 15 November; implement only the selected direction.
4. After choosing, create the environment, test, and experiment scaffolding around that environment’s smallest end-to-end experiment.

## Suggested minimal project layout

Create these only as they become useful; the repository does not yet contain thesis code.

```text
Thesis-Ase-Fly/
├── README.md
├── THESIS_PLAN.md       # Research question, decisions, protocol, and dated checkpoints
├── pyproject.toml       # Project metadata and test configuration, when Python code begins
├── src/                 # Small environment, agents, and experiment runner
├── tests/               # Environment behavior and seeded reproducibility checks
└── results/             # Generated metrics and figures; document what is reproducible
```

## Decision log

| Date | Decision or update |
|---|---|
| 30 Oct 2026 | Coordinator confirmed both candidate directions are acceptable; no specific technical requirements. Keep the choice open and compare feasibility before selecting one. |
