# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias


# Misión 7: inteligencia Artificial con Gnu Radio

### Contexto 

En esta misión se busca integrar el uso de herramientas de inteligencia artificial en el desarrollo de sistemas de telecomunicaciones avanzados. El objetivo es crear un prototipo de receptor cognitivo capaz de analizar y adaptarse dinámicamente a las condiciones del canal. Para ello, se implementarán bloques personalizados en GNU Radio que permitan medir en tiempo real parámetros estadísticos esenciales de una señal, como la potencia, la media y la desviación estándar. Esta actividad combina el uso de IA generativa con el diseño de procesamiento digital de señales, fomentando la automatización y optimización en la ingeniería de radiofrecuencia.




## Fase 1: Especificación y Generación (Ingeniería de Prompts)

En esta fase se definieron los requerimientos de los bloques y se elaboraron los *prompts* necesarios para que una herramienta de inteligencia artificial generara el código en Python compatible con GNU Radio.  
El propósito fue crear dos bloques personalizados: un **Estimador de Potencia** y un **Bloque de Estadísticas de Amplitud**, ambos diseñados como Embedded Python Blocks.

---

### Bloque 1: Estimador de Potencia

**Descripción:**  
Este bloque recibe una ventana de muestras complejas y calcula la potencia promedio de la señal.

**Prompt utilizado:**  

Necesito el código para un bloque Embedded Python Block de GNU Radio.
El bloque debe tener una entrada (vector, tipo complejo) y una salida (un solo item, tipo float).
La función work debe calcular la potencia promedio de la ventana de entrada.
La potencia se define como la media del cuadrado de la magnitud de las muestras.
Asegúrese de importar la biblioteca numpy.

### Codigo dado por la IA chatgpt


![Código del Bloque 1: Estimador de Potencia](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/raw/main/imagenes/Misión_7/Estimador_potencia_Codigo.jpg)

## Bloque 2: Estadísticas de Amplitud

**Descripción:**  
Este bloque recibe una ventana de muestras complejas y calcula dos valores: la **media** y la **desviación estándar** de la magnitud.
Se obtiene la magnitud de cada muestra y luego se calculan la **media** y la **desviación estándar** de ese conjunto de magnitudes utilizando funciones de `numpy`.

---

**Prompt utilizado:**  
Genere el código para un Embedded Python Block de GNU Radio con una entrada (vector, tipo complejo) 
y dos salidas (un solo item por salida, ambas tipo float). 
La salida out[0] debe ser la media de la magnitud de las muestras de entrada 
(calculada como numpy.mean(numpy.abs(in_sig[0]))). 
La salida out[1] debe ser la desviación estándar de la magnitud de ese mismo muestreo.

### Codigo dado por la IA chatgpt

![Código del Bloque 2: Estadísticas de Amplitud](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/raw/main/imagenes/Misión_7/Estadisticas_Amplitud_Codigo.jpg)



##  Fase 2: Integración y Pruebas (Implementación en GRC)

###  Construcción del Banco de Pruebas  
Se implementó en GNU Radio Companion (GRC) un diagrama de flujo que permite probar y validar el funcionamiento de los bloques desarrollados.  
El banco de pruebas incluye:  
- Una fuente de ruido gaussiano (Noise Source) como señal de entrada.  
- Un bloque Throttle para controlar la velocidad de muestreo.  
- Bloques QT GUI Time Sink y QT GUI Histogram Sink para visualizar la señal de ruido.  
- Los bloques Embedded Python Block generados por la IA en la Fase 1:
  - Bloque 1: Estimador de Potencia 
  - Bloque 2: Estadísticas de Amplitud  

###  Integración de los Bloques Personalizados  
- Se integró el Bloque 1 (Potencia) conectando su entrada al Throttle y su salida a un QT GUI Number Sink etiquetado como *Potencia*.  
- Se integró el Bloque 2 (Estadísticas) con dos salidas tipo float, conectadas respectivamente a los visores numéricos etiquetados como Media y Desv. Estándar.  
- Finalmente, se conectaron todos los bloques para observar en tiempo real los valores calculados.

###  Diagrama de Flujo en GRC  
![Diagrama de flujo en GNU Radio](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Misión_7/Fase_2.jpg)








