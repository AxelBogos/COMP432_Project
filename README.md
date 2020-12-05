# :beers: COMP 432 – Project :tiger:

[Repo URL](https://github.com/AxelBogos/COMP432_Project) <br>
---

Axel Bogos - 40077502 <br>

---
## Preliminary Information


---
## Structure
The following directory structure is assumed: 
```
. /root
|
| Pre-processing&Baseliness.ipynb
| TFID_RanForest-XGBoost.ipynb
| LSTM.ipynb
| ELECTRA.ipynb
│
└───data
|   └───NELA
|   |   | true.csv
|   |   | false.csv
|   |   | complete_processed.csv
|   |   | complete_unprocessed.csv
|   |   └───BERT_data
|   |   | test.csv
|   |   | train.csv
└───models
|   └───sklearn
|   |   | best_gnb.pkl
|   |   | ...
│   └───LSTM
|   |   | ...
```
Unless otherwise mentioned, models are saved in the eponymous directory. Notebooks are organized in the following manner:
* Pre-processing&Baselines.ipynb : This notebook contains initial data exploration, data pre-processing, saves the processed data and trains a Naive Gauss baseline model. 

* TFID_RanForest-XGB.ipynb : This notebook reads the processed data, vectorizes it with on a term frequency basis with a TFID vectorizer and trains random-forest and XGBoost models on it. Hyperparameter search for these model is also done in the notebook.

* LSTM.ipynb : This notebook reads the processed data, vecotirzes it with a Word2Vec strategy and use it as an embedding layer of a bi-LSTM model. This notebook was ran on Google Collab.

* ELECTRA.ipynb : This notebooks reads the processed data, splits it in the expected format for the model and trains an ELECTRA model. This notebook was ran on Google Collab.


---
