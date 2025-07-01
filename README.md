# Chest_Cancer_Detection_DeepLearning

Este proyecto presenta el desarrollo de un modelo de clasificación basado en redes neuronales convolucionales (CNN), utilizando TensorFlow y Keras, para detectar signos de cáncer en imágenes tomográficas de tórax. El modelo fue entrenado con un conjunto de imágenes médicas en escala de grises y alcanzó una precisión de **hasta el 98% en validación**, mostrando resultados prometedores para aplicaciones médicas asistidas por inteligencia artificial.

### 🔍 Exploración y Preparación de Datos
- Se utilizó un conjunto de imágenes de tórax en escala de grises divididas en carpetas `train/` y `test/`.
- Las imágenes fueron redimensionadas a **128x128 píxeles** y normalizadas entre **0 y 1**.
- Se utilizó `image_dataset_from_directory` de TensorFlow para cargar y etiquetar automáticamente las imágenes.
---

### ⚙️ Construcción del Modelo
Se implementó una CNN con la siguiente arquitectura:
- Capa `Conv2D` con **32 filtros** y kernel de **3x3**
- `MaxPooling2D`
- `Flatten` y `Dense` con **128 neuronas**
- `Dropout` para evitar overfitting
- Capa de salida con activación **softmax** para clasificación binaria
---

### 🧠 Técnicas Aplicadas
- **Regularización L2** para penalizar pesos grandes
- **Dropout** con tasa de **0.3**
- **EarlyStopping** para evitar sobreentrenamiento
- **ModelCheckpoint** para guardar automáticamente el mejor modelo
---

### 📈 Resultados
- **Precisión en validación:** hasta **98%**
- **Pérdida mínima de validación:** **0.5843**
- Se detectó **overfitting** tras la época 24, y se aplicó `early stopping` correctamente.
---

### 🖼️ Visualizaciones
- Ejemplos de imágenes de entrenamiento con etiquetas
- Gráfico de pérdida (`loss`) vs. épocas
- Matriz de confusión para evaluar predicciones finales
---

### 🔮 Predicción en Nuevas Imágenes
- Se probó el modelo con imágenes nuevas redimensionadas a **128x128** y convertidas a escala de grises, mostrando la predicción de la clase:
0 = sin cáncer
1 = cáncer

- Puedes descargar el modelo entrenado desde el siguiente enlace de One Drive:  
👉 [Descargar modelo mejor_modelo.keras](https://1drv.ms/u/c/7d2c730eba597f09/EZIAqNrFO_tHt4eYCh9mu-EByKP_rMckMRrKBUtSQKC9pg?e=GcAwqI)

