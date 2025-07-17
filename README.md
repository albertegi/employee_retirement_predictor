# Predicting Years of Experience from Employment Data

## Project Overview

This project aims to predict the **years of experience** of employees using machine learning regression models.  
The target variable `years_of_experience` is derived from the `employment_date` feature in the dataset.

---

## Data Processing

The key step in feature engineering is converting the `employment_date` to a numerical value representing years of experience:

```python
from datetime import datetime
import pandas as pd

df['employment_date'] = pd.to_datetime(df['employment_date'])
df['years_of_experience'] = datetime.now().year - df['employment_date'].dt.year
