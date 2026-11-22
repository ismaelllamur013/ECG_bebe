# Extracción de ECG Fetal mediante Red Neuronal ADALINE 🫀👶

Proyecto desarrollado en el marco de la materia **Introducción a la Bioingeniería** de la **FACET (Facultad de Ciencias Exactas y Tecnología - UNT)**. El objetivo es aislar y recuperar la señal del electrocardiograma fetal (**fECG**) a partir de registros abdominales no invasivos, eliminando la interferencia dominante del electrocardiograma materno (**mECG**) mediante un filtro adaptativo basado en la red neuronal **ADALINE** (*Adaptive Linear Element*).

## 📋 Fundamento y Problema Biomédico

La monitorización no invasiva de la frecuencia cardíaca y actividad eléctrica fetal se realiza colocando electrodos sobre el abdomen de la madre. Sin embargo, la señal captada es una mezcla donde el latido materno tiene una amplitud considerablemente mayor que el fetal, sumado al ruido muscular y de línea base.

Para resolverlo sin recurrir a métodos invasivos:
* Se toma una **señal de referencia torácica** (donde predomina el ECG materno puro).
* Se toma una **señal abdominal** (mezcla de ECG materno + ECG fetal + ruido).
* La red **ADALINE** aprende de forma adaptativa la función de transferencia entre el tórax y el abdomen materno, estimando la componente materna presente en el abdomen para sustraerla y dejar limpia la señal del **ECG fetal**.

## 📁 Estructura del Repositorio

* **`ADALINE.ipynb`**: Notebook de Python que implementa el preprocesamiento de las señales biomédicas, la arquitectura y entrenamiento de la red neuronal ADALINE (regla de aprendizaje LMS / Widrow-Hoff), la cancelación adaptativa de interferencia materna y la visualización comparativa de las señales (materna, abdominal y fetal recuperada).

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Jupyter Notebook / Google Colaboratory**
* **NumPy**: operaciones vectoriales, cálculo de pesos sinápticos y actualización iterativa del error.
* **SciPy / Pandas**: carga, filtrado y manejo de las series temporales de ECG.
* **Matplotlib**: visualización de señales en el dominio del tiempo y curvas de convergencia del error.

## 🚀 Cómo Ejecutar el Proyecto

1. **Clonar el repositorio:**
   `git clone https://github.com/ismaelllamur013/ECG_bebe.git`
2. **Instalar dependencias:**
   `pip install jupyter numpy scipy pandas matplotlib`
3. **Abrir el notebook:**
   `jupyter notebook ADALINE.ipynb`
4. **Ejecutar las celdas:**
   Corre secuencialmente las celdas del notebook para visualizar las señales originales, el ajuste de hiperparámetros (tasa de aprendizaje y retardo/taps) y la extracción resultante del ECG fetal.

## 🎓 Contexto Académico

* **Institución:** Facultad de Ciencias Exactas y Tecnología (FACET) - Universidad Nacional de Tucumán (UNT)
* **Asignatura:** Introducción a la Bioingeniería
* **Autor:** Ismael Llamur - [@ismaelllamur013](https://github.com/ismaelllamur013)
