# Clustering de Imágenes OCT

Análisis comparativo de algoritmos de clustering en imágenes de Tomografía de Coherencia Óptica (OCT) de retina utilizando embeddings de modelos de deep learning.

## Descripción

Este proyecto aplica técnicas de clustering no supervisado sobre imágenes de cortes de retina de pacientes con diversas patologías y sanos. Se comparan diferentes algoritmos de clustering y modelos de embeddings para identificar patrones y agrupaciones en los datos.

## Modelos de Embeddings

- **ResNet50** (2048 dimensiones)
- **Vision Transformer L16** (ViT-L16)
- **Swin Transformer V2**

## Algoritmos de Clustering

- DBSCAN
- K-Means
- HDBSCAN
- OPTICS
- Gaussian Mixture Models (GMM)
- Agglomerative Clustering

## Técnicas de Reducción de Dimensionalidad

- PCA (Principal Component Analysis)

## Métricas de Evaluación

- Silhouette Score
- Calinski-Harabasz Score
- Davies-Bouldin Score

## Estructura del Proyecto

```
├── APAU_PracticaClusteringOCT.ipynb  # Notebook principal con análisis completo
├── PCA+DBSCAN.ipynb                   # Optimización de PCA + DBSCAN
├── data/
│   ├── embeddings_resnet50.csv        # Embeddings generados con ResNet50 (NO incluido)*
│   ├── embeddings_swinv2.csv          # Embeddings generados con Swin V2 (NO incluido)*
│   ├── embeddings_vitl16.csv          # Embeddings generados con ViT-L16 (NO incluido)*
│   └── images/                        # Imágenes OCT originales (5600 imágenes)
└── README.md
```

**\*Nota:** Los archivos CSV de embeddings (236 MB en total) no están incluidos en este repositorio debido al límite de tamaño de archivo de GitHub (100 MB). Los embeddings fueron generados previamente usando modelos preentrenados y se utilizan directamente en los notebooks.

## Requisitos

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- plotly
- seaborn
- PIL (Pillow)

## Uso

1. Cargar uno de los archivos de embeddings disponibles
2. Aplicar normalización con StandardScaler
3. Reducir dimensionalidad con PCA (opcional)
4. Aplicar el algoritmo de clustering deseado
5. Evaluar resultados con las métricas implementadas
6. Visualizar clusters con gráficos 2D/3D

## Notebooks

- **APAU_PracticaClusteringOCT.ipynb**: Análisis completo incluyendo visualizaciones, comparación de algoritmos y métricas de evaluación.
- **PCA+DBSCAN.ipynb**: Optimización específica de hiperparámetros para la combinación PCA + DBSCAN.

## Autor

Marco López
Proyecto realizado como parte de la asignatura APAU - UPM
