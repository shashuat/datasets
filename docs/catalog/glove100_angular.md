<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="glove100_angular" />
  <meta itemprop="description" content="Pre-trained Global Vectors for Word Representation (GloVe) embeddings for&#10;approximate nearest neighbor search. This dataset consists of two splits:&#10;&#10;  1. &#x27;database&#x27;: consists of 1,183,514 data points, each has features:&#10;    &#x27;embedding&#x27; (100 floats), &#x27;index&#x27; (int64), &#x27;neighbors&#x27; (empty list).&#10;  2. &#x27;test&#x27;: consists of 10,000 data points, each has features: &#x27;embedding&#x27; (100&#10;    floats), &#x27;index&#x27; (int64), &#x27;neighbors&#x27; (list of &#x27;index&#x27; and &#x27;distance&#x27;&#10;    of the nearest neighbors in the database.)&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;glove100_angular&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/glove100_angular" />
  <meta itemprop="sameAs" content="https://nlp.stanford.edu/projects/glove/" />
  <meta itemprop="citation" content="@inproceedings{pennington2014glove,&#10;  author = {Jeffrey Pennington and Richard Socher and Christopher D. Manning},&#10;  booktitle = {Empirical Methods in Natural Language Processing (EMNLP)},&#10;  title = {GloVe: Global Vectors for Word Representation},&#10;  year = {2014},&#10;  pages = {1532--1543},&#10;  url = {http://www.aclweb.org/anthology/D14-1162},&#10;}" />
</div>

# `glove100_angular`


Note: This dataset was added recently and is only available in our
`tfds-nightly` package
<span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>.

*   **Description**:

Pre-trained Global Vectors for Word Representation (GloVe) embeddings for
approximate nearest neighbor search. This dataset consists of two splits:

1.  'database': consists of 1,183,514 data points, each has features:
    'embedding' (100 floats), 'index' (int64), 'neighbors' (empty list).
2.  'test': consists of 10,000 data points, each has features: 'embedding' (100
    floats), 'index' (int64), 'neighbors' (list of 'index' and 'distance' of the
    nearest neighbors in the database.)

*   **Homepage**:
    [https://nlp.stanford.edu/projects/glove/](https://nlp.stanford.edu/projects/glove/)

*   **Source code**:
    [`tfds.nearest_neighbors.glove_100_angular.Glove100Angular`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/nearest_neighbors/glove_100_angular/glove_100_angular.py)

*   **Versions**:

    *   **`1.0.0`** (default): Initial release.

*   **Download size**: `462.93 MiB`

*   **Dataset size**: `567.90 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    No

*   **Splits**:

Split        | Examples
:----------- | --------:
`'database'` | 1,183,514
`'test'`     | 10,000

*   **Feature structure**:

```python
FeaturesDict({
    'embedding': Tensor(shape=(100,), dtype=tf.float32),
    'index': Scalar(shape=(), dtype=tf.int64),
    'neighbors': Sequence({
        'distance': Scalar(shape=(), dtype=tf.float32),
        'index': Scalar(shape=(), dtype=tf.int64),
    }),
})
```

*   **Feature documentation**:

| Feature            | Class        | Shape  | Dtype      | Description        |
| :----------------- | :----------- | :----- | :--------- | :----------------- |
|                    | FeaturesDict |        |            |                    |
| embedding          | Tensor       | (100,) | tf.float32 |                    |
| index              | Scalar       |        | tf.int64   | Index within the   |
:                    :              :        :            : split.             :
| neighbors          | Sequence     |        |            | The computed       |
:                    :              :        :            : neighbors, which   :
:                    :              :        :            : is only available  :
:                    :              :        :            : for the test       :
:                    :              :        :            : split.             :
| neighbors/distance | Scalar       |        | tf.float32 | Neighbor distance. |
| neighbors/index    | Scalar       |        | tf.int64   | Neighbor index.    |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `None`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

*   **Citation**:

```
@inproceedings{pennington2014glove,
  author = {Jeffrey Pennington and Richard Socher and Christopher D. Manning},
  booktitle = {Empirical Methods in Natural Language Processing (EMNLP)},
  title = {GloVe: Global Vectors for Word Representation},
  year = {2014},
  pages = {1532--1543},
  url = {http://www.aclweb.org/anthology/D14-1162},
}
```
