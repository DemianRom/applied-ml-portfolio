# Python tricks para entrevistas de ML/datos

## Collections
```python
from collections import Counter, defaultdict, deque

Counter("banana")           # {'a': 3, 'n': 2, 'b': 1}
Counter.most_common(2)      # top 2 más frecuentes

d = defaultdict(list)       # no KeyError al acceder
d["key"].append(1)

q = deque([1,2,3])
q.appendleft(0)             # O(1) por ambos lados
q.popleft()
```

## NumPy esencial
```python
import numpy as np

np.zeros((3,3))
np.ones((3,3))
np.eye(3)                   # matriz identidad
np.dot(A, B)                # producto matricial
np.linalg.inv(A)            # inversa
np.linalg.norm(v)           # norma euclidiana

a = np.array([1,2,3,4])
a[a > 2]                    # boolean indexing → [3, 4]
a.reshape(2, 2)
```

## Pandas esencial
```python
import pandas as pd

df.describe()
df.isnull().sum()
df.dropna()
df.fillna(df.mean())
df.groupby("col").agg({"val": "mean"})
df.sort_values("col", ascending=False)
df.merge(df2, on="id", how="left")
df.pivot_table(values="val", index="a", columns="b")
pd.get_dummies(df["cat_col"])
```

## Sklearn pipeline
```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression

pipe = Pipeline([
    ("scaler", StandardScaler()),
    ("model", LogisticRegression())
])
pipe.fit(X_train, y_train)
pipe.score(X_test, y_test)
```

## Bisect (binary search en listas ordenadas)
```python
import bisect
bisect.bisect_left([1,3,5,7], 5)   # → 2
bisect.insort(lst, val)             # inserta manteniendo orden
```
