<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

	- [About H2O](#about-h2o)
	- [About this workshop](#about-this-workshop)
	- [About the algorithms](#about-the-algorithms)
		- [Generalized Linear Models (GLM)](#generalized-linear-models-glm)
		- [Word2vec](#word2vec)
	- [Vignettes](#vignettes)

<!-- /TOC -->

## About H2O

[In H2O Docs](http://docs.h2o.ai/h2o/latest-stable/h2o-docs/welcome.html)

## About this workshop

[WeCodeFest slides](https://docs.google.com/presentation/d/1d5nJh9_Fo1XqSliTXLGBHcry2RtURfon_LA4c2PL3FE/edit?usp=sharing)

## About the algorithms

### Generalized Linear Models (GLM)

[In H2O Docs](http://docs.h2o.ai/h2o/latest-stable/h2o-docs/data-science/glm.html)

[Introduction to Generalized Linear Models](http://statmath.wu.ac.at/courses/heather_turner/glmCourse_001.pdf)

[Demo H2O World](https://github.com/h2oai/h2o-tutorials/tree/master/tutorials/glm)

Generalized Linear Models (GLM) estimate regression models for outcomes following exponential distributions. In addition to the Gaussian (i.e. normal) distribution, these include Poisson, binomial, and gamma distributions. Each serves a different purpose, and depending on distribution and link function choice, can be used either for prediction or classification.

**Options**

- Datasets are commonly split into training, testing, and validation sets.
    - A *training* dataset is a dataset of examples used for learning, that is to fit the parameters of, for example, a classifier.
    - A *validation* dataset is a set of examples used to tune the hyperparameters of a classifier. It, as well as the testing set, should follow the same probability distribution as the training dataset.
    - A *test* dataset is a dataset that is independent of the training dataset, but that follows the same probability distribution as the training dataset.
- K-fold cross-validation is used to validate a model internally, i.e., estimate the model performance without having to sacrifice a validation split. Also, you avoid statistical issues with your validation split (it might be a “lucky” split, especially for imbalanced data). Good values for K are around 5 to 10. Comparing the K validation metrics is always a good idea, to check the stability of the estimation, before “trusting” the main model.
- Seed: This option specifies the random number generator (RNG) seed for algorithms that are dependent on randomization. When a seed is defined, the algorithm will behave deterministically.

### Word2vec

[In H2O Docs](http://docs.h2o.ai/h2o/latest-stable/h2o-docs/data-science/word2vec.html)

The Word2vec algorithm takes a text corpus as an input and produces the word vectors as output. The algorithm first creates a vocabulary from the training text data and then learns vector representations of the words. The vector space can include hundreds of dimensions, with each unique word in the sample corpus being assigned a corresponding vector in the space. In addition, words that share similar contexts in the corpus are placed in close proximity to one another in the space.


## Vignettes

[GLM Booklet](http://www.h2o.ai/wp-content/uploads/2018/01/GLM-BOOKLET.pdf)
[R Vignette](https://h2o-release.s3.amazonaws.com/h2o/rel-tibshirani/3/docs-website/h2o-docs/booklets/R_Vignette.pdf).
