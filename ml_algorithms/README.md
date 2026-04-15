# Algoritmos de ML desde cero

Cada algoritmo está implementado en Python puro — sin sklearn.
El objetivo es entender la matemática, no solo llamar `.fit()`.

| Archivo | Algoritmo | Tipo |
|---|---|---|
| `linear_regression.py` | Regresión Lineal | Regresión |
| `logistic_regression.py` | Regresión Logística | Clasificación |
| `decision_tree.py` | Árbol de Decisión | Clasificación/Regresión |
| `knn.py` | K-Nearest Neighbors | Clasificación/Regresión |
| `k_means.py` | K-Means | Clustering |
| `naive_bayes.py` | Naive Bayes | Clasificación |

## evaluation/
Métricas y validación de modelos.

| Archivo | Contenido |
|---|---|
| `metrics_classification.py` | Accuracy, Precision, Recall, F1, ROC-AUC |
| `metrics_regression.py` | MAE, MSE, RMSE, R² |
| `cross_validation.py` | K-Fold, Stratified K-Fold, Leave-One-Out |
| `bias_variance.py` | Tradeoff, underfitting, overfitting |

**Preguntas frecuentes:**
- ¿Cuándo usar Precision vs Recall?
- ¿Qué es el ROC-AUC?
- ¿Por qué usar cross-validation?
- ¿Cómo detectas overfitting?
