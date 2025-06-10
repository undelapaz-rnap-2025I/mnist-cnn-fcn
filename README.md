## **Comparación entre Redes Neuronales Totalmente Conectadas y Convolucionales con PyTorch sobre MNIST**

---

## Objetivo

Implementar y comparar dos arquitecturas de redes neuronales (FC y CNN) usando PyTorch sobre el conjunto de datos MNIST. Se evaluará su rendimiento en términos de **número de parámetros**, **accuracy**, **AUC** y se aplicará **sintonización de al menos tres hiperparámetros**.

---

## Instrucciones

### 1. Carga y preprocesamiento de datos

Cargar los datos usando `DataLoader` para manejar los lotes (batches) como en la anterior tarea.

---

### 2. 🧠 Definición de modelos

Implementa dos modelos con las siguientes características:

#### Modelo A: Red totalmente conectada (FC)

* Entrada `Flatten` de 28x28 → 784.
* Al menos una capa oculta (ej. 128 neuronas, `ReLU`).
* Capa de salida: 10 neuronas.

#### Modelo B: Red convolucional (CNN)

* 1–2 capas convolucionales (ej. 32 y 64 filtros, kernel 3x3).
* `MaxPool2d` después de cada capa convolucional.
* `Flatten` → `Linear` → 10 neuronas de salida.

---

### 3. Sintonización de hiperparámetros

Seleccionar **al menos tres hiperparámetros** entre:

* Tasa de aprendizaje
* Tamaño del batch
* Número de neuronas o filtros
* Número de capas ocultas
* Dropout
* Kernel size (solo CNN)

Utiliza un método de selección de hiperparámetros. Explica el proceso.

Evaluar usando accuracy en validación o prueba (según lo definido).

### 4. Evaluación

Para cada modelo:

* Calcular **número total de parámetros**.
* Calcular **accuracy** sobre el conjunto de prueba.
* Calcular **AUC macro** (usar `sklearn.metrics.roc_auc_score` con `multi_class='ovo'` o `ovr`).
* Mostrar matriz de confusión (opcional: `seaborn.heatmap` o `sklearn.metrics.confusion_matrix`).
* Graficar curva ROC para todas las clases.

Incluir:

* Gráficas de loss y accuracy por época.
* Curvas ROC.
* Tiempo de entrenamiento.

---

## Entregables

**Notebook** con:

   * Carga de datos
   * Definición de modelos
   * Entrenamiento
   * Sintonización
   * Evaluación
   * Tabla resumen