A decision tree is a type of supervised machine learning use to categorize and make predictions based on how previous questions were answered


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
takae instances about a restaurant and product a binary output whether to go or not

A decision tree is a tree like strucutre where each node represents an attribute or a question, and the eadges represent the possible values or answers<br>

![image](https://github.com/Swiftal13/Machine-Learning/assets/76588047/38065834-e06c-46a2-9264-d8f520e27357)

 This is how you represent the decisions you take towards a specific output
circles are decision nodes<br>
the lines are edges, the specific values, Am I hungry? true or false<br>
Square boxes are actual outputs<br>
This is representation
once you go down the decision tree using a specific instance (inputed values), considering the decision nodes and values, you can determine their class
