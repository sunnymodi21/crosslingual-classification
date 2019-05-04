## Cross Lingual Classification without translation or retraining

This project aim to create a sentiment classification model to be trained in one language and without retraining or translation of data use the the same model for any language

## Dependencies
* Python 2/3 with [NumPy](http://www.numpy.org/)/[SciPy](https://www.scipy.org/)
* [scikit-learn](http://scikit-learn.org/)
* [nltk](https://www.nltk.org/)

MUSE is available on CPU or GPU, in Python 2 or 3. Faiss is *optional* for GPU users - though Faiss-GPU will greatly speed up nearest neighbor search - and *highly recommended* for CPU users. Faiss can be installed using "conda install faiss-cpu -c pytorch" or "conda install faiss-gpu -c pytorch".

## Datasets
Amazon review datasets:
* Book review dataset in [*data/amazon-data*](https://github.com/sunnymodi21/crosslingual-classification/tree/master/data/amazon-dataset)
* 2000 for training and 2000 for testing
* Rating used as labels for positve or negative sentiment

You can download the English (en) French (es) and German (de) embeddings this way:
```bash
# English MUSE embeddings
curl -Lo data/wiki.en.vec https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.en.vec
# French MUSE Wikipedia embeddings
curl -Lo data/wiki.fr.vec https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.fr.vec
# German MUSE Wikipedia embeddings
curl -Lo data/wiki.de.vec https://dl.fbaipublicfiles.com/arrival/vectors/wiki.multi.de.vec
```

## Train and test classifier
This project includes testing all language pair to i.e En-En, En-Fr, En-De ,Fr-Fr, Fr-En, Fr-De, De-De, De-En, De-Fr:

To evalaute the results simply run:
```bash
python crosslingual-classification.py
```