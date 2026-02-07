# X-VESTA: Explainability Architecture for Semantic V2G Energy Management

This repository contains evaluation data, analysis scripts, and generated figures for the X-VESTA explainability architecture, which extends the VESTA semantic V2G framework with multi-stakeholder explanation generation capabilities.

## Overview

**VESTA** (Vehicle Energy Sharing Through Artificial Intelligence) is a semantic V2G framework that uses AI-driven decision-making and semantic-aware vehicle access control (SEVAC) for intelligent energy management.

**X-VESTA** adds a non-invasive explainability layer on top of VESTA, providing stakeholder-appropriate explanations for automated V2G decisions without modifying the underlying optimization logic.

## Related Publications

### Foundation Framework
**Artificially Intelligent Vehicle-to-Grid Energy Management: A Semantic-Aware Framework Balancing Grid Demands and User Autonomy**  
Mahmoud Elkhodr, Ergun Gide  
*Computers*, vol. 13, no. 10, article 249, October 2024  
DOI: [10.3390/computers13100249](https://doi.org/10.3390/computers13100249)  
Available: https://www.mdpi.com/2073-431X/13/10/249

### Explainability Extension (This Work)

**X-VESTA: An Explainability Architecture for Semantic Vehicle-to-Grid Energy Management
 Mashmoud Elkhodr and E. Gide, in Proceedings of the In-
ternational Conference on Cybernetics and Innovations (ICCI), Thailand,
April 2026, (Submitted).

**Multi-Stakeholder Explainable AI for Vehicle-to-Grid (V2G) Energy Management: The X-VESTA Architecture**  
Mahmoud Elkhodr, Ergun Gide, Ibrahim El Didi, Abdallah Al-Sabbagh  
Preprint pending, 2025 (submitted)

## Repository Contents

### Data Files
- `xvesta_scenarios_melbourne.csv` - 37,610 decision scenarios derived from Melbourne charging data
- `attribution_results_melbourne.csv` - Computed attribution weights for all scenarios
- `attribution_statistics.json` - Summary statistics for attribution analysis
- `baseline_comparison_detailed.csv` - Comparative baseline evaluation results
- `e_price.csv`, `volume.csv`, `weather.csv` - Raw CHARGED dataset (Melbourne subset)

### Analysis Scripts
- `process_charged_data.py` - Transforms CHARGED dataset into X-VESTA scenarios
- `analyze_real_data.py` - Computes attribution patterns and generates statistics
- `baseline_comparison.py` - Comparative evaluation against baseline methods

### Generated Figures
All figures used in the X-VESTA paper (Figures 2-10):
- Performance evaluation: `scalability_plot_refined.png`, `complexity_plot_refined.png`
- Operational data analysis: `fig_attribution_pie.png`, `fig_mode_comparison.png`, `fig_price_correlation.png`, `fig_temporal_heatmap.png`
- Stakeholder adaptation: `readability_hist_refined.png`
- Baseline comparison: `fig_baseline_examples.png`, `fig_baseline_comparison.png`

## Data Source

Operational charging data sourced from the **CHARGED** global EV charging dataset:
- 6 months (April-September 2023) from 62 Melbourne public charging stations
- Dataset: https://github.com/IntelligentSystemsLab/CHARGED
- Paper: https://www.nature.com/articles/s41597-025-05584-7

## Usage

### Processing CHARGED Data
```bash
python process_charged_data.py
```
Generates `xvesta_scenarios_melbourne.csv` from raw CHARGED data.

### Running Attribution Analysis
```bash
python analyze_real_data.py
```
Computes attribution weights and generates operational data figures.

### Baseline Comparison
```bash
python baseline_comparison.py
```
Evaluates X-VESTA against alternative explanation methods.

## Requirements
```
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
```

## License

This work is licensed under [MIT].

## Contact

Mahmoud Elkhodr - m.elkhodr@cqu.edu.au  
Central Queensland University, Sydney, Australia

## Citations

If you use this code or data, please cite both papers:

### VESTA Framework
```bibtex
@article{elkhodr2024artificially,
  author={Elkhodr, Mahmoud and Gide, Ergun},
  title={Artificially Intelligent Vehicle-to-Grid Energy Management: A Semantic-Aware Framework Balancing Grid Demands and User Autonomy},
  journal={Computers},
  volume={13},
  number={10},
  pages={249},
  year={2024},
  publisher={MDPI},
  doi={10.3390/computers13100249},
  url={https://www.mdpi.com/2073-431X/13/10/249}
}
```


```
