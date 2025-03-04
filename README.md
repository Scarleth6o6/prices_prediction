# 🚗 Estimación de Precios de Vehículos
Este proyecto tiene como objetivo procesar las características de distintos vehículos para realizar análisis y estimar sus precios basados en la información de una base de datos proporcionada por una página web de venta de vehículos.

A través de este proyecto, se entrenan y comparan los resultados de cuatro modelos de Machine Learning para determinar cuál de ellos ofrece la mejor estimación de los precios.
## 📌 Descripción
El conjunto de datos utilizado incluye diversas características de vehículos, como:

- ✅ Marca
- ✅ Modelo
- ✅ Año
- ✅ Kilometraje
- ✅ Tipo de combustible
- ✅ Color
- ✅ Y más…

A partir de estos datos, se busca predecir el precio de los vehículos en base a sus características.

Los modelos entrenados y evaluados son:

- 🔹 Regresión Lineal
- 🔹 Árbol de Decisión
- 🔹 Bosque Aleatorio
- 🔹 LightGBM

Cada modelo es evaluado utilizando la métrica RECM (Raíz del Error Cuadrático Medio) y se comparan en términos de precisión y tiempo de ejecución.

## 📌 Datos Escalados vs. No Escalados
Inicialmente, los modelos fueron entrenados con datos sin escalar, obteniendo los siguientes resultados:

Regresión Lineal: RECM superior a 3000.
Árbol de Decisión y Bosque Aleatorio: RECM cercano a 2000.
LightGBM: Mejor desempeño con un RECM de ~1700.
Luego, se decidió escalar los datos, lo que mejoró notablemente el desempeño de los modelos de Regresión Lineal, Árbol de Decisión y Bosque Aleatorio. Sin embargo, LightGBM tuvo un mejor rendimiento con los datos sin escalar.

## 📌 Tecnologías y Herramientas
Este proyecto utiliza las siguientes herramientas:

- 🖥 Jupyter Notebook (Todo el código se encuentra en estimacion_precios.ipynb).
- 🐍 Python 3.x
- 📊 Pandas y NumPy (Manipulación de datos).
- 🤖 Scikit-learn (Modelos de Machine Learning).
- ⚡ LightGBM (Modelo basado en potenciación del gradiente).
- 📉 Matplotlib y Seaborn (Visualización de datos).

## 📂 Contenido del Proyecto
- 📄 `notebooks/` → Contiene el código en **Jupyter Notebook**.
- 📊 `data/` → Conjunto de datos utilizado para entrenar los modelos.
- 📜 `README.md` → Este archivo con la descripción del proyecto.

## 🚀 Cómo Usar el Proyecto
1️⃣ Clonar el repositorio:
   ```bash
   git clone https://github.com/Scarleth6o6/prices_prediction.git
   ```
2️⃣ Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
3️⃣ Ejecutar el notebook en Jupyter Notebook o Google Colab.
   ```bash
   jupyter notebook
   ```
4️⃣ Abre el archivo estimacion_precios.ipynb y ejecuta las celdas.

📌 Análisis de Resultados
Los modelos fueron evaluados en función de RECM (Raíz del Error Cuadrático Medio) y tiempo de ejecución.

- 🔹 Regresión Lineal: Modelo más rápido, pero con una menor precisión.
- 🔹 Árbol de Decisión y Bosque Aleatorio: Buena precisión, pero mayor tiempo de entrenamiento.
- 🔹 LightGBM: No mostró mejoras significativas y su desempeño fue mejor sin escalar los datos.

## 📌 Conclusión
Este proyecto demuestra que, aunque modelos avanzados como LightGBM pueden ser potentes, los modelos más simples como Regresión Lineal y Random Forest pueden ofrecer resultados competitivos dependiendo del balance entre precisión y velocidad de entrenamiento.

Si se prioriza la velocidad, Regresión Lineal es la mejor opción.
Si se busca precisión, Random Forest tiene mejor desempeño.

## 📌 Mejoras Futuras
🚀 Evaluar otros modelos como XGBoost o SVM.
🚀 Realizar un análisis de importancia de características.
🚀 Implementar validación cruzada para mejorar la evaluación de los modelos.

## 📌 Contribuciones
Si deseas contribuir a este proyecto:

- 1️⃣ Haz un fork del repositorio.
- 2️⃣ Crea una nueva rama (git checkout -b feature/nueva-caracteristica).
- 3️⃣ Realiza tus cambios y haz commit (git commit -am "Añadir nueva característica").
- 4️⃣ Haz push a la rama (git push origin feature/nueva-caracteristica).
- 5️⃣ Abre un Pull Request.
- 📅 **Última actualización:** Marzo 2025
