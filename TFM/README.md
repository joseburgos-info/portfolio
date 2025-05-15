# 🧠 Trabajo Fin de Máster – Prevención de Suplantación Facial mediante GANs y Detección de Profundidad

**Autor:** José Burgos Miras  
**Máster Universitario en Ciberseguridad – Universidad de Alicante**  
**Año:** 2025  
**Tutora:** Dra. Ester Martínez Martín

---

## 🛡️ Descripción general

Este Trabajo Fin de Máster aborda la detección de ataques por suplantación facial (presentation attacks) combinando dos líneas de defensa:

1. **Generación y discriminación de imágenes sintéticas con GANs**.
2. **Análisis estructural a través de mapas de profundidad generados por MiDaS**.

El objetivo es reforzar los sistemas biométricos de reconocimiento facial ante intentos de suplantación mediante impresiones físicas o deepfakes.

---

## 🧪 Tecnologías y herramientas

- `Python` · `TensorFlow` · `PyTorch`
- `OpenCV`, `NumPy`, `Matplotlib`
- `MiDaS` (Intel, DPT-Large)
- `FER2013`, `MNIST`, `Kaggle print-attack dataset`
- Entrenamiento en entorno remoto con GPU (SSH, Conda, SCP)

---

## 🧠 Componentes del sistema

### 🔁 1. Generación de Rostros con GANs

- Entrenamiento progresivo sobre tres datasets (MNIST, rostros impresos, FER2013).
- Modelos evaluados por resolución y calidad visual.
- Scripts: `gan2.py`, `gan3.py`, `gan4.py`.

### 🌊 2. Análisis de Profundidad con MiDaS

- Detección de diferencias estructurales entre imágenes reales y fotocopias.
- Extracción de región facial (ROI), métricas de textura y profundidad.
- Visualización de histogramas y mapas de calor.
- Scripts: `run_midas.py`, `analyze.py`, `imageDepthAnalyzer.py`.

---

## 📈 Resultados destacados

| Enfoque | Métrica clave | Resultado |
|--------|----------------|-----------|
| GANs (discriminador) | Precisión inicial | +90% (pero caída por sobreajuste) |
| GANs (generador) | Calidad visual | Mejora progresiva hasta epoch 900 |
| MiDaS | Textura (Laplaciano) | >50% más baja en imágenes falsas |
| MiDaS | Desviación estándar | Diferencias sistemáticas por clase |

---

## 🧩 Limitaciones y mejoras

- ⚠️ El discriminador GAN mostró **sobreajuste** con datos no vistos.
- ⚠️ MiDaS sensible a condiciones de iluminación y resolución.
- 💡 Propuesta futura: integración híbrida GAN + profundidad + interfaz de usuario.

---

## 📎 Acceso al documento

📄 [Ver TFM completo en PDF](./TFM_JoseBurgos.pdf)

---

> *“Una sola vulnerabilidad es todo lo que un atacante necesita.” – Window Snyder*
