# LightGBM
Light GBM is a gradient boosting framework that uses tree based learning algorithm.

## Installation

Use the package manager [pip](https://lightgbm.readthedocs.io/en/latest/Installation-Guide.html) to install LightGBM. Use the following to incorporate lightgbm into your Anaconda platform

```bash
conda install -c conda-forge lightgbm
```
## Data Description
A very small dataset with 400 rows and 5 columns. We want to predict whether the customer will buy the product from advertise given his age and estimated salary. This dataset contains no missing values and has been standardized into a proper format. 



## Usage
```python
import lightgbm as lgb
d_train = lgb.Dataset(x_train, label=y_train)
params = {}
```

