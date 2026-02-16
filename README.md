# ML Takehome Project

Machine learning project for income classification and customer segmentation using Census Bureau data.

## Project Structure

```
.
├── classification.ipynb          # Income classification notebook
├── segmentation.ipynb            # Customer segmentation notebook
├── census-bureau.data            # Dataset (comma-separated)
├── census-bureau.columns         # Column headers
├── clustering_pipeline.pkl       # Saved clustering model
├── census_segmented.csv          # Segmented output file
├── requirements.txt              # Python dependencies
├── ML-TakehomeProject.pdf        # Assignment instructions
├── Report.docx.pdf               # Final report
└── README.md                     # This file
```

## Environment Setup

### 1. Create Virtual Environment (Recommended)

**Mac / Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

## Running the Income Classification Model

1. Start Jupyter:
   ```bash
   jupyter lab
   ```
   or
   ```bash
   jupyter notebook
   ```

2. Open `classification.ipynb`

3. Run all cells sequentially

**Requirements:** Ensure the following files are in the same directory:
- `census-bureau.data`
- `census-bureau.columns`

**Output:** All evaluation metrics and plots will be generated automatically.

## Running the Customer Segmentation Model

1. Open `segmentation.ipynb`

2. Run all cells sequentially

**Outputs Generated:**
- `census_segmented.csv` - Segmented customer data
- `clustering_pipeline.pkl` - Saved clustering model

## Using the Saved Clustering Model

Load and use the pre-trained clustering pipeline:

```python
import pickle

with open("clustering_pipeline.pkl", "rb") as f:
    pipeline = pickle.load(f)

predictions = pipeline.predict(new_data)
```

## Project Files

- **classification.ipynb** - Income classification model with evaluation metrics
- **segmentation.ipynb** - Customer segmentation and clustering analysis
- **ML-TakehomeProject.pdf** - Original assignment instructions
- **Report.docx.pdf** - Final project report with findings and conclusions
- **requirements.txt** - All required Python packages and versions

## Notes

- Ensure all input data files are present before running notebooks
- The clustering pipeline can be reused for predictions on new data
