# Global Malicious IP Threat Intelligence Analysis

Cleaning, validating, and exploring a real-world cybersecurity dataset of 10,000 IP addresses reported as malicious, to answer a concrete question: **where is malicious IP activity concentrated, and how widely spread is it geographically?**

## What's in this repo

| File | What it is |
|---|---|
| `Malicious_IP_Analysis.ipynb` | The full analysis — data audit, cleaning pipeline, and visualizations, with explanations at each step |
| `Project_Report.docx` | A written summary of the project for a non-technical audience |
| `raw_data.csv` | The original, unmodified dataset |
| `final_kaggle_cyber_dataset_cleaned.csv` | The dataset after cleaning |
| `figures/` | Exported chart images used in the notebook and report |

## Key findings

- The United States accounts for ~43% of all reported malicious IPs — over 5x the next-highest country (China) — most likely reflecting hosting infrastructure concentration rather than attacker origin.
- North America has the highest total volume of reports but that volume is concentrated in very few countries; Asia has lower volume but is spread across ~37 distinct countries, meaning no single country dominates.
- The raw dataset had no missing values or duplicates, but 7.5% of rows had failed geographic lookups that were fully recoverable, and transcontinental countries (e.g. Russia, Turkey) were labeled inconsistently.

See the notebook or report for full methodology, charts, and discussion.

## Tools

Python, pandas, matplotlib, Jupyter Notebook

## Running it yourself

```bash
pip install pandas matplotlib requests
jupyter notebook Malicious_IP_Analysis.ipynb
```

The notebook includes a live IP-geolocation lookup step that requires an internet connection to fully resolve one remaining record.


