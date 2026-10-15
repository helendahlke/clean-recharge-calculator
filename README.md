# Clean Recharge Calculator

An interactive, mobile-friendly educational tool for exploring how **residual soil nitrate-N might be diluted with clean recharge water** during agricultural managed aquifer recharge (Ag-MAR). The calculator estimates an **average pore water nitrate-N concentration** from a selected residual nitrate-N inventory and an applied recharge water depth.

**[Open the Clean Recharge Calculator](https://helendahlke.github.io/clean-recharge-calculator/)**

## How to use it

1. **Select residual soil nitrate-N** using one of eight bubbles: **5, 10, 15, 25, 40, 50, 75, or 100 lb N/acre**. The default is **25 lb N/acre**. These are illustrative nitrate inventories, not agronomic risk categories.
2. **Move the applied recharge water slider** between **0.5 and 8 feet**, in 0.5-foot increments, to explore how the estimated pore water nitrate-N concentration changes. The default is **3 feet**.
3. **Read the estimated average pore water nitrate-N concentration**, expressed in **mg/L NO₃-N**.
4. **Review the water-depth threshold** shown for a calculated average concentration **below 10 mg/L NO₃-N**, the drinking-water maximum contaminant level for nitrate expressed as nitrogen. The displayed threshold corresponds to exactly 10 mg/L in this idealized model; strictly less than 10 mg/L requires more water.
5. **Explore the graph**, which plots estimated average pore water nitrate-N concentration against applied water depth. The dashed horizontal line marks 10 mg/L; the dot marks the selected water depth.

## What does residual soil nitrate-N mean?

Residual soil nitrate-N is nitrate nitrogen remaining in the soil after crop uptake. Farmers can estimate it from soil samples analyzed by a soil-testing laboratory.

**The bubbles represent a nitrate-N inventory in pounds of nitrogen per acre (lb N/acre), not a concentration in ppm.** For interpretation, the tool assumes this inventory represents the upper **3 feet of soil**. If the soil laboratory reports nitrate-N in **ppm (mg/kg dry soil)**, converting that concentration to lb N/acre requires the **sampled depth and soil bulk density**. Do not enter a ppm value directly as lb N/acre.

Although soil texture and bulk density influence the conversion from ppm to lb N/acre, they are **not additional inputs to this calculator** once the nitrate-N inventory is known.

## Calculation

The calculator uses a simplified mass balance, assuming that all residual nitrate-N is flushed and mixed uniformly into all applied recharge water:

```text
Estimated average pore water NO₃-N (mg/L)
    = 0.3678109 × residual nitrate-N (lb N/acre)
                ÷ applied recharge water depth (feet)
```

The threshold water depth for an estimated average concentration of **10 mg/L NO₃-N** is:

```text
Threshold depth (feet)
    = 0.3678109 × residual nitrate-N (lb N/acre) ÷ 10
```

The incoming recharge water is assumed to contain **zero nitrate-N**.

## Scientific assumptions and limitations

This is a **complete-flushing, uniform-dilution screening calculation**, **not** a vadose-zone flow or reactive transport model. It assumes:

- The entire selected residual soil nitrate-N inventory is mobilized and exported.
- All applied water becomes deep percolation and mixes uniformly with that nitrate inventory.
- Recharge water initially contains no nitrate-N.
- Evaporation, antecedent soil-water deficits, pre-existing soil water, nitrate reactions, preferential flow, and deeper nitrate sources are not represented.
- Travel time and mixing with groundwater are not represented.

**Important:** Actual pore water and leachate concentrations can vary greatly with depth and time. An initial nitrate-rich flushing pulse may exceed **10 mg/L NO₃-N** even if the calculated average is below that value. The calculation **does not predict groundwater concentrations**, demonstrate drinking-water compliance, or establish a safe field application depth. Applying more water is not automatically a safe or practical nitrate-management strategy.

The 10 mg/L reference is the U.S. drinking-water maximum contaminant level for **nitrate as nitrogen (NO₃-N)**, not for nitrate ion (NO₃⁻).

## Run locally

Download `index.html` and open it in a modern web browser. No installation, account, server, or external software libraries are required.

## Publish updates with GitHub Pages

1. Keep `index.html` and `README.md` in the repository's root directory.
2. In **Settings → Pages**, select **Deploy from a branch**, `main`, and `/ (root)`.
3. Commit changes to `index.html` or `README.md` to publish updates automatically.

## Status

**Educational prototype.** The calculation is intended to demonstrate idealized dilution and should be validated and supplemented with field-specific data before use for management recommendations.
