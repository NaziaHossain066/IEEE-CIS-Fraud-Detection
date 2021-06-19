# Project Title

[IEEE-CIS Fraud Detection](https://www.kaggle.com/c/ieee-fraud-detection/overview)

## Description

In this Kaggle competition, IEEE Computational Intelligence Society (IEEE-CIS) partnered with the world’s leading payment service company, Vesta Corporation, seeking the best solutions for the fraud prevention industry. The participant had to benchmark machine learning models on a challenging large-scale dataset containing data from Vesta's real-world e-commerce transactions. The objective of the competition was to improve the efficacy of fraudulent transaction alerts for millions of people around the world, helping hundreds of thousands of businesses reduce their fraud loss and increase their revenue.
## Getting Started

The most daunting task in this dataset is to preprocess such a huge number of features. But the step is inevitable, because as the saying goes, 'Garbage in, Garbage out'. Different algorithms can be tried out to reduce the dimensionality of the dataset. 

### Dependencies

Environment: Kaggle Notebook

### Executing program

* The notebook can be downloaded and run on the local machine.
* An immediate help would be to run the notebook in  [nbviewer](https://nbviewer.jupyter.org/)

Link to the Notebook:
>https://github.com/NaziaHossain66/IEEE-CIS-Fraud-Detection/blob/b56770c2945575e51cd257ad004213149a9f30f3/fraud-detection.8429.ipynb


## Help

If you find it difficult to work with the dataset in  a kaggle kernel, and keep hitting the RAM limit, reduce the size of the dataset using the following code:

```python:
def reduce_mem_usage(df):
    for col in df.columns:
        col_type=df[col].dtypes
        if df[col].dtypes != object:
            col_type_min = df[col].min()
            col_type_max = df[col].max()
            if str(col_type)[:3] == 'int':
                if col_type_min > np.iinfo(np.int8).min and col_type_max < np.iinfo(np.int8).max:
                    df[col] = df[col].astype(np.int8)
                elif col_type_min> np.iinfo(np.int16).min and col_type_max < np.iinfo(np.int16).max:
                    df[col] = df[col].astype(np.int16)
                elif col_type_min> np.iinfo(np.int32).min and col_type_max< np.iinfo(np.int32).max:
                    df[col] = df[col].astype(np.int32)
                elif col_type_min > np.iinfo(np.int64).min and col_type_max < np.iinfo(np.int64).max:
                    df[col] = df[col].astype(np.int64)
            else:
                if col_type_min > np.finfo(np.float16).min and col_type_max < np.finfo(np.float16).max:
                    df[col] = df[col].astype(np.float16)
                elif col_type_min> np.finfo(np.float32).min and col_type_max < np.finfo(np.float32).max:
                    df[col] = df[col].astype(np.float32)
                else:
                    df[col] = df[col].astype(np.float64)
    return df
  ```
    

## Authors

[Nazia Hossain](https://naziahossain66.github.io/Resume/)

[Linkedin](https://www.linkedin.com/in/nazia-hossain66/)

## Acknowledgments
* [towardsdatascience](https://towardsdatascience.com/)
* [geeksforgeeks](https://www.geeksforgeeks.org/)




