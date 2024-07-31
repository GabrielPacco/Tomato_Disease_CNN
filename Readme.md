# Proyecto de Detección de Plagas en Cultivos Utilizando Redes Neuronales Profundas

## Descripción General

Este proyecto tiene como objetivo desarrollar modelos de redes neuronales profundas para la detección automática de plagas en cultivos de tomate, utilizando técnicas avanzadas de visión por computadora y aprendizaje profundo. Los modelos son entrenados y evaluados utilizando un conjunto de datos de imágenes de hojas de tomate afectadas por diversas enfermedades y plagas.

## Estructura del Proyecto

### 1. Preprocesamiento de Datos
El proyecto comienza con la carga y preprocesamiento del conjunto de datos de imágenes. Este paso incluye:
- **Carga de imágenes**: Lectura de imágenes desde el sistema de archivos.
- **Etiquetado de imágenes**: Asignación de etiquetas a cada imagen basada en la enfermedad o plaga.
- **Aumentación de datos**: Aplicación de técnicas de aumentación para incrementar la diversidad del conjunto de datos y prevenir el sobreajuste.
- **Normalización de imágenes**: Escalado de los valores de píxeles para mejorar la eficiencia del entrenamiento del modelo.

### 2. Definición y Entrenamiento de Modelos
Tres modelos preentrenados diferentes se utilizan para comparar su rendimiento en la tarea de detección de plagas:
- **EfficientNetV2**
- **Vision Transformer (ViT)**
- **ResNet50**

Cada modelo se compila y entrena utilizando el optimizador Adam con una tasa de aprendizaje inicial de 0.001. Los datos se dividen en conjuntos de entrenamiento, validación y prueba para evaluar el rendimiento de los modelos de manera justa.

### 3. Evaluación de Modelos
Después del entrenamiento, los modelos se evalúan utilizando varias métricas de rendimiento, incluyendo:
- **Precisión (accuracy)**
- **Recall**
- **F1-Score**

Se generan matrices de confusión para visualizar el rendimiento de los modelos en la clasificación de las imágenes de prueba. Además, se calculan las métricas macro-promediadas, micro-promediadas y ponderadas para proporcionar una visión completa del rendimiento de los modelos.

### 4. Monitoreo del Impacto Ambiental
Se utiliza la biblioteca CodeCarbon para monitorizar el consumo de energía y las emisiones de carbono durante el entrenamiento de los modelos. Esto permite evaluar la sostenibilidad de las prácticas de entrenamiento y tomar decisiones informadas para optimizar el uso de recursos.

### 5. Resultados y Análisis
Los resultados de las evaluaciones se presentan y analizan para identificar el modelo más eficiente y preciso para la detección de plagas en cultivos de tomate. Se discuten las implicaciones prácticas de los resultados y se proporcionan recomendaciones para futuros trabajos en este campo.

## Configuración Experimental

Los experimentos se llevaron a cabo en una máquina equipada con la siguiente configuración de hardware:

- **GPU:** 1 x NVIDIA A100-SXM4-40GB
- **CPU:** Intel(R) Xeon(R) CPU @ 2.20GHz
- **Número de CPUs:** 12
- **RAM disponible:** 83.477 GB
- **Sistema operativo:** Linux-6.1.85+-x86_64-with-glibc2.35
- **Versión de Python:** 3.10.12

Se utilizó la biblioteca TensorFlow para la implementación de los modelos. Esta configuración permitió llevar a cabo los experimentos de manera eficiente, aprovechando la capacidad de procesamiento paralelo de la GPU y la CPU, así como la gran cantidad de memoria RAM disponible para manejar los datos y los modelos.

## Declaración de Ética

Durante el desarrollo de este proyecto, se tuvieron en cuenta varias consideraciones éticas:
- **Fuentes de Datos:** Los datos utilizados para el entrenamiento de los modelos provienen de fuentes legítimas y se respetaron todas las normativas de protección de datos.
- **Implicaciones Éticas:** Se reflexionó sobre las posibles implicaciones éticas de utilizar modelos de detección de plagas en la práctica agrícola, como el potencial desplazamiento de trabajadores humanos y la dependencia de la tecnología.
- **Impacto Ambiental:** Se consideró el impacto ambiental de la implementación de sistemas automatizados de monitoreo de cultivos, como el consumo de energía y los desechos electrónicos. La biblioteca CodeCarbon se utilizó para monitorizar y minimizar el impacto ambiental durante el entrenamiento de los modelos.
