A decision tree is a type of supervised machine learning use to categorize and make predictions based on how previous questions were answered
(USED FOR CLASSIFICATION)


## Classification and Regression
Two fundamental practices in supervised learning

# Classification
Classification, taking inputs and mapping it to a discrete label

**Instances** are inputted data values, discrete<br>
**Concept** is the function that maps the inputs to outputs<br>
**Target** is the answer we are trying to acheive<br>
**Hypothesis class** set of all concepts (classification functions) that you are considering<br>
the set of all possible decision trees<br>
**Sample** training set of  inputs paired with labels (correct output)<br>
**Candidate** is the hypotehtihs or concept that you think is the target concept


## Decision tree
take in instances, produce binary outputs to decide

A decision tree is a tree like strucutre where each node represents an attribute or a question, and the eadges represent the possible values or answers<br>

![image](https://github.com/Swiftal13/Machine-Learning/assets/76588047/38065834-e06c-46a2-9264-d8f520e27357)

 This is how you represent the decisions you take towards a specific output
circles are decision nodes<br>
the lines are edges, the specific values, Am I hungry? true or false<br>
Square boxes are actual outputs<br>
This is representation
once you go down the decision tree using a specific instance (inputed values), considering the decision nodes and values, you can determine their class

# Building a decision tree
pick the best attribute, which splits it in half

In decision trees, the "best attribute" refers to the feature or attribute that is most informative in splitting the data into different classes or categories. It is the attribute that provides the most significant reduction in uncertainty or impurity when used as a decision criterion.

# Boolean expressionism in Decision trees

![image](https://github.com/Swiftal13/Machine-Learning/assets/76588047/c5d5c24b-c625-48c0-8d5a-54535a6583e8)
<br>Decision trees can represent boolean functions. These take in a **binary input and produce a binary output**<br>
For example A **and** B. Both A and B must be true, for the expression to be True

A **Or** B
![image](https://github.com/Swiftal13/Machine-Learning/assets/76588047/ede4be37-0003-4922-92cf-ca2a3912b637)

A **XOR** B
XOR = exclusive OR
Alot of times in real life when you say Or you mean XOR, only one, in truth gates OR includes both to be true aswell


