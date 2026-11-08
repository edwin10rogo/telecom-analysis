# Proyecto 6: Análisis de una empresa de telecomunicaciones (ConnectaTel)

## 🎯 Objetivo del proyecto
El objetivo de este proyecto es analizar el comportamiento de los clientes de **ConnectaTel** en Latinoamérica (México y Colombia) mediante la exploración, limpieza y procesamiento de tres bases de datos relacionales. Esto permite identificar patrones de uso (llamadas y mensajes), detectar anomalías o *outliers*, y construir segmentaciones de clientes para optimizar la oferta comercial y mejorar la retención.

## 📂 Datasets utilizados
El análisis se integra a partir de tres fuentes principales:
1. **`plans.csv`**: Catálogo de planes actuales (precio, minutos y mensajes incluidos, GB por mes y costos por consumo extra). Descárgalo [aquí](https://drive.google.com/uc?export=download&id=17Mkcs9rRWwiC_gaqVBYuFieON7s9v7Bn).
2. **`users_latam.csv`**: Información demográfica y de registro de los clientes (edad, ciudad, fecha de registro, plan contratado y fecha de baja/churn). Descárgalo [aquí](https://drive.google.com/uc?export=download&id=17wuqxalUsUnw9PXvCN2_UaAz6xeS9B0T).
3. **`usage.csv`**: Detalle transaccional del uso real de los servicios (llamadas con duración y mensajes con longitud). Descárgalo [aquí](https://drive.google.com/uc?export=download&id=11T8MQf-ouxJu9tia4F8aNpY7M_fb9O4h).

## 🛠️ Etapas del análisis realizadas
1. **Carga y exploración inicial:** Validación de la estructura, dimensiones y tipos de datos de cada dataset.
2. **Control de calidad de datos:** Detección y tratamiento de valores nulos, sentinels (ej. `-999` en edad, `?` en ciudad) y fechas futuras fuera de rango.
3. **Estadísticas descriptivas y agregación:** Creación de un perfil por usuario agrupando métricas clave de llamadas y mensajes.
4. **Visualización y detección de outliers:** Análisis visual mediante histogramas y *boxplots*, aplicando el método IQR para evaluar valores extremos.
5. **Segmentación de clientes:** Creación de categorías basadas en comportamiento de uso (`grupo_uso`) y etapas de edad (`grupo_edad`).
6. **Conclusiones e insights ejecutivos:** Generación de recomendaciones comerciales orientadas a la personalización de planes y fidelización de usuarios (*power users*).

## 💻 Requisitos y dependencias
Para ejecutar este notebook de forma local o en la nube, asegúrate de tener instaladas las siguientes librerías de Python:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

## 🚀 Cómo ejecutar el proyecto
1. Clona este repositorio o descarga los archivos.
2. Abre el archivo principal del Jupyter Notebook (`.ipynb`) en tu entorno local (JupyterLab / Jupyter Notebook) o cárgalo directamente en [Google Colab](https://colab.research.google.com/).
3. Asegúrate de colocar los archivos CSV en la ruta correspondiente (o ajusta las rutas relativas en las celdas de carga de datos).
4. Ejecuta las celdas secuencialmente de arriba a abajo para reproducir el análisis completo.
