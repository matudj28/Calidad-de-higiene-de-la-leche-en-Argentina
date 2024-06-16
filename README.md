# Calidad de Higiene

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

#Descripcion y origenes:

Este proyecto tiene como objetivo desarrollar un modelo de predicción basado en cuatro archivos CSV para estimar la calidad de higiene de la leche cruda en Argentina. Los conjuntos de datos fueron obtenidos de la página "datos.gob.ar". Dos fuentes principales de datos son "Lácteos - Calidad higiénico sanitaria de la leche cruda a nivel provincial" y "Lácteos - Calidad higiénico sanitaria de la leche cruda a nivel nacional", adquiridos el 2/6/2024. La razón de tener dos conjuntos de datos por cada nivel es debido al registro de las células, donde hay un registro en cada CSV.

#Los conjuntos de datos se componen de la siguiente manera:

El conjunto a nivel provincial tiene 9 columnas: "indice tiempo" (string), "pais id" (int), "pais" (string), "producto id" (int), "producto" (string), "unidad de medida" (string), "cantidad" (int), "provincia id" (int), "provincia" (string), con un total de 766 instancias.
El conjunto a nivel nacional tiene 7 columnas, las mismas que el conjunto provincial pero sin las columnas "provincia id" ni "provincia", y cuenta con un total de 150 instancias.

#Columnas relevantes:

Las columnas más relevantes para este proyecto son "indice tiempo", "cantidad" y "provincia". 

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for {{ cookiecutter.module_name }}
│                         and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── {{ cookiecutter.module_name }}                <- Source code for use in this project.
    │
    ├── __init__.py    <- Makes {{ cookiecutter.module_name }} a Python module
    │
    ├── data           <- Scripts to download or generate data
    │   └── make_dataset.py
    │
    ├── features       <- Scripts to turn raw data into features for modeling
    │   └── build_features.py
    │
    ├── models         <- Scripts to train models and then use trained models to make
    │   │                 predictions
    │   ├── predict_model.py
    │   └── train_model.py
    │
    └── visualization  <- Scripts to create exploratory and results oriented visualizations
        └── visualize.py
```

--------

