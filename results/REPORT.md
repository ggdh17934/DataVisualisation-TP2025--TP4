# TP4 — Answers

## Data and cleaning
World Bank WDI, 2000–2023; 5208 country-year rows. Aggregate regions are
excluded. The latest year **within this selected dataset** is 2023,
not a claim about the newest year currently published by the World Bank.
Economies include some territories as classified by the source.
Numerical types are standardized, duplicate country-years removed and missing
values excluded only for analyses that need them. Comparative charts use
204 complete GDP/life/population economies; the heatmap uses
180 economies complete on all four indicators. No values are imputed.
The assignment labels its variable GDP_Per_Capita but gives NY.GDP.MKTP.CD
(total GDP). We use **NY.GDP.PCAP.CD**, the correct per-person indicator.

## Comparative chart choice
| Chart | Advantage | Disadvantage | Best use |
|---|---|---|---|
| Scatter | Shows the income/life relationship clearly | Every country has equal visual weight | Two-variable relationship |
| Bubble | Adds population as marker area | Overlap and area comparisons can be difficult | Population scale and impact |
| Density | Reveals concentrations of countries | Hides individual identities and population weights | Observation clusters |

Choose the **bubble chart** for the requested message. The horizontal spread
and vertical positions let us compare life expectancy among poorer economies;
the large areas identify populous middle-income economies. Population is
encoded as area, not radius. Logarithmic GDP spreads out low-income observations.
Density counts countries rather than people, so cannot communicate population
burden by itself. A bubble plot helps explain weights but does not itself
calculate the global population-weighted average or establish causation.

## Pearson correlations
The strongest absolute pair is **Life_Expectancy / Internet_Users_Pct**,
r = **0.807**. A plausible hypothesis is that economic development,
education, infrastructure and public services jointly relate to income,
connectivity and health; this is an interpretation, not a causal finding.
- Population vs GDP_Per_Capita: r = -0.057.
- Population vs Life_Expectancy: r = 0.003.
- Population vs Internet_Users_Pct: r = -0.004.
Population is total country size, whereas GDP is per person and internet use
is a percentage. Size alone therefore need not have a strong linear association
with development. Skewed population/GDP values and a few large economies affect
Pearson's measure; the heatmap uses raw values, unlike the log-scaled plot axis.

## Interactive tools and hierarchy
Germany and Algeria provide high-income and developing-country GDP trends;
hover, pan, zoom and the toolbar are enabled. Current-dollar trends include
price and exchange-rate effects and are not inflation-adjusted growth measures.
The Folium map displays 2023 life expectancy and country tooltips.
Gray means absent or unmatched data; historical boundary differences and ISO3
coverage can leave some economies unmapped. HTML files open in a browser.
The NetworkX graph includes all 217 selected economies under their
World Bank regions; ISO3 labels keep the full graph legible, with a names CSV.
Membership edges describe geography, not actual economic flows.

To model economic relationships, use countries as nodes and directed trade,
FDI, remittance or supply-chain links as edges, weighted by value/volume and
dated by year. This requires bilateral partner data, common country IDs,
currency/unit definitions and reporting dates. Regional membership alone does
not supply these transactions. No optional node-size or Altair bonus is added.

Sources: https://data.worldbank.org/indicator/NY.GDP.PCAP.CD (WDI, CC BY 4.0);
boundaries: https://github.com/johan/world.geo.json (public-domain repository).
Assignment: https://github.com/ahmed3991/DataVisualisation-TP2025/blob/main/TP4/TP4.md
