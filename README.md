# Data Science: ноутбуки з курсу

Збірка практичних робіт із курсу Data Science: від NumPy та Pandas до класичного машинного навчання, нейронних мереж і обробки тексту. Кожна робота оформлена окремим Jupyter-ноутбуком з кодом, графіками та власними висновками. Номер на початку назви відповідає номеру домашнього завдання.

## Зміст

| Ноутбук | Тема | Інструменти |
|---|---|---|
| [01_numpy_basics.ipynb](01_numpy_basics.ipynb) | Основи роботи з масивами | NumPy |
| [02_1_pandas_visualization.ipynb](02_1_pandas_visualization.ipynb) | Аналіз даних і візуалізація | Pandas, NumPy, Matplotlib |
| [02_2_pandas_data_cleaning.ipynb](02_2_pandas_data_cleaning.ipynb) | Очищення та аналіз даних (датасет `2017_jun_final.csv`) | Pandas, Seaborn |
| [02_3_pandas_bestsellers.ipynb](02_3_pandas_bestsellers.ipynb) | Аналіз бестселерів (датасет `bestsellers with categories.csv`) | Pandas, Seaborn |
| [06_linear_regression.ipynb](06_linear_regression.ipynb) | Лінійна регресія та градієнтний спуск (`Housing.csv`) | scikit-learn, NumPy |
| [07_regularization.ipynb](07_regularization.ipynb) | Лінійна регресія: перенавчання, колінеарність, регуляризація (`bikes_rent.csv`) | scikit-learn |
| [08_classification_svm_rf.ipynb](08_classification_svm_rf.ipynb) | Класифікація: SVM та Random Forest | scikit-learn, SciPy |
| [09_kmeans_clustering.ipynb](09_kmeans_clustering.ipynb) | Кластеризація K-Means, метод «ліктя» (2D-дані та MNIST) | scikit-learn |
| [10_recommender_systems.ipynb](10_recommender_systems.ipynb) | Рекомендаційні системи: SVD, SVD++, NMF (MovieLens 100k) | Surprise |
| [11_neural_network_tensorflow.ipynb](11_neural_network_tensorflow.ipynb) | Повнозв'язна нейромережа на MNIST, створена на низькорівневому TensorFlow | TensorFlow |
| [12_mlp_fashion_mnist.ipynb](12_mlp_fashion_mnist.ipynb) | Багатошаровий перцептрон на Fashion MNIST | Keras |
| [13_1_cnn_fashion_mnist.ipynb](13_1_cnn_fashion_mnist.ipynb) | Згорткова нейромережа (CNN) на Fashion MNIST | Keras |
| [13_2_vgg16_transfer_learning.ipynb](13_2_vgg16_transfer_learning.ipynb) | Перенесення навчання: VGG16 на Fashion MNIST | Keras |
| [14_rnn_sentiment_imdb.ipynb](14_rnn_sentiment_imdb.ipynb) | Аналіз тональності відгуків IMDB: RNN, LSTM, GRU, BRNN, DRNN | Keras |
| [15_text_summarization.ipynb](15_text_summarization.ipynb) | Автоматичне реферування тексту | NLTK, spaCy |

## Ключові результати

- **Fashion MNIST:** багатошаровий перцептрон дав близько 89,5 % точності, згорткова мережа близько 92 %, VGG16 з вагами ImageNet 90,6 %. На думку автора, VGG16 програє CNN, бо йому довелося подавати одноканальні зображення як трьохканальні.
- **Рекомендаційні системи (MovieLens 100k, 5-кратна крос-валідація):** найточніша модель SVD++ (RMSE 0,9208), далі SVD (0,9372) та NMF (0,9611). SVD++ найповільніша, SVD дає найкращий баланс точності й швидкості.
- **Аналіз тональності IMDB:** за метриками й графіками кращою виявилася LSTM, далі GRU, BRNN, DRNN і SimpleRNN.

Повні висновки та графіки дивись у відповідних ноутбуках.

## Технології

Python, Jupyter Notebook, NumPy, Pandas, Matplotlib, Seaborn, SciPy, scikit-learn, TensorFlow / Keras, scikit-surprise, NLTK, spaCy.

## Запуск

1. Клонуй репозиторій:

   ```bash
   git clone https://github.com/SHEV-4/data-science-notebooks.git
   cd data-science-notebooks
   ```

2. Встанови залежності:

   ```bash
   pip install numpy pandas matplotlib seaborn scipy scikit-learn tensorflow scikit-surprise nltk spacy jupyter
   python -m spacy download en_core_web_sm
   ```

3. Для `15_text_summarization.ipynb` завантаж дані NLTK:

   ```python
   import nltk
   nltk.download("stopwords")
   nltk.download("punkt")
   ```

4. Запусти Jupyter і відкрий потрібний ноутбук:

   ```bash
   jupyter notebook
   ```

## Дані

Файли з даними не входять до репозиторію, тому перед запуском поклади їх поруч із ноутбуками:

| Ноутбук | Потрібні файли |
|---|---|
| 02_2_pandas_data_cleaning | `2017_jun_final.csv` |
| 02_3_pandas_bestsellers | `bestsellers with categories.csv` |
| 06_linear_regression | `Housing.csv` |
| 07_regularization | `bikes_rent.csv` |
| 08_classification_svm_rf | набір `.csv` у папці, яку вказано в ноутбуці |
| 09_kmeans_clustering | `data/data_2d.csv`, `data/mnist.csv` |

Датасети Fashion MNIST, MNIST, IMDB та MovieLens 100k завантажуються автоматично бібліотеками Keras і Surprise.

`06_linear_regression` і `07_regularization` писалися в Google Colab (`google.colab.files.upload`), тому їх зручно відкривати в [Google Colab](https://colab.research.google.com/). У локальному Jupyter замінь завантаження файлу на звичайний `pd.read_csv(...)`.

## Пов'язані проєкти

- [fashion-mnist-classifier](https://github.com/SHEV-4/fashion-mnist-classifier): Streamlit-застосунок із моделями CNN та VGG16 для Fashion MNIST.
- [telecom-churn-prediction](https://github.com/SHEV-4/telecom-churn-prediction): прогнозування відтоку клієнтів телеком-оператора.

## Автор

[SHEV-4](https://github.com/SHEV-4)
