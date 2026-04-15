# ML Interview Prep 🤖
### by Demian Romero Bautista - ISC - ESCOM

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![License](https://img.shields.io/badge/license-MIT-green)
![Tests](https://github.com/DemianRom/applied-ml-portfolio/actions/workflows/tests.yml/badge.svg)

---

## ¿Por qué existe este repo?

Soy Demian Romero Bautista, estudiante de Ingeniería en Sistemas Computacionales en el IPN — ESCOM, especializándome en Inteligencia Artificial, Ciencia de Datos y su análisis. Construí este repositorio para estructurar mi preparación hacia entrevistas técnicas de forma seria y documentada. Cada solución incluye mi proceso de pensamiento, análisis de complejidad y casos borde — no es un dump de respuestas, es un registro de cómo aprendo y resuelvo problemas.

El enfoque está en tres cosas:

1. **Fundamentos matemáticos** — estadística y probabilidad implementadas desde cero
2. **Algoritmos de ML** — cada modelo escrito en Python puro antes de usar librerías
3. **Proyectos completos** — datasets reales de inicio a fin en `case_studies/`

---

## Estructura

```
ml-interview-prep/
├── dsa/                # Fundamentos esenciales para roles de datos
├── statistics/         # Base matemática: estadística y probabilidad
├── eda/                # Análisis exploratorio de datos
├── ml_algorithms/      # Algoritmos implementados desde cero
│   └── evaluation/     # Métricas y validación de modelos
├── numpy_pandas/       # Herramientas de análisis
├── sql/                # Queries para análisis de datos
│   └── interview_problems/
├── sklearn_applied/    # ML aplicado con Scikit-learn
├── case_studies/       # Proyectos completos con datasets reales
├── deep_learning/      # Fundamentos (en progreso)
├── resources/          # Cheatsheets y referencia rápida
├── tests/              # Tests con pytest
├── template.py         # Formato estándar para cada solución
└── PROGRESS.md         # Tracker de avance
```

---

## Algoritmos de ML implementados desde cero

| Algoritmo | Archivo | Tests |
|---|---|---|
| Linear Regression | [`ml_algorithms/linear_regression.py`](ml_algorithms/linear_regression.py) | |
| Logistic Regression | [`ml_algorithms/logistic_regression.py`](ml_algorithms/logistic_regression.py) | |
| Decision Tree | [`ml_algorithms/decision_tree.py`](ml_algorithms/decision_tree.py) | |
| KNN | [`ml_algorithms/knn.py`](ml_algorithms/knn.py) | |
| K-Means | [`ml_algorithms/k_means.py`](ml_algorithms/k_means.py) | |
| Naive Bayes | [`ml_algorithms/naive_bayes.py`](ml_algorithms/naive_bayes.py) | |

---

## Evaluación de modelos

| Módulo | Archivo |
|---|---|
| Métricas clasificación | [`ml_algorithms/evaluation/metrics_classification.py`](ml_algorithms/evaluation/metrics_classification.py) |
| Métricas regresión | [`ml_algorithms/evaluation/metrics_regression.py`](ml_algorithms/evaluation/metrics_regression.py) |
| Cross-validation | [`ml_algorithms/evaluation/cross_validation.py`](ml_algorithms/evaluation/cross_validation.py) |
| Bias-Variance | [`ml_algorithms/evaluation/bias_variance.py`](ml_algorithms/evaluation/bias_variance.py) |

---

## Case Studies

| Proyecto | Tipo | Archivo |
|---|---|---|
| House Prices | Regresión | [`case_studies/01_house_prices/`](case_studies/01_house_prices/) |
| Titanic | Clasificación | [`case_studies/02_titanic/`](case_studies/02_titanic/) |
| Customer Segmentation | Clustering | [`case_studies/03_customer_segmentation/`](case_studies/03_customer_segmentation/) |

---

## DSA esencial para roles de datos

| Tema | Archivo |
|---|---|
| Arrays y Hashing | [`dsa/arrays_hashing.py`](dsa/arrays_hashing.py) |
| Sorting | [`dsa/sorting.py`](dsa/sorting.py) |
| Binary Search | [`dsa/binary_search.py`](dsa/binary_search.py) |
| Recursión | [`dsa/recursion.py`](dsa/recursion.py) |

---

## Correr los tests

```bash
pip install -r requirements.txt
pytest
pytest -v
pytest tests/test_linear_regression.py
```

---

## Recursos

- [ML Concepts Cheatsheet](resources/cheatsheets/ml_concepts.md)
- [SQL Cheatsheet](resources/cheatsheets/sql_cheatsheet.md)
- [Python tricks para entrevistas](resources/cheatsheets/python_tricks.md)
- [Big-O](resources/cheatsheets/big_o.md)
- [Complejidades por estructura](resources/complexity.md)
