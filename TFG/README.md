# 🎓 Trabajo Fin de Grado – Reconocimiento de Acciones Humanas mediante Deep Learning

**Autor:** José Burgos Miras  
**Grado en Ingeniería Informática – Universidad de Alicante**  
**Año:** 2024  
**Tutora:** Dra. Ester Martínez Martín

---

## 📘 Descripción

Este trabajo propone un sistema de reconocimiento automático de acciones humanas en vídeo utilizando técnicas de *Deep Learning* y visión por computador. Se evaluaron dos modelos: **ConvLSTM** y **CNN-RNN**, usando secuencias de esqueletos generadas a partir de vídeos RGB procesados con **MediaPipe**.

El objetivo es explorar arquitecturas que permitan reconocer actividades en entornos reales (hogares, seguridad, asistencia) de forma eficiente y con buena capacidad de generalización.

---

## 🔍 Tecnologías utilizadas

- 🧠 TensorFlow 2.x, Keras
- 📦 OpenCV, MediaPipe
- 💻 Python 3.11
- 🧮 ConvLSTM, GRU (CNN-RNN)
- 🎞️ Dataset: [Toyota Smarthome](https://project.inria.fr/toyotasmarthome/)

---

## 🧪 Metodología

1. **Procesamiento de vídeo**
   - Extracción de frames
   - Generación de esqueletos con MediaPipe
   - Normalización y padding

2. **Modelado**
   - ConvLSTM: capturando características espaciotemporales
   - CNN + GRU: extracción espacial + secuencias temporales

3. **Entrenamiento**
   - División estratificada (train/val/test)
   - Variación de batch size, épocas y resolución
   - Uso de técnicas como EarlyStopping y Dropout

---

## 📊 Resultados principales

| Modelo     | Precisión Máxima |
|------------|------------------|
| ConvLSTM   | 67%              |
| CNN-RNN    | 60%              |

- El modelo CNN-RNN demostró mejor **robustez general**.
- ConvLSTM logró picos de precisión más altos con configuraciones óptimas.
- La clase más reconocida fue **Stir**, otras mostraron confusión entre sí (ej. *Cleandishes* vs *Cleanup*).

---

## 📌 Lecciones y futuro trabajo

- 💡 Aplicar arquitecturas como Transformers para mejor comprensión temporal.
- 🗂️ Incrementar diversidad y calidad del dataset.
- ⚙️ Incorporar señales multimodales (audio, depth).
- ⏱️ Optimizar modelos para inferencia en tiempo real.

---

## 📎 Acceso al documento

📄 [Ver TFG completo en PDF](./TFG_BurgosMiras.pdf)

---

> *“El Deep Learning no solo aprende datos. Aprende cómo ver el mundo.”*
