# Energy Systems Modelling – Portfolio

Personal projects by **Arthur Aussenac**, engineer (IMT Atlantique, Master's degree 2026) specialised in energy system modelling and mathematical optimisation.
[LinkedIn](https://www.linkedin.com/in/arthur-aussenac) · arthur.aussenac@gmail.com

*Version française des descriptions détaillées : voir le README de chaque dossier.*

## Projects

| Project | What it does | Tools | Status |
|---|---|---|---|
| [**French power dispatch**](pypsa/) | Rebuilds the French power system (2015–2026) as an economic dispatch model and compares it with observed generation. Nuclear output is reproduced within 2%; the under-dispatch of thermal plants is diagnosed (missing ramp / minimum-load constraints). Carbon-price and nuclear-outage scenarios. | PyPSA, HiGHS, pandas, public RTE data | Done |
| [**PV + battery + grid sizing**](PYOMO/) | MILP that sizes PV panels and battery modules for a French household and optimises the hourly dispatch over a full year, minimising annualised cost. Quantifies the cost of increasing self-sufficiency, with a sensitivity analysis. | Pyomo, HiGHS, pvlib, ENTSO-E | Done |
| [**France carbon scenarios**](iam/) | Educational web app: France's energy, economy and emissions, and four emission scenarios (trend with backtest, demand, supply, combined) compared with a cumulative carbon budget derived from global budgets. Next stage: an optimised pathway with OSeMOSYS + PyPSA. | Python, Streamlit, Plotly | In progress – release late Nov 2026 |

The PyPSA and Pyomo folders each contain a detailed README (French, with an English summary), the notebook and a results report (PDF).

## Quick start

```bash
git clone https://github.com/ruhtraauss/energy-systems-modelling.git
cd energy-systems-modelling
pip install -r requirements.txt
jupyter notebook
```

The ENTSO-E API key used in the Pyomo project is never stored in the code: it is requested at runtime.
