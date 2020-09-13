# Tabular Data

[Notebook](https://github.com/fastai/fastbook/blob/master/09_tabular.ipynb)

The good news is that modern machine learning can be distilled down to a couple
of key techniques that are widely applicable. Recent studies have shown that
the vast majority of datasets can be best modeled with just two methods:

- Ensembles of decision trees (i.e., random forests and gradient boosting
machines), mainly for structured data (such as you might find in a database
table at most companies) 
- Multilayered neural networks learned with SGD (i.e.,
shallow and/or deep learning), mainly for unstructured data (such as audio,
images, and natural language)

Although deep learning is nearly always clearly superior for unstructured data,
these two approaches tend to give quite similar results for many kinds of
structured data. But ensembles of decision trees tend to train faster, are
often easier to interpret, do not require special GPU hardware for inference at
scale, and often require less hyperparameter tuning. They have also been
popular for quite a lot longer than deep learning, so there is a more mature
ecosystem of tooling and documentation around them.

Therefore, ensembles of decision trees are our first approach for analyzing a
new tabular dataset.

The exception to this guideline is when the dataset meets one of these conditions:

- There are some high-cardinality categorical variables that are very important ("cardinality" refers to the number of discrete levels representing categories, so a high-cardinality categorical variable is something like a zip code, which can take on thousands of possible levels).

 - There are some columns that contain data that would be best understood with a neural network, such as plain text data.

