# Final
## Configuration instructions
### I used Voting
1. KNN
```python
knn = KNeighborsClassifier(n_neighbors=1)
```
2. SVM
```python
svc = Pipeline([
    ('pca', PCA(n_components=800)),
    ('MM', MinMaxScaler()),
    ('svm', SVC(C=100, kernel='rbf', degree=2, gamma=50,probability=True, random_state=42))
])
```


3. Voting
```python
from sklearn.ensemble import VotingClassifier
vote = VotingClassifier(estimators=[
                                    ('KNN1',knn_clf1),
                                    ('SVC1',svc_clf1)
                                   ])
```

## Copyright and licensing information
- MIT License


## Contact information
- Name: 
- Student ID: 
- E-mail: 
