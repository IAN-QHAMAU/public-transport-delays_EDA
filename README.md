# Public Transport Delay Analysis

A data analysis project exploring patterns in public transport delays using a Jupyter notebook, exported visualizations, and HTML reports.

## Project Overview

This project analyzes transport delay behavior across:
- time of day
- transport type
- route-level performance
- weather conditions
- special events

The notebook performs data loading, cleaning, exploratory analysis, and chart generation. Outputs are exported into the outputs folder for presentation and reporting.

## Project Structure

- data/public_transport_delays.csv → source dataset
- notebooks/Transport.ipynb → main analysis notebook
- outputs/Transport.html → full notebook converted to HTML
- outputs/visual_summary.html → styled narrative summary report
- outputs/index.html → entry page linking key HTML outputs
- outputs/*.png → generated chart files
- visualisations/ → optional custom dashboard files

## Quick Start

### 1) Activate environment

```bash
source venv/bin/activate
```

### 2) Open the notebook

```bash
jupyter notebook notebooks/Transport.ipynb
```

### 3) Run notebook cells

Run all cells in order to regenerate visuals and analysis outputs.

## Export Notebook to HTML

Use this command from the project root:

```bash
venv/bin/python -m jupyter nbconvert --to html notebooks/Transport.ipynb --output Transport.html --output-dir outputs
```

After export, open:
- outputs/Transport.html

## View Reports

Open this file first for navigation:
- outputs/index.html

It links to:
- outputs/Transport.html (full notebook)
- outputs/visual_summary.html (designed summary)

## Troubleshooting

### "View Full Notebook" link does not open

Ensure the footer link in outputs/visual_summary.html points to:
- Transport.html

### When Images show as missing

Make sure charts exist in outputs, for example:
- boxplot_transport.png
- delay_by_hour.png
- event_vs_no_event.png
- top_delayed_routes.png
- weather_transport_grouped.png

If missing, rerun the notebook cells that generate plots.

### nbconvert fails

Common causes:
- wrong notebook filename
- environment not activated
- missing jupyter/nbconvert packages

Verify you are converting:
- notebooks/Transport.ipynb

## Notes

- The canonical notebook in this project is Transport.ipynb.
- Generated HTML and images in outputs are intended for sharing and presentation.

## EDA Conclusion (Key Discoveries)

This analysis shows that delay is not random noise — it follows clear operational patterns.

### What stands out most

- **Delay concentrates at predictable times**: certain hours consistently experience higher average delays, indicating pressure windows in the daily network.
- **Not all transport types behave the same**: distribution plots show that some modes are not just slower on average, but also more variable and less predictable.
- **Events amplify lateness**: event-day comparisons reveal a measurable jump in delay, suggesting demand and congestion shocks are a major trigger.
- **Weather compounds system stress**: grouped weather-vs-transport visuals highlight that adverse weather does not affect every mode equally.
- **A small set of routes drives outsized delay**: top-route rankings suggest targeted route interventions could deliver disproportionate gains.

### Why this is powerful

Instead of treating late arrivals as isolated incidents, the EDA reframes delays as a **structured, explainable system outcome** linked to time, context, and route design. That means improvement is actionable: optimize peak-hour scheduling, harden event-day operations, weather-proof vulnerable modes, and prioritize fixes on the highest-delay corridors first.

### Final takeaway

The dataset tells a compelling story: reliability can be improved not by broad, expensive changes everywhere, but by **precision interventions where the data repeatedly points**. In short, this project converts raw delay records into a practical roadmap for smarter, more resilient public transport operations.
