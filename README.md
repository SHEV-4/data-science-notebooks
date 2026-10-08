# Data Science: Course Notebooks

A collection of practical assignments from a Data Science course: from NumPy and Pandas to classical machine learning, neural networks, and text processing. Each assignment is a separate Jupyter notebook with code, charts, and my own conclusions. The number at the start of each file name corresponds to the homework number.

## Contents

| Notebook | Topic | Tools |
|---|---|---|
| [01_numpy_basics.ipynb](01_numpy_basics.ipynb) | Working with arrays: the basics | NumPy |
| [02_1_pandas_visualization.ipynb](02_1_pandas_visualization.ipynb) | Data analysis and visualization | Pandas, NumPy, Matplotlib |
| [02_2_pandas_data_cleaning.ipynb](02_2_pandas_data_cleaning.ipynb) | Data cleaning and analysis (dataset `2017_jun_final.csv`) | Pandas, Seaborn |
| [02_3_pandas_bestsellers.ipynb](02_3_pandas_bestsellers.ipynb) | Bestsellers analysis (dataset `bestsellers with categories.csv`) | Pandas, Seaborn |
| [06_linear_regression.ipynb](06_linear_regression.ipynb) | Linear regression and gradient descent (`Housing.csv`) | scikit-learn, NumPy |
| [07_regularization.ipynb](07_regularization.ipynb) | Linear regression: overfitting, collinearity, regularization (`bikes_rent.csv`) | scikit-learn |
| [08_classification_svm_rf.ipynb](08_classification_svm_rf.ipynb) | Classification: SVM and Random Forest | scikit-learn, SciPy |
| [09_kmeans_clustering.ipynb](09_kmeans_clustering.ipynb) | K-Means clustering, the elbow method (2D data and MNIST) | scikit-learn |
| [10_recommender_systems.ipynb](10_recommender_systems.ipynb) | Recommender systems: SVD, SVD++, NMF (MovieLens 100k) | Surprise |
| [11_neural_network_tensorflow.ipynb](11_neural_network_tensorflow.ipynb) | Fully connected neural network on MNIST, built with low-level TensorFlow | TensorFlow |
| [12_mlp_fashion_mnist.ipynb](12_mlp_fashion_mnist.ipynb) | Multilayer perceptron on Fashion MNIST | Keras |
| [13_1_cnn_fashion_mnist.ipynb](13_1_cnn_fashion_mnist.ipynb) | Convolutional neural network (CNN) on Fashion MNIST | Keras |
| [13_2_vgg16_transfer_learning.ipynb](13_2_vgg16_transfer_learning.ipynb) | Transfer learning: VGG16 on Fashion MNIST | Keras |
| [14_rnn_sentiment_imdb.ipynb](14_rnn_sentiment_imdb.ipynb) | Sentiment analysis of IMDB reviews: RNN, LSTM, GRU, BRNN, DRNN | Keras |
| [15_text_summarization.ipynb](15_text_summarization.ipynb) | Automatic text summarization | NLTK, spaCy |

## Key Results

- **Fashion MNIST:** the multilayer perceptron reached about 89.5% accuracy, the convolutional network about 92%, and VGG16 with ImageNet weights 90.6%. In the author's view, VGG16 falls behind the CNN because single-channel images had to be fed to it as three-channel ones.
- **Recommender systems (MovieLens 100k, 5-fold cross-validation):** the most accurate model is SVD++ (RMSE 0.9208), followed by SVD (0.9372) and NMF (0.9611). SVD++ is the slowest, while SVD offers the best balance of accuracy and speed.
- **IMDB sentiment analysis:** judging by the metrics and charts, LSTM performed best, followed by GRU, BRNN, DRNN, and SimpleRNN.

See the corresponding notebooks for the full conclusions and charts.

## Technologies

Python, Jupyter Notebook, NumPy, Pandas, Matplotlib, Seaborn, SciPy, scikit-learn, TensorFlow / Keras, scikit-surprise, NLTK, spaCy.

## Running

1. Clone the repository:

   ```bash
   git clone https://github.com/SHEV-4/data-science-notebooks.git
   cd data-science-notebooks
   ```

2. Install the dependencies:

   ```bash
   pip install numpy pandas matplotlib seaborn scipy scikit-learn tensorflow scikit-surprise nltk spacy jupyter
   python -m spacy download en_core_web_sm
   ```

3. For `15_text_summarization.ipynb`, download the NLTK data:

   ```python
   import nltk
   nltk.download("stopwords")
   nltk.download("punkt")
   ```

4. Start Jupyter and open the notebook you need:

   ```bash
   jupyter notebook
   ```

## Data

The data files are not included in the repository, so place them next to the notebooks before running:

| Notebook | Required files |
|---|---|
| 02_2_pandas_data_cleaning | `2017_jun_final.csv` |
| 02_3_pandas_bestsellers | `bestsellers with categories.csv` |
| 06_linear_regression | `Housing.csv` |
| 07_regularization | `bikes_rent.csv` |
| 08_classification_svm_rf | a set of `.csv` files in the folder specified in the notebook |
| 09_kmeans_clustering | `data/data_2d.csv`, `data/mnist.csv` |

The Fashion MNIST, MNIST, IMDB, and MovieLens 100k datasets are downloaded automatically by the Keras and Surprise libraries.

`06_linear_regression` and `07_regularization` were written in Google Colab (`google.colab.files.upload`), so they are convenient to open in [Google Colab](https://colab.research.google.com/). In a local Jupyter, replace the file upload with a regular `pd.read_csv(...)`.

## Related Projects

- [fashion-mnist-classifier](https://github.com/SHEV-4/fashion-mnist-classifier): a Streamlit app with CNN and VGG16 models for Fashion MNIST.
- [telecom-churn-prediction](https://github.com/SHEV-4/telecom-churn-prediction): customer churn prediction for a telecom operator.

## Author

[SHEV-4](https://github.com/SHEV-4)
