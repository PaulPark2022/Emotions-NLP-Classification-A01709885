# EMOTIONS NLP CLASSIFICATION 🎭

**Autor:** Paul Park (A01709885)  
**Curso:** Inteligencia artificial avanzada para la ciencia de datos II  
**Fecha:** 7 de noviembre de 2025  

---

## 📖 Descripción
Implementación de un modelo de *Deep Learning* para la **clasificación de emociones en texto**, utilizando una red **LSTM bidireccional** con técnicas de regularización.  
El proyecto entrena un modelo capaz de identificar la emoción dominante en frases cortas en inglés.

Emociones detectadas:  
**joy, sadness, anger, fear, love, surprise**

---

## 🧩 Arquitectura y framework
- **Framework:** TensorFlow / Keras  
- **Modelo Base:** Embedding (64) + LSTM(64) + Dropout  
- **Modelo Mejorado:** Embedding (128) + LSTM(128) + Dense(64 ReLU) + Dropout + EarlyStopping  
- **Pérdida:** Sparse Categorical Crossentropy  
- **Optimizador:** Adam  
- **Métrica:** Accuracy  

---

## 🧠 Resultados
| Modelo | Test Accuracy | Observaciones |
|--------|----------------|----------------|
| Base | 0.88 | Buen desempeño inicial, sin sobreajuste significativo |
| Mejorado | 0.90 | Mayor estabilidad y menor pérdida en validación |

El modelo mejorado logra un equilibrio sólido entre capacidad y generalización, capturando correctamente el tono emocional de frases cortas.

---

## ⚙️ Archivos del proyecto
| Archivo | Descripción |
|----------|--------------|
| `Emotions_Training.ipynb` | Entrena y compara modelo base y mejorado, genera métricas y guarda el modelo final. |
| `Emotions_Prediction.ipynb` | Carga el modelo final y realiza predicciones rápidas en consola. |
| `train.txt`, `val.txt`, `test.txt` | Dataset de texto y etiquetas de emoción. |
| `emotion_model.keras` | Modelo LSTM entrenado (versión mejorada). |
| `tokenizer.pkl`, `label_encoder.pkl` | Objetos de preprocesamiento necesarios para predicciones. |

---

## 🧾 Documentación técnica
- Curvas de *accuracy* y *loss* del entrenamiento.  
- Comparativa entre el modelo base y mejorado.  
- Evaluación cuantitativa y cualitativa en el dataset de prueba.  
- Ejemplos de inferencia incluidos.

---

## 💡 Próximos pasos
- Integrar embeddings preentrenados (GloVe, Word2Vec)  
- Probar modelos basados en Transformers (BERT)  
- Desplegar una interfaz gráfica para usuarios  

---

## 📘 Referencias
Dataset original basado en el *Emotions Dataset for NLP Classification Tasks* (Kaggle).  
Inspirado en los lineamientos del paper *Affect in Tweets* (Mohammad et al., ACL 2018).
