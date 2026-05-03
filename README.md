# Predicción de Intervención Quirúrgica en Cólico Equino (Metodología CRISP-DM)

Este proyecto aplica la metodología **CRISP-DM** (*Cross-Industry Standard Process for Data Mining*) para predecir si un caballo con cólico requiere cirugía o puede ser tratado médicamente, basándose en indicadores clínicos y fisiológicos.

El análisis utiliza el conjunto de datos **Horse Colic** del repositorio UCI Machine Learning.

## 📊 Descripción del Proyecto

El cólico es una de las principales causas de mortalidad en equinos. Decidir a tiempo si un paciente requiere cirugía es crítico para su supervivencia. Este proyecto busca construir un pipeline de datos robusto que prepare la información clínica para modelos de aprendizaje automático.

### Metodología: CRISP-DM
El desarrollo se estructura en las siguientes fases (actualmente completadas hasta la Fase 3):

1.  **Fase 1: Comprensión del Negocio (Business Understanding):** Definición del problema de clasificación binaria y establecimiento de métricas de éxito.
2.  **Fase 2: Comprensión de los Datos (Data Understanding):** 
    - Análisis exploratorio de datos (EDA).
    - Pruebas de significancia estadística (ANOVA).
    - Validación de supuestos (Normalidad y Homocedasticidad).
    - Análisis de correlación y valores nulos.
3.  **Fase 3: Preparación de los Datos (Data Preparation):**
    - Construcción de `Pipelines` y `ColumnTransformer`.
    - Imputación avanzada de nulos mediante `KNNImputer`.
    - Ingeniería de características (`taquicardia_grave`).
    - Balanceo de clases utilizando **SMOTE**.
    - Reducción de dimensionalidad (PCA y SelectKBest).

## 🛠️ Tecnologías Utilizadas

*   **Lenguaje:** Python 3.x
*   **Librerías Principales:**
    *   `pandas` & `numpy`: Manipulación de datos.
    *   `scikit-learn`: Pipelines, transformaciones y selección de modelos.
    *   `seaborn` & `matplotlib`: Visualización estadística.
    *   `scipy`: Pruebas de hipótesis estadísticas.
    *   `imbalanced-learn`: Balanceo con SMOTE.

## 📁 Estructura del Repositorio

*   `parcial-1.ipynb`: Cuaderno principal con el desarrollo detallado de las fases 1, 2 y 3.
*   `horse-colic.data`: Dataset de entrenamiento original.
*   `horse-colic.test`: Dataset de prueba original.
*   `train_preprocesado_smote.xlsx`: Datos finales listos para la fase de modelado (balanceados).
*   `README.md`: Descripción del proyecto.

## 🚀 Cómo Empezar

1.  **Clonar el repositorio:**
    ```bash
    git clone https://github.com/tu-usuario/horse-colic-crispdm.git
    cd horse-colic-crispdm
    ```

2.  **Instalar dependencias:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn scipy imbalanced-learn openpyxl
    ```

3.  **Ejecutar el Cuaderno:**
    Abre `parcial-1.ipynb` en Jupyter Notebook o Google Colab para ver el proceso paso a paso.

## 📝 Conclusiones de la Preparación
Tras el preprocesamiento, se logró reducir el ruido eliminando variables con más del 30% de nulos y se mitigó el sesgo de la clase mayoritaria, dejando un dataset de 39 características (tras One-Hot Encoding) listo para la fase de entrenamiento de algoritmos de Machine Learning.

---
**Autor:** [Tu Nombre/Usuario]  
**Fecha:** Abril 2026  
**Estado:** Fase 3 Completa - Listo para Modelado.
