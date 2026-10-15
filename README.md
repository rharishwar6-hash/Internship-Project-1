## Dataset Information

### Data Source
This project uses a synthetic (simulated) dataset created for educational and analytical purposes. It does not contain real company or customer transaction records.

### Dataset Overview
- Total records: 540
- Total columns: 11
- Regions: North, South, and West
- Data frequency: Daily
- Date range: January 1, 2025 – June 29, 2025

### Key Variables
- `our_price`: Our product selling price
- `competitor_price`: Simulated competitor price
- `units_sold`: Number of units sold
- `revenue`: Daily sales revenue
- `treatment`: Indicates exposure to the simulated pricing intervention
- `period`: Identifies pre-treatment and post-treatment periods

### Important Note
The North region is assigned a simulated price increase beginning May 1, 2025. South and West are potential comparison regions for the synthetic control analysis. All findings are for demonstration and learning purposes and should not be interpreted as real-world business results.

## Data Validation (Week 1)

| Notebook | Owner | What it checks |
| --- | --- | --- |
| `01_data_validation.ipynb` | Harishwar | Missing values, duplicate rows, data types, treatment labels; exports cleaned CSV |
| `01b_data_validation_extended.ipynb` | Dhananjay | One row per region per day, revenue = price × units, outliers, PASS/FAIL summary |

**Result:** all checks pass. 540 rows (3 regions × 180 days), no missing values, gaps or duplicates.
Only North is treated: its price rises about 7% from 1 May 2025, while South and West stay flat and form the donor pool.
