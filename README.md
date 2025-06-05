# Step 1: Load the Superstore dataset (available within seaborn or can be simulated)
# Since we don't have internet access, simulate the Superstore dataset structure
import pandas as pd
import numpy as np

# Simulated version of Superstore dataset
np.random.seed(42)
dates = pd.date_range(start="2021-01-01", end="2023-12-31", freq='D')
data = {
    "Order Date": np.random.choice(dates, 1000),
    "Region": np.random.choice(["East", "West", "Central", "South"], 1000),
    "Category": np.random.choice(["Furniture", "Office Supplies", "Technology"], 1000),
    "Sub-Category": np.random.choice(["Chairs", "Phones", "Binders", "Tables", "Storage", "Accessories"], 1000),
    "Sales": np.random.uniform(20, 500, 1000),
    "Profit": np.random.uniform(-50, 150, 1000),
    "Quantity": np.random.randint(1, 10, 1000),
    "Segment": np.random.choice(["Consumer", "Corporate", "Home Office"], 1000)
}
superstore_df = pd.DataFrame(data)

# Preview the simulated dataset
superstore_df.head()
# task-4-dashboard
