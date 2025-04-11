# Car Fuel Consumption

The scope of this project is to apply data science tools to assess the fuel consumption of internal combustion engine cars, based on a limited amount of information. In addition to standard data analysis, unsupervised learning is applied to identify groups of vehicles that share similar characteristics, and supervised learning is performed to train a predictor for the fuel consumption variable.

The project consists of three notebooks:

1. **Introduction and Data Collection:** Introduces the scope of the project, discusses the data source, and performs data extraction from a web API.
2. **Data Analysis and Cleaning:** Performs exploratory data analysis and data cleaning. It includes a discussion on the splitting strategy for cross-validation and final evaluation.
3. **Machine Learning:** Trains clustering and regression models. It includes a custom scikit-learn estimator to improve the imputation performance.

The notebooks employ popular data science libraries such as [NumPy](https://numpy.org/), [SciPy](https://scipy.org/), [pandas](https://pandas.pydata.org/), [scikit-learn](https://scikit-learn.org/), [Matplotlib](https://matplotlib.org/), and [seaborn](https://seaborn.pydata.org/). They have been executed with Python 3.13.1, and the virtual environment can be recreated as usual via the requirements file: `python -m pip install -r requirements.txt`. Our final scikit-learn models are serialized with skops. Please follow [skops' documentation](https://skops.readthedocs.io/en/stable/persistence.html) to deserialize them; in particular, note that deserializing the linear regressor requires having defined our custom estimator `ClusteringImputer` within the current notebook or script.

This data science project is released under the MIT license. The data is sourced from the [European Environment Agency Datahub](https://www.eea.europa.eu/en/datahub), which publishes it under the CC-BY license. Please refer to the LICENSE file and to the first notebook for more information.
