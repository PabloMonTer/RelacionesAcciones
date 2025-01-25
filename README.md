# Relaciones entre Acciones

Este proyecto tiene como objetivo analizar las relaciones y patrones subyacentes en los precios históricos de las acciones de múltiples empresas utilizando técnicas avanzadas de análisis de datos y topología computacional. 

## Metodología
El flujo de trabajo se organiza en varias etapas:

### 1. Obtención de Datos
Los datos utilizados en este proyecto consisten en los precios históricos de las acciones de múltiples empresas. Estos datos fueron obtenidos de fuentes públicas como APIs financieras (Yahoo Finance), que proporcionan series temporales con información diaria sobre el valor de las acciones.

### 2. Reducción de Dimensionalidad con UMAP
El primer paso para tratar con los datos de alta dimensión es aplicar UMAP (Uniform Manifold Approximation and Projection), una técnica de reducción de dimensionalidad. UMAP es particularmente útil para mantener las relaciones locales y globales entre puntos de datos mientras reduce el número de dimensiones, facilitando la visualización y análisis posterior.

UMAP transforma las características originales del conjunto de datos (precios de las acciones a lo largo del tiempo) en un espacio de menor dimensión (generalmente 2D o 3D), lo que permite identificar relaciones entre diferentes empresas de manera más clara.

### 3. Clustering con DBSCAN
Una vez que los datos fueron proyectados en un espacio de menor dimensión usando UMAP, se aplicó el algoritmo de clustering DBSCAN (Density-Based Spatial Clustering of Applications with Noise). DBSCAN es un algoritmo de clustering que agrupa puntos de datos basándose en la densidad de puntos en el espacio. Es ideal para detectar grupos de empresas con comportamientos similares en cuanto a sus precios de acciones.

### 4. Algoritmo Mapper para Analizar Relaciones Topológicas
Después de realizar la reducción de dimensionalidad y el clustering, se utilizó el algoritmo Mapper para crear una representación topológica de los datos, lo que permite observar relaciones y patrones entre las acciones de distintas empresas. Mapper es un algoritmo de topología computacional que, en este contexto, ayuda a visualizar la estructura de relaciones entre los clusters obtenidos con DBSCAN y las empresas analizadas.

- Clusters de empresas similares: DBSCAN identificó empresas cuyos precios de acciones mostraron comportamientos similares a lo largo del tiempo.
- Estructura topológica: Mapper permitió observar cómo las empresas estaban interconectadas en un espacio topológico, ayudando a identificar tendencias y relaciones complejas que no eran obvias a simple vista.
- Además, las visualizaciones generadas por UMAP y Mapper ayudaron a proporcionar una representación clara y comprensible de los datos, destacando las relaciones entre los diferentes grupos de empresas y proporcionando insights sobre posibles movimientos del mercado.
