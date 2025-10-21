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
- 🧫 mesa
-  nada

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
|20242695004 | Andres Pulido | mause | data/raw/20242695004_mouse.mp4 |
|20242695004 | Andres Pulido | teclado | data/raw/20242695004_teclado.mp4 |
|20242695004 | Andres Pulido | silla | data/raw/20242695004_silla.mp4 |
|20242695004 | Andres Pulido | mesa | data/raw/20242695004_mesa.mp4 |
|20242695004 | Andres Pulido | cpu | data/raw/20242695004_cpu.mp4 |
|20242695004 | Andres Pulido | pantalla | data/raw/20242695004_pantalla.mp4 |
|20242695004 | Andres Pulido | nada | data/raw/20242695004_nada.mp4 |
|20242595005 | Fernando Zubieta | nada | data/raw/20242595005_ruido.mp4 |
|20242595005 | Fernando Zubieta | cpu | data/raw/20242595005_cpu.mp4 |
|20242595005 | Fernando Zubieta | silla | data/raw/20242595005_silla.mp4 |
|20242595005 | Fernando Zubieta | mesa | data/raw/20242595005_mesa.mp4 |
|20242595005 | Fernando Zubieta | teclado | data/raw/20242595005_teclado.mp4 |
|20242595005 | Fernando Zubieta | mouse | data/raw/20242595005_mouse.mp4 |
|20251595006 | Alvaro Zarabanda | nada | data/raw/20251595006_Ruido.mp4 |
|20251595006 | Alvaro Zarabanda | cpu | data/raw/20251595006_Cpu.mp4 |
|20251595006 | Alvaro Zarabanda | silla | data/raw/20251595006_Silla.mp4 |
|20251595006 | Alvaro Zarabanda | mesa | data/raw/20251595006_Mesa.mp4 |
|20251595006 | Alvaro Zarabanda | teclado | data/raw/20251595006_Teclado.mp4 |
|20251595006 | Alvaro Zarabanda | mouse | data/raw/20251595006_Mouse.mp4 |
|20251595006 | Alvaro Zarabanda | pantalla | data/raw/20251595006_Pantalla.mp4 |
(Agrega tu fila al contribuir)

---


## Licencia
Este proyecto se distribuye bajo la licencia MIT.
Puedes reutilizar y modificar el contenido con fines educativos y de investigación.


