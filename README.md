# Revenue Analysis: Location Matching & Financial Adjustment

This project solves a two-part data science problem using two parquet datasets: `raw_financials.parquet` and `business_locations.parquet`. In **Part A**, it links noisy financial location records to business POI records using a two-pass entity resolution pipeline built on text cleaning, blocking, fuzzy matching, and one-to-one match enforcement. In **Part B**, it estimates total revenue from card-only revenue using segmented multiplier systems, with a size-based method as the primary approach and a geo-based method as an exploratory comparison. The workflow is designed to be transparent, practical, and easy to explain, while still handling large real-world datasets with messy names and addresses. The final output includes matched financial records, adjusted revenue estimates, summary metrics, and visual analysis.

Demo: https://entity-revenue-stream.vercel.app/

## Project Files

- `raw_financials.parquet` — financial records with location and revenue information  
- `business_locations.parquet` — POI/business location reference table  
- `requirements.txt` — Python dependencies needed to run the project  
- `*.ipynb` — Jupyter Notebook containing the full analysis pipeline  

## How to Reproduce This Project

### 1. Download the project files
Make sure the following files are available on your system in the same project folder:

- `raw_financials.parquet`
- `business_locations.parquet`
- `requirements.txt`
- the project notebook file

### 2. Create a project folder
Create a folder on your machine and place all files inside it.

Example structure:

```bash
project-folder/
│
├── raw_financials.parquet
├── business_locations.parquet
├── requirements.txt
└── revenue_analysis.ipynb
```

### 3.Create and activate a virtual environment
On macOS / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

On Windows
```bash
python -m venv venv
venv\Scripts\activate
```

### 4. Install dependencies

Install all required packages using:
```bash
pip install -r requirements.txt
```

### 5. Launch Jupyter Notebook

Start Jupyter Notebook in the project folder:
```bash
jupyter notebook
```
