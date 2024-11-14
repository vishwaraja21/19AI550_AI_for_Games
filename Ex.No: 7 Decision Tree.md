# Ex.No: 7 Implementation of Decision Tree Learning 
#### DATE:20-09-2024
#### REGISTER NUMBER : 2122212220060
### AIM:

Design a decision tree for following data. 

Healthy, In Cover, With Ammo -> Attack

Hurt, In Cover, With Ammo -> Attack

Healthy, In Cover, Empty -> Defend

Hurt, In Cover, Empty -> Defend

Hurt, Exposed, With Ammo -> Defend

### ALGORITHM :

1. Start the program
   
2. import the necessary packages
   
3. Design a training data and test data
   
4. Create a decision tree classifier model
   
5. Output the predictions
     
6. Visualize the decision tree

### PROGRAM:

```python
from sklearn import tree
import pandas as pd

# Data: [Health, Cover, Ammo, Exposed]
# Health: 1 for Healthy, 0 for Hurt
# Cover: 1 for In Cover, 0 for Exposed
# Ammo: 1 for With Ammo, 0 for Empty
# Exposed: 1 for Exposed, 0 for In Cover
# Actions: 0 for Defend, 1 for Attack

# Define the training data and corresponding labels (actions)
data = [
    [1, 1, 1],  # Healthy, In Cover, With Ammo -> Attack
    [0, 1, 1],  # Hurt, In Cover, With Ammo -> Attack
    [1, 1, 0],  # Healthy, In Cover, Empty -> Defend
    [0, 1, 0],  # Hurt, In Cover, Empty -> Defend
    [0, 0, 1],  # Hurt, Exposed, With Ammo -> Defend
]

# Labels: 1 for Attack, 0 for Defend
labels = [1, 1, 0, 0, 0]

# Create a Decision Tree Classifier model
clf = DecisionTreeClassifier(criterion="entropy")

# Train the model
clf.fit(data, labels)

# Make predictions (example data points)
test_data = [
    [1, 1, 1],  # Healthy, In Cover, With Ammo
    [0, 0, 1],  # Hurt, Exposed, With Ammo
    [1, 1, 0],  # Healthy, In Cover, Empty
]

# Predict actions for the test data
predictions = clf.predict(test_data)

# Output the predictions
for i, pred in enumerate(predictions):
    action = "Attack" if pred == 1 else "Defend"
    print(f"Test case {i+1}: Predicted action is {action}")

# Optional: Visualize the decision tree
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 6))
tree.plot_tree(clf, feature_names=['Health', 'Cover', 'Ammo', 'Exposed'], class_names=['Defend', 'Attack'], filled=True)
plt.show()

```
### OUTPUT:

![image](https://github.com/user-attachments/assets/dc19cf35-1fc1-4e2b-8365-0d4b9676b6cf)

### RESULT:
Thus the optimum value of max player was found using minimax search.
