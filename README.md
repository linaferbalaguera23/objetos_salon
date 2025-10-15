# objetos_salon
## Proyecto colaborativo: Reconocimiento de objetos con TensorFlow

* Este repositorio forma parte del módulo de **Redes Convolucionales** 2025-3
* En el curso **BigData**
* Impartido por Gerardo Muñoz

---

## Objetivo
Construir, entrenar y evaluar un modelo de visión que identifique objetos del entorno grabados por los estudiantes, utilizando redes convolucionales, autoencoders y clasificadores.

---

## Objetos a detectar
Cada estudiante grabará un video corto (1 a 3 segundos) de los siguientes objetos del salón:

- 🧰 teclado  
- 🖱️ mouse  
- 💻 pantalla  
- 🖥️ cpu  
- 🪑 silla  
- 🧫 masa

>  Todos los videos deben tomarse en el entorno del aula o laboratorio para mantener consistencia visual.

---

## 📁 Estructura del repositorio

```
data/
├─📁 raw/ # Videos originales
│ ├── 20202020202_teclado.mp4
│ ├── 20202020202_mouse.mp4
│ └── ...
├─📁 processed/ # Frames extraídos por clase
│ ├─📁 teclado/
│ │ ├── 20202020202_0001.jpg
│ │ ├── 20202020202_0002.jpg
│ ├─📁 mouse/
│ │ ├── 20202020202_0001.jpg
│ │ ├── 20202020202_0002.jpg
│ └── ...
notebooks/
├── 20202020202.ipynb # Experimentos y entrenamiento por estudiante
├── 20202020202.ipynb
└── ...
models/
├── 20202020202_autoencoder.h5 # Pesos entrenados del autoencoder
├── 20202020202_classifier.h5 # Pesos del clasificador
└── ...
```

>  Los nombres de archivos siguen el formato:
> - Videos: `"{codigo}_{objeto}.mp4"`
> - Frames: `"{objeto}/{codigo}_{indice}.jpg"`
> - Notebooks: `"{codigo}.ipynb"`
> - Pesos: `"{codigo}_autoencoder.h5"` o `"{codigo}_classifier.h5"`

---

## Cómo contribuir

1. **Haz un fork** de este repositorio.  
2. **Agrega tu video** en `data/raw/` con el nombre `"{codigo}_{objeto}.mp4"`.  
3. **Extrae los frames** y colócalos en `data/processed/{objeto}/{codigo}_{indice}.jpg`.  
4. **Crea tu notebook** en `notebooks/{codigo}.ipynb` con tus experimentos.  
5. Si entrenas modelos, guarda los pesos en `models/` con el formato indicado.  
6. **Actualiza este README** agregando tu nombre y el objeto que grabaste.  
7. **Haz un Pull Request** al repositorio principal de la organización.

---

## Requisitos básicos

* Extraer frames (1 cada 10–15 cuadros).
* Entrenar un autoencoder con las imágenes de todos los objetos.
* Usar el encoder para extraer features de cada imagen.
* Entrenar un clasificador (CNN) para predecir el tipo de objeto.
* Evaluar el modelo con los videos de otros compañeros.

---

## Resultados esperados
* Representaciones latentes del autoencoder (espacio comprimido de imágenes).
* Clasificación de objetos del entorno.
* Comparación de rendimiento entre distintos entornos o cámaras.

---

## Participantes
| Código | Nombre | Objeto | Video |
|-|-|-|-|
|20202020202 | Nombre | teclado | data/raw/20202020202_teclado.mp4 |
|20202020202 | Nombre | teclado | data/raw/20202020202_mouse.mp4 |

(Agrega tu fila al contribuir)

---


## Licencia
Este proyecto se distribuye bajo la licencia MIT.
Puedes reutilizar y modificar el contenido con fines educativos y de investigación.

---


## Créditos
Desarrollado por los estudiantes del curso con el apoyo del equipo docente.
Proyecto inspirado en la idea de crear datasets colaborativos reales para aplicar redes convolucionales en entornos cotidianos.
