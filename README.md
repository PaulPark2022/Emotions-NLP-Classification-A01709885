# Emotions NLP Classification
**Autor:** Paul Park  
**Curso:** Aprendizaje e IA  
**Descripción:**  
Este proyecto implementa un modelo de deep learning (LSTM bidireccional) para clasificar emociones en texto (alegría, tristeza, enojo, miedo, amor y sorpresa).  

**Framework:** TensorFlow / Keras  
**Dataset:** Textos etiquetados con emociones (train/val/test)  

**Estructura del repo:**
- `train.txt`, `val.txt`, `test.txt` → conjuntos de datos  
- `emotions_NLP_classification.ipynb` → notebook de implementación  
- `README.md` → documentación  

**Resultados:**
- Modelo base: 90% de accuracy en test  
- Modelo mejorado: ~91–93% (según ejecución)  
- Técnicas aplicadas: tokenización, padding, embedding, LSTM bidireccional, dropout, early stopping.  

**Ejemplo de uso:**
```python
predict_emotion("I feel so happy today!")  # joy
