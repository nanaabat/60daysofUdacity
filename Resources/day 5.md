# Differential Privacy For Deep Learning

Perfect Privacy - a query of database returns the same value even if we remove any person from the database 

In the case of deep learning — we replaced “query of database” with “training a model on a dataset”.

**This adds two types of complexities:

```base
- do we always know the people being referenced in the datasets?

- neural networks rarely ever train to the same location even when trained on the same datasets twice.
```

**How can solve this???

```base
- Treating each training example as one seperate person(1st probs)--more info coming up

- Second question answer in next videos....

```
**One thing I got today is that

```base
- DP is more dependant on trust between the two parties(user and trusted curator), the level of trust determines that sort of technique that is being used!
```

# Project Intro Example Scenario Deep Learning In a Hospital

There are times when you want to train a datasets, but there is not enough information(expecially if the datasets are not labelled) to make that happen and so one way to train your datasets is by this process:

Let us take this scenario for example:

Say you want to use data from the hospital to create a neural network but you do not have sufficient information because the dataset is not labelled. What can you do? In order to train your new classifer, you can do so by train on their dataset in order to automatically label your own.

```base
You can reach out to 10 other hospitals which do have annotated data. This will enable you train your new classifer on their datasets so that you can automatically label your own 
```
Just in case these hospitals are concerned with privacy issues then you can use this technique

```base
Ask the hospital to train a model in their dataset
```
```base
Use each model to predict your own local dataset, generating 10 labels for each dataset(now you have labelled data)
```
```base
Then you perform a DP query to generate a final true DP label for each datapoint. This query will be a max function;this will be the most frequent label accross the 10 labels assigned for each individdual image. Then you can add Laplacian noise to make it differentially private to a certain epsilon delta constraint.
```
```base
Then you retrain the new model on your local dataset which now has DP labels
```

# Generating Differentially Private Labels For a Dataset

Practical Explanation of How we can Add labels to our local unlabbeled datasets



