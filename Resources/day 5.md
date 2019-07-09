Differential Privacy For Deep Learning

Perfect Privacy - a query of database returns the same value even if we remove any person from the database 

In the case of deep learning — we replaced “query of database” with “training a model on a dataset”.

This adds two types of complexities:

- do we always know the people being referenced in the datasets?
- neural networks rarely ever train to the same location even when trained on the same datasets twice.

How can solve this???

- Treating each training example as one seperate person(1st probs)--more info coming up
- Second question answer in next videos....

One thing I got today is that
- DP is more dependant on trust between the two parties(user and trusted curator), the level of trust determines that sort of technique that is being used!