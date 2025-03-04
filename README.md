# 🚗 Estimación de Precios de Vehículos

## 📌 Descripción del Proyecto
Este proyecto tiene como objetivo analizar las características de distintos vehículos para estimar sus precios. Utiliza un conjunto de datos de una página web de venta de automóviles y compara el desempeño de cuatro modelos de Machine Learning en la predicción de precios.

## 📊 Modelos Evaluados
Se entrenaron y compararon los siguientes modelos:
- **Regresión Lineal**
- **Árbol de Decisión (Decision Tree)**
- **Bosque Aleatorio (Random Forest)**
- **LightGBM**

## 🔍 Análisis y Comparación
Los modelos fueron entrenados inicialmente con **datos sin escalar**, obteniendo los siguientes resultados:
- La **Regresión Lineal** obtuvo un **RMSE superior a 3000**, el peor desempeño.
- **Árbol de Decisión y Bosque Aleatorio** tuvieron un **RMSE cercano a 2000**.
- **LightGBM** fue el mejor modelo con un **RMSE de aproximadamente 1700**.

Para mejorar el desempeño, en una versión más reciente del proyecto **se escalaron los datos antes del entrenamiento**. Esto tuvo los siguientes efectos:
- **Regresión Lineal, Árbol de Decisión y Random Forest mejoraron significativamente**, con RMSE por debajo de **1.0**.
- **LightGBM, en cambio, mostró un peor rendimiento con datos escalados**, manteniendo un RMSE de **1665** incluso con ajuste de hiperparámetros.

Ajustando parámetros como `learning_rate = 0.08`, el modelo de LightGBM mejoró ligeramente en unos **20 puntos de RMSE**, pero siguió por detrás de los otros modelos en precisión y velocidad.

## 📌 Conclusión
- Si se busca **priorizar la velocidad**, el mejor modelo es **Regresión Lineal**.
- Si se desea **maximizar la precisión**, **Random Forest** es la mejor opción.
- **LightGBM**, a pesar de ser un modelo avanzado, no logró superar a las opciones más simples en este conjunto de datos.

Este análisis demuestra que **modelos más complejos no siempre son la mejor opción** y que la **preparación de los datos** tiene un impacto significativo en el rendimiento del modelo.

## 📂 Contenido del Proyecto
- 📄 `notebooks/` → Contiene el código en **Jupyter Notebook**.
- 📊 `data/` → Conjunto de datos utilizado para entrenar los modelos.
- 📜 `README.md` → Este archivo con la descripción del proyecto.

## 🚀 Cómo Usar el Proyecto
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/Scarleth6o6/prices_prediction.git
   ```
2. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecutar el notebook en Jupyter Notebook o Google Colab.

---
📌 **Autor:** Scarleth San Martin  
📅 **Última actualización:** Marzo 2025
