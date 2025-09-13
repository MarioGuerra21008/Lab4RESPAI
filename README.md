# 🧪 Laboratorio 4: Explicando modelos con SHAP

Este laboratorio forma parte del curso de **Responsable AI** y tiene como objetivo aplicar la librería [SHAP](https://shap.readthedocs.io/) para **interpretar las decisiones de un modelo de visión por computadora**.  

Utilizamos el modelo **MobileNetV2** preentrenado en *ImageNet* y el explicador **Partition** de SHAP para generar explicaciones visuales que muestran qué regiones de la imagen influyen en las predicciones.

---

## 🎯 Objetivos
- Cargar un modelo de clasificación de imágenes preentrenado (MobileNetV2).
- Realizar predicciones sobre un conjunto de imágenes de prueba.
- Generar explicaciones con SHAP utilizando el explainer **Partition**.
- Visualizar las regiones relevantes mediante *heatmaps* superpuestos en las imágenes.
- Reflexionar sobre el comportamiento del modelo: aciertos, errores y posibles sesgos.

---

## 📂 Contenido
El laboratorio está organizado de la siguiente forma:

1. **Carga del modelo**
   - MobileNetV2 con pesos preentrenados de *ImageNet*.
   - Definición de categorías y normalización de datos.

2. **Selección de imágenes**
   - Se utilizan al menos 2–3 imágenes de ejemplo (`avion.jpg`, `gallo.jpg`, `gorras.jpg`).

3. **Predicción**
   - El modelo genera probabilidades y top-5 de clases más probables para cada imagen.

4. **Explicaciones con SHAP**
   - Se aplica el `Partition explainer` para estimar la contribución de cada píxel/región.
   - Se generan *heatmaps* con superposición manual sobre las imágenes originales.

5. **Reflexión**
   - Se analiza si las áreas resaltadas coinciden con los objetos principales.
   - Se estudia si el modelo se enfoca en regiones relevantes.
   - Se interpretan los casos en los que el modelo se confunde.

---

## 🛠️ Dependencias

Antes de ejecutar el notebook, asegúrate de instalar las dependencias necesarias.  
Puedes hacerlo directamente con el archivo **requirements.txt** incluido en este repositorio:

```bash
pip install -r requirements.txt

