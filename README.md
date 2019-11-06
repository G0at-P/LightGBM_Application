# LightGBM_Application
LightGBM is a gradient boosting framework that uses tree based learning algorithm. This repository presents an application using LightGBM.

## LightGBM Installation

Follow the [instructions](https://lightgbm.readthedocs.io/en/latest/Installation-Guide.html) here to install LightGBM. Use the following bash command to incorporate lightgbm into your Anaconda platform

```bash
conda install -c conda-forge lightgbm
```
## Data Description
A very small [dataset](https://drive.google.com/file/d/0By9Y49AzZGaUakdSbFRodWJsUU0/view) with 400 rows and 5 columns We want to predict whether the customer will buy the product from advertise given his age and estimated salary. This dataset contains no missing values and has been standardized into a proper format. 



## Usage
In order to perform LightGBM on this dataset, we need to convert our training data into LightBGM data format. Also, we need to fine tune the parameters for better performance.
```python
import lightgbm as lgb
d_train = lgb.Dataset(x_train, label=y_train)
params = {}
params['learning_rate']=0.003
params['boosting_type']='gbdt'
params['objective']='binary'
params['metric']='binary_logloss'
params['sub_feature']=0.5
params['num_leaves']=10
params['min_data']=50
params['max_depth']=10
```

## Result
LightGBM achieves 94% accuracy with 500 iterations on this dataset. Also, the resulting confusion matrix shows low false positive rate and low negative rate for LightGBM.
