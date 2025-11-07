# Emotions NLP Classification 🎭

**Autor:** Paul Park (A01709885)  
**Curso:** Inteligencia artificial avanzada para la ciencia de datos II 
**Fecha:** 7 de noviembre de 2025  

## 📖 Descripción
Implementación de un modelo de *deep learning* para la **clasificación de emociones en texto**, usando una red **LSTM bidireccional** entrenada en un dataset real con seis emociones: *joy, sadness, anger, fear, love y surprise*.

## ⚙️ Framework y técnicas
- TensorFlow / Keras  
- Embedding de 10,000 palabras  
- LSTM Bidireccional  
- Dropout y EarlyStopping  
- Comparación entre modelo base y modelo mejorado  

## 🧠 Resultados
| Modelo | Test Accuracy | Observaciones |
|--------|----------------|----------------|
| Base | 0.90 | Buen equilibrio entre bias y varianza |
| Mejorado | 0.90 | Mayor estabilidad y menor val_loss |

El modelo demuestra capacidad para capturar emociones de texto con alta precisión.

## 🧪 Ejemplo de uso
```python
predict_emotion("I feel so happy today!")  # joy
predict_emotion("I'm scared of what might happen next.")  # fear

## 📊 Dataset
train.txt, val.txt, test.txt

Cada línea: texto;etiqueta

Ejemplo:

I am so happy today;joy
I'm afraid of what will happen;fear

## 💡 Próximos pasos

Integrar embeddings preentrenados (GloVe)
Añadir interfaz gráfica sencilla
Experimentar con modelos tipo BERT
