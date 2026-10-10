# Public Confidence in Healthcare Dashboard

An interactive dashboard from Sinead Madden’s Hybrid Simulation Modelling Lab exploring public confidence through a simple one-stock System Dynamics model.

## Survey informing the model

**Public confidence in Ireland's Health Service Executive, Mid-West region: Findings from a 2024 regional survey**

**Author:** Sinead Madden  
**Published survey:** https://link.springer.com/article/10.1186/s12913-025-13663-z

## Getting started

1. Save the dashboard HTML as `index.html`.
2. Open `index.html` in a modern web browser.
3. The three default scenario curves appear automatically.

The dashboard runs entirely in your browser. No installation, external JavaScript libraries or server is required.

## Using the dashboard

- **Run model:** animates the three scenario curves over approximately four seconds.
- **Reset:** restores the default controls and clears the graph and results.
- **Model controls:** change the initial confidence, building rate, erosion coefficient, custom adverse perception, simulation duration or time step.
- **Calculation method:** select the exact continuous-time solution or Euler integration.
- **Download results CSV:** exports the latest successful calculation, including all three presets and the custom scenario.

After changing any controls, press **Run model** to update the results.

The custom scenario appears in the summary cards, results table and CSV export. The graph displays the three preset scenarios.

## Model structure

**Public Confidence** is the single stock. **Confidence Building** increases the stock, and **Confidence Erosion** decreases it.

The equations are:

```text
Confidence Building =
    Confidence Building Rate × Public Confidence

Confidence Erosion Rate =
    Embedded erosion coefficient × Adverse System Perception

Confidence Erosion =
    Confidence Erosion Rate × Public Confidence

Change in Public Confidence =
    Confidence Building − Confidence Erosion
