# :beers: COMP 432 – Project :tiger:

[Repo URL](https://github.com/AxelBogos/COMP432_Project) <br>
[Drive Folder with all content: notebooks, data and models that are not too big](https://drive.google.com/drive/folders/1nTKjXKobiQYIKER-sZe7c9Iv9b9Ns5tH?usp=sharing) <br>
---

Axel Bogos - 40077502 <br>
Group 39 <br>

---

## Preliminary Information

* Unfortunately the dataset is too big to be included. It is needed to either:
    1. Download it from the above link, put the folder in local directory and run local notebooks;
    2. Run the notebooks on Google Collab. There are cells to either download the data directly into the environments there, or you may upload the data and model directories into the environment. 

* The content of the folder on the Drive is exactly the same as the submission except for the means of reading the datafiles in the notebooks. The ELECTRA and LSTM notebooks were executed on a Google Collab GPU; their runtime on a CPU is unknown.  

* The required environment is included in the .yml file 

* The notebook are also available in the Google Drive link above, to run in Collab if need be.

* It is not recommended to run all cells of a notebook indiscriminately. Some cells execution's like hyperparameter search or bigram computation is quite long. 


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
| environment.yml
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
