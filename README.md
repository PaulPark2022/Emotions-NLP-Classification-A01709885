# EMOTIONS NLP CLASSIFICATION

**Autor:** Paul Park (A01709885)  
**Fecha:** 7 de noviembre de 2025  

## 🧠 Descripción general
Este proyecto implementa un modelo de *deep learning* para la **clasificación de emociones en texto**, aplicando una arquitectura de **red LSTM bidireccional** en TensorFlow/Keras.  

El objetivo es que el modelo identifique la emoción dominante en una oración en inglés, entre seis posibles categorías:
**joy, sadness, anger, fear, love, surprise**.

---

## 📂 Estructura del repositorio
| Archivo | Descripción |
|----------|--------------|
| `Emotions_Training.ipynb` | Entrena el modelo desde cero. Descarga el dataset, preprocesa, entrena, evalúa y guarda el modelo entrenado. |
| `Emotions_Prediction.ipynb` | Carga el modelo ya entrenado y permite hacer predicciones inmediatas sobre nuevos textos. |
| `train.txt`, `val.txt`, `test.txt` | Archivos de datos con frases y sus etiquetas emocionales separadas por punto y coma. |
| `emotion_model.h5` | Modelo LSTM bidireccional entrenado y guardado. |
| `tokenizer.pkl`, `label_encoder.pkl` | Objetos serializados necesarios para el preprocesamiento y decodificación. |

---

## 🧩 Arquitectura de la red
- **Capa de Embedding** (dimensión 128)
- **LSTM bidireccional** (128 unidades)
- **Dropout** (0.6 y 0.4 para regularización)
- **Capa densa** (64 unidades ReLU)
- **Capa de salida Softmax** (6 clases)
- **Optimizador:** Adam  
- **Pérdida:** Sparse Categorical Crossentropy  
- **Métrica:** Accuracy

---

## 🚀 Resultados
- Precisión en el conjunto de prueba: **≈ 90 %**
- Buen equilibrio entre *accuracy* y *loss*  
- Las clases más fácilmente distinguibles fueron **joy** y **sadness**.  
- Clases con mayor confusión: **love** y **surprise**, debido a su ambigüedad semántica.

---

## ⚙️ Instrucciones de uso

### 🧠 Entrenamiento (opcional)
Si deseas volver a entrenar el modelo desde cero:
1. Abre `Emotions_Training.ipynb` en Google Colab.  
2. Ejecuta todas las celdas (toma ~15 minutos).  
3. Se generarán los archivos:
   - `emotion_model.h5`
   - `tokenizer.pkl`
   - `label_encoder.pkl`

### ⚡ Predicción (demostración rápida)
1. Abre `Emotions_Prediction.ipynb`.  
2. Asegúrate de tener los archivos `.h5` y `.pkl` en la misma carpeta.  
3. Ejecuta todo el notebook.  
4. Prueba con tus propias frases:
   ```python
   predict_emotion("I'm feeling nervous about tomorrow.")

## 🧾 Documentación técnica

Los experimentos y métricas de desempeño (curvas de accuracy/loss y reportes de clasificación) se encuentran en el notebook
Emotions_Training.ipynb.
Muestra tanto los resultados visuales como textuales, junto con una comparación entre el modelo base y el modelo mejorado.

## 🧩 Mejoras implementadas

- Incremento de dimensión en embeddings (64 → 128)
- Más unidades LSTM (64 → 128)
- Nuevas capas de Dropout para regularización
- Uso de EarlyStopping
- Separación de entrenamiento y predicción en Colabs distintos para mayor eficiencia

## 🔮 Futuras mejoras

- Uso de embeddings preentrenados (GloVe, Word2Vec)
- Integración de modelos basados en Transformers (BERT)
- Expansión del dataset con ejemplos multilingües
- Despliegue del modelo en una API o interfaz web interactiva
