---
tags:
  - dev
  - py
title: Python
---
```bash
pip freeze | %{$_.split('==')[0]} | %{pip install --upgrade $_}
```

From <[https://www.activestate.com/resources/quick-reads/how-to-update-all-python-packages/](https://www.activestate.com/resources/quick-reads/how-to-update-all-python-packages/)>

[poetry cheat sheet](https://gist.github.com/CarlosDomingues/b88df15749af23a463148bd2c2b9b3fb)

## Twisted #net
Network engine

numpy scipy jupyterlab matplotlib pandas scikit-learn

## Nuitka
Compiler

## Plotly
Publication-quality Graphs

[NLTK](https://www.nltk.org) #ai 
[NLP](../../Speech/NLP/NLP.md)

If you are not getting good results, you should first check that you are using the right [classification](../../AI/Classification/Classification.md) algorithm (is your data well fit to be classified by a linear [SVM](../../AI/Classification/Supervised/SVM.md)?) and that you have enough training data. Practically, that means you might consider visualizing your dataset through PCA or t-SNE to see how "clustered" your classes are, and checking how your classification metrics evolve with the amount of data your classifier is given.

If you then confirm that investing in tweaking your linear [SVM](../../AI/Classification/Supervised/SVM.md) is the right way to approach your problem, you can look at modifying the class weights. Note then that what you suggest as weights is probably the opposite of what you want to do: you are giving more weights to less frequent classes, marginalizing them further - said differently, you typically want to use weights that are inversely proportional to class frequencies. You can calculate these manually, or you can let sklearn do it automatically for you by specificing class_weight='balanced'.

From <[https://stats.stackexchange.com/questions/254779/optimal-class-weight-for-svc](https://stats.stackexchange.com/questions/254779/optimal-class-weight-for-svc)>