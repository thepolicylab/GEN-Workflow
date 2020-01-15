---
title: Modeling for Non-Python Projects
date: 2020-01-02
slug: modeling-for-non-python-platforms

---

Because we work with the government, we often need to build models for platforms that are not based on Python. For example, for the Early Warning System with RIDE, we had to train models in ML.net, because RIDE's system is based on C#. We have documented a few compatibility notes for working with those systems.

## ML.net

`ML.net` is Microsoft's machine learning solution for their .net platform. For compatibility, ML.net provides a Python package called `nimbusml` that allows data scientists to train models in Python and port the model to ML.net. This package offers some compatibility with `Scikit-Learn`. However, there are some issues with this "train in Python, deploy in ML.net" workflow:

1. The type of objects used in training `nimbusml` models matters. Like `Scikit-Learn` model classes, `nimbusml` classes also offer `model.fit(X, y)` methods to train the models. However, it matters whether `X` is a `DataFrame` or a `numpy` array. If `X` is a `DataFrame`, then the saved model will carry information about the name of the features, but if `X` is an array, then the feature names are not stored in the saved `.zip` file. We recommend always passing `model.fit` a data frame so the feature names are saved.

2. Although `nimbusml` offers `LightGBM` algorithm out-of-box, `ML.net` does not have native support for `LightGBM` models and won't accept the `LightGBM` models trained in `nimbusml`. Models trained in `LightGBM` package for Python won't work either.

3. ML.net seems to be able to use models saved in `ONNX` format. Most Scikit-Learn models can be saved in this format with [the `sklearn-onnx` package](https://github.com/onnx/sklearn-onnx). `Catboost` supports `ONNX` formats as well, but models trained with categorical features cannot be saved in this format yet.