# France carbon scenarios – educational tool (work in progress)

**Status:** scenario engine and web app in development, release planned for late November 2026.

A free, educational web app (Streamlit + Plotly) that explains France's energy system, economy and greenhouse-gas emissions, and lets anyone compare emission pathways with the carbon budget France has left.

> This is a carbon-scenario tool, not an integrated assessment model: there is no optimisation and no economy–climate feedback loop in this first stage.

## What it shows

1. **Context** – France's energy mix, economy and emissions.
2. **Remaining carbon budget** – a French budget derived from global budgets using different allocation keys (fair-share rules).
3. **Four scenarios on one page**, plotted together and driven by sliders:

| Scenario | Levers | Purpose |
|---|---|---|
| **S1 – Trend** | none | Component-wise extrapolation of past emissions, with uncertainty bands and a backtest. Shows the year the cumulative budget is exceeded. |
| **S2 – Demand** | sufficiency, efficiency, modal shift, consumption, share of domestic goods, population, product lifetime / repair | What demand-side action alone achieves |
| **S3 – Supply** | share of each energy carrier, carbon intensity, electrification, district heating, fuel switching with an efficiency factor (e.g. heat pumps) | What supply-side action alone achieves |
| **S4 – Combined** | all S2 + S3 levers, multiplicative effects | Interaction measured as S4 − S2 − S3 + S1 |

## Method

- Everything in CO₂e. Energy is counted on a **life-cycle basis** (upstream emissions abroad included), so imported energy products are removed from the imports term to avoid double counting.
- Accounting identity: **emissions = territorial (energy LCA + industry + agriculture) + imports − exports − sinks**.
- The budget is checked on **cumulative** emissions, not annual ones.
- After 2050: emissions ≤ removals.
- **Test invariant:** with every slider at zero, S2, S3 and S4 reproduce S1.
- The calculation engine is pure Python functions with unit tests, separate from the Streamlit interface.

## Roadmap

- [ ] Scenario engine S1–S4 with tests
- [ ] Streamlit + Plotly web app, free online
- [ ] Next stage: an optimised pathway – capacity planning with OSeMOSYS, hourly feasibility with the [PyPSA dispatch model](../pypsa), economic and geopolitical impacts, and a policy roadmap
- [ ] Then: extension to the world

---

**FR —** Outil pédagogique et gratuit (Streamlit + Plotly) qui explique l'énergie, l'économie et les émissions de la France, et compare quatre scénarios d'émissions (tendanciel, demande, offre, combiné) au budget carbone restant, calculé à partir des budgets mondiaux selon plusieurs clés de répartition. Étape suivante : un scénario optimisé (OSeMOSYS + PyPSA) avec impacts économiques et géopolitiques, puis le monde.
