# What is Machine Learning?

ML is the process of <u>**training**</u> a piece of software, called a <u>**model**</u>, to make useful <u>**predictions**</u> or generate content from data.

## Example

For example, suppose we wanted to create an app to predict rainfall. We could use either a traditional approach or an ML approach. Using a traditional approach, we'd create a physics-based representation of the Earth's atmosphere and surface, computing massive amounts of fluid dynamics equations. This is incredibly difficult.

## Types of ML Systems

### Supervised learning

Training a model from features and their corresponding labels.

[Supervised learning](https://developers.google.com/machine-learning/glossary#supervised-machine-learning) models can make predictions after seeing lots of data with the correct answers and then discovering the connections between the elements in the data that produce the correct answers. These ML systems are "supervised" in the sense that a human gives the ML system data with the known correct results.

Two of the most common use cases for supervised learning are regression and classification.

#### Regression

A [regression model](https://developers.google.com/machine-learning/glossary#regression-model) predicts a numeric value. 

Informally, a model that generates a numerical prediction. 

#### Classification

[Classification models](https://developers.google.com/machine-learning/glossary#classification-model) predict the likelihood that something belongs to a category. Unlike regression models, whose output is a number, classification models output a value that states whether or not something belongs to a particular category. For example, classification models are used to predict if an email is spam or if a photo contains a cat.

Classification models are divided into two groups: binary classification and multiclass classification. Binary classification models output a value from a class that contains only two values, for example, a model that outputs either `rain` or `no rain`. Multiclass classification models output a value from a class that contains more than two values, for example, a model that can output either `rain`, `hail`, `snow`, or `sleet`.

#### Foundational supervised learning concepts

1. Data
1. Model
1. Training
1. Evaluating
1. Inference

##### Data

Data is the driving force of ML. Data comes in the form of words and numbers stored in tables, or as the values of pixels and waveforms captured in images and audio files. We store related data in datasets. For example.

A dataset is characterized by its size and diversity. Size indicates the number of examples. Diversity indicates the range those examples cover. Good datasets are both large and highly diverse.

A dataset can also be characterized by the number of its features. For example, some weather datasets might contain hundreds of features, ranging from satellite imagery to cloud coverage values. Other datasets might contain only three or four features, like humidity, atmospheric pressure, and temperature. Datasets with more features can help a model discover additional patterns and make better predictions. However, datasets with more features don't *always* produce models that make better predictions because some features might have no causal relationship to the label.

##### Model

In supervised learning, a model is the complex collection of numbers that define the mathematical relationship from specific input feature patterns to specific output label values. The model discovers these patterns through training.

##### Training

Before a supervised model can make predictions, it must be trained. To train a model, we give the model a dataset with labeled examples. The model's goal is to work out the best solution for predicting the labels from the features. The model finds the best solution by comparing its predicted value to the label's actual value. Based on the difference between the predicted and actual values—defined as the [loss](https://developers.google.com/machine-learning/glossary#loss)—the model gradually updates its solution. In other words, the model learns the mathematical relationship between the features and the label so that it can make the best predictions on unseen data.

##### Evaluating

We evaluate a trained model to determine how well it learned. When we evaluate a model, we use a labeled dataset, but we only give the model the dataset's features. We then compare the model's predictions to the label's true values. Depending on the model's predictions, we might do more training and evaluating before deploying the model in a real-world application.



### Unsupervised learning

[Unsupervised learning](https://developers.google.com/machine-learning/glossary#unsupervised-machine-learning) models make predictions by being given data that does not contain any correct answers. An unsupervised learning model's goal is to identify meaningful patterns among the data. In other words, the model has no hints on how to categorize each piece of data, but instead it must infer its own rules.

A commonly used unsupervised learning model employs a technique called [clustering](https://developers.google.com/machine-learning/glossary#clustering). The model finds data points that demarcate natural groupings.

Clustering differs from classification because the categories aren't defined by you. For example, an unsupervised model might cluster a weather dataset based on temperature, revealing segmentations that define the seasons. You might then attempt to name those clusters based on your understanding of the dataset.

### Reinforcement learning

[Reinforcement learning](https://developers.google.com/machine-learning/glossary#reinforcement-learning-rl) models make predictions by getting [rewards](https://developers.google.com/machine-learning/glossary#reward) or penalties based on actions performed within an environment. A reinforcement learning system generates a [policy](https://developers.google.com/machine-learning/glossary#policy) that defines the best strategy for getting the most rewards.

