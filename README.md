# objetos_salon
# 🧠 Proyecto colaborativo: Reconocimiento de objetos con TensorFlow

Este repositorio forma parte del curso *Redes Convolucionales y Representaciones Latentes (2025)*.

## Objetivo
Construir, entrenar y evaluar un modelo de visión que identifique objetos del entorno grabados por los estudiantes.
## Objetos a detectar
* teclado
* mouse
* pantalla
* cpu
* masa
* silla

## Estructura
- `data/raw/`: videos, cada estudiante hace un video de cada objeto  (entre 1 seg y 3 seg) nombrado f"{codigo}_{objeto}.mp4".
- `data/processed/`: frames extraídos por clase nombrados f"{codigo}_{objeto}_{indice}.jpg".
- `notebooks/`: experimentos y entrenamiento nombrados f"{codigo}.ipynb".
- `models/`: pesos entrenados del autoencoder y clasificador nombrados f"{codigo}_autoencoder.h5" o f"{codigo}_classifier.h5".


## 🚀 Cómo contribuir
1. Haz un fork de este repositorio.
2. Agrega tu video en `data/raw/`.
3. Extrae los frames y colócalos en `data/processed/<tu_objeto>/`.
4. Actualiza esta tabla y haz un Pull Request.

## 🧠 Modelo base
El modelo usa TensorFlow/Keras y se entrena en Google Colab.
