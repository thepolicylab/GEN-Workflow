---
title: A Note on Notebooks
date: 2020-01-02
slug: a-note-on-notebooks

---

Jupiter notebooks are useful tools for us to interactively explore data and prototype different model-building techniques. However, if not carefully used, the notebooks soon become a mess and affect readability and productivity. Below are a few tips on how to organize and use notebooks.

## Storage

All notebooks should go under `notebooks` directory in the project repo.

## Naming conventions

The names of the notebooks should clearly indicate which segment of the workflow the notebook addresses and the order in which the notebooks should be read. Therefore, begin each name of the notebook with a number to indicate the order, followed by the purpose of the notebook (e.g. 2. Exploratory Data Analysis.ipynb). In case a step in the workflow consists multiple sub-steps, use another number to indicate order (e.g. 4.2. Training the model.ipynb). The following are a few recommended names to consider:

```
0. Clean the data.ipynb
1. Exploratory analysis.ipynb
2. Feature engineering.ipynb # sometimes 1 and 2 can be combined
3. Modeling
    3.1. Data preparation.ipynb
    3.2. Feature selection.ipynb
    3.3. Model training.ipynb
    3.4. Model evaluation
4. Report.ipynb
5. Model deployment.ipynb
```

## Structuring notebooks

Since notebooks allow execution of code not necessarily in order, the code can soon get out of order and become confusing even to the original author. Therefore, we recommend restarting the kernel and run all cells at least every 30 minutes or so to ensure that the cells are in order and the outputs are most up-to-date. We also recommend using **JupyterLab** instead of `jupyter notebook`, because the former allows dragging and dropping multiple cells to easily reorder the cells, along with many other more modern features such as dark mode.

Use headers to mark different sections in the notebook. Take sometime to write a few words that describes the purposes of each section. Use the techniques in [this article](https://medium.com/@dsteffan96/basic-jupyer-notebook-organization-with-html-6756442a2c31) to format headers and subsection headers and link them using hyperlinks.

![](https://miro.medium.com/max/4128/1*4xygHD1UkjjY289FBh-aDw.png)