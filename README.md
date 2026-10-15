# Clean Recharge Calculator

An interactive educational screening tool for exploring how residual soil nitrate-N and applied water depth affect the **estimated average nitrate-N concentration** during agricultural managed aquifer recharge (Ag-MAR).

The calculator is a single, mobile-friendly webpage (`index.html`) that runs in a browser without installation or a server.

## Use the calculator

1. Select a residual soil nitrate-N inventory: **25, 50, 100, or 200 lb N/acre**. These are illustrative categories, not established agronomic thresholds.
2. Adjust the applied recharge water depth from **0.5 to 8 feet**.
3. Read the estimated average nitrate-N concentration in **mg/L as N** and the idealized water depth required to reach **10 mg/L nitrate-N**.

Residual nitrate-N is entered as an **areal inventory (lb N/acre)**, assumed to represent the upper 3 feet of soil. Because it is already an areal inventory, the calculation does not require bulk density or soil texture. If starting from a soil test reported in ppm (mg/kg dry soil), converting to lb N/acre requires the sampled depth and soil bulk density.

## Calculation

The tool converts the residual nitrate-N inventory to kg N/ha and applied water depth to centimeters, then computes:

`Estimated average NO3-N (mg/L) = [Residual nitrate-N (kg/ha) × 10] / [Applied water depth (cm)]`

It also solves this equation for the applied water depth corresponding to a target of **10 mg/L NO3-N**. The incoming recharge water is assumed to contain no nitrate-N.

## Scientific assumptions and limitations

This is a **simplified, complete-flushing mass balance**, not a vadose-zone transport model. It assumes:

- The entire selected residual soil nitrate-N inventory is flushed into the percolating water.
- All applied water becomes deep percolation and mixes uniformly with the nitrate inventory.
- Incoming recharge water contains no nitrate-N.
- Nitrate transformations, preferential flow, pre-existing soil water, retention, and groundwater mixing are ignored.

**Important:** Actual leachate can have a high-concentration initial nitrate pulse even if the calculated average is below 10 mg/L. The tool cannot predict the nitrate concentration at the water table or demonstrate compliance with groundwater-quality standards. Applying more water is not automatically a safe or practical nitrate-management strategy; field-specific measurements and management are needed.

The **10 mg/L NO3-N** comparison value is the U.S. drinking-water maximum contaminant level for nitrate expressed as nitrogen, not a certification of recharge safety.

## Run locally

Download `index.html` and open it in any modern browser.

## Publish with GitHub Pages

1. Add `index.html` and `README.md` to the root of a public GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Save and open the GitHub Pages URL once deployment completes.

## Status

**Educational prototype.** Validate assumptions and calculations before using it for outreach or field-specific recharge recommendations.
