# DataVisualisation-TP2025 — TP4

Simple solution of the [teacher's TP4](https://github.com/ahmed3991/DataVisualisation-TP2025/blob/main/TP4/TP4.md), covering the required tasks only.

- **TP4.ipynb**: executed notebook, with real outputs and the written answers.
- **tp4.py**: equivalent Python entry point.
- **EXPLICATION_AR.md**: Arabic explanation of each step and the results.
- **data/**: the actual source data used.
- **results/**: generated results and **REPORT.md** with the required answers.

## Run

Download `TP4.ipynb` from this private repository, upload it to [Google Colab](https://colab.research.google.com/), and choose **Runtime → Run all**. The first cell installs missing libraries. Private GitHub links can require authentication; uploading the downloaded notebook avoids that issue.

Alternatively, from this repository folder:

```sh
python -m pip install -r requirements.txt
python tp4.py
```

Open `results/05_interactive_gdp.html` and `results/06_life_expectancy_map.html` in a browser for hover and zoom. Colab shows them inline. The dataset deliberately covers 2000–2023; GDP per capita uses the corrected World Bank code `NY.GDP.PCAP.CD`.

Verified: all notebook cells executed successfully on 5,208 World Bank country-year observations. The required static charts, Plotly chart, Folium map, full regional hierarchy and written interpretations are included.
