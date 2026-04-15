# ML Concepts Cheatsheet

## Bias-Variance Tradeoff

| | Bias alto | Bias bajo |
|---|---|---|
| **Varianza alta** | Imposible en la práctica | Overfitting |
| **Varianza baja** | Underfitting | Ideal |

- **Underfitting:** modelo muy simple, no aprende el patrón
- **Overfitting:** modelo muy complejo, memoriza el ruido

## Métricas de clasificación

```
Precision = TP / (TP + FP)   → de los que dije positivo, ¿cuántos lo eran?
Recall    = TP / (TP + FN)   → de los positivos reales, ¿cuántos detecté?
F1        = 2 * (P * R) / (P + R)
```

**¿Cuándo usar cada una?**
- Precision: cuando el costo de un falso positivo es alto (spam, fraude)
- Recall: cuando el costo de un falso negativo es alto (diagnóstico médico)
- F1: cuando quieres balance entre ambas

## Métricas de regresión

```
MAE  = mean(|y - ŷ|)            → robusto a outliers
MSE  = mean((y - ŷ)²)           → penaliza errores grandes
RMSE = sqrt(MSE)                 → mismas unidades que y
R²   = 1 - SS_res/SS_tot        → % de varianza explicada
```

## Regularización

- **L1 (Lasso):** penaliza suma de |coeficientes| → puede llevar coefs a 0 (feature selection)
- **L2 (Ridge):** penaliza suma de coeficientes² → shrinkage, nunca a 0

## Normalización vs Estandarización

- **Normalización (MinMax):** escala a [0,1] — útil cuando la distribución NO es normal
- **Estandarización (StandardScaler):** media=0, std=1 — útil para la mayoría de algoritmos

## Cuándo usar cada algoritmo

| Algoritmo | Cuándo usarlo |
|---|---|
| Linear Regression | Relación lineal, interpretabilidad importa |
| Logistic Regression | Clasificación binaria, baseline rápido |
| Decision Tree | Interpretabilidad, datos mixtos |
| KNN | Dataset pequeño, sin supuestos sobre distribución |
| K-Means | Clustering cuando sabes cuántos grupos |
| Naive Bayes | Texto, NLP, datasets grandes |
