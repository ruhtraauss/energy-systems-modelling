# Energy transition scenarios – France & World (work in progress)

**Status: in development.** This folder will host an open energy transition scenario tool.

## Goal
Build France and world energy transition scenarios (status quo, net zero, alternative) and assess:
- the number of years needed to reach net zero,
- impacts on GDP and employment,
- import dependency (France 2035 module).

## Approach (planned)
- **OSeMOSYS** (open-source energy system optimisation framework) for long-term capacity expansion scenarios.
- Coupling with the **PyPSA** dispatch model of the French power system ([`../pypsa`](../pypsa/)) to check hourly feasibility.
- Simple economic indicators derived from scenario outputs.
- A free **Streamlit** web app to explore the results (`site_internet.py`, currently a placeholder).

## Roadmap
- [ ] Build a reference OSeMOSYS model for France
- [ ] Define and run the three scenarios
- [ ] Link with PyPSA dispatch outputs
- [ ] Publish results in the web app

---

**FR —** Outil ouvert de scénarios de transition énergétique France / monde (en cours de développement) : modèle OSeMOSYS couplé au modèle de dispatch PyPSA, indicateurs PIB / emploi / dépendance aux importations, et application web Streamlit.
