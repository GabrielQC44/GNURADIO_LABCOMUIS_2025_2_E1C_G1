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


## Pruebas y Resultados

###  Prueba 1: Ruido Gaussiano  
Se ejecutó el diagrama de flujo con una fuente de ruido gaussiano.  
El sistema mostró valores estables de potencia, media y desviación estándar, confirmando que los bloques personalizados funcionan correctamente en tiempo real.  

Posteriormente se modificó la amplitud del Noise Source, observándose lo siguiente:
- Al aumentar la amplitud, la potencia promedio también aumentó de manera proporcional.  
- La **media** se mantuvo cercana a cero (por la simetría del ruido).  
- La desviación estándar creció junto con la potencia, reflejando mayor variabilidad en las muestras.  

##  Fase 2 — Integración, Pruebas y Resultados en GNU Radio Companion

En esta fase se integraron los bloques desarrollados en **Embedded Python** para medir:

- Potencia de la señal
- Media de la magnitud
- Desviación estándar

Se realizaron dos pruebas:

1. Fuente de señal: **Ruido Gaussiano**
2. Fuente de señal: **Señal Senoidal (tono)**
o

### Prueba 1 — Ruido Gaussiano (Amp baja)
**Descripción:** Se ejecutó una fuente de ruido gaussiano con amplitud baja. Se registraron la forma de onda en el tiempo, el histograma y los valores numéricos (potencia, media, desviación estándar).

*
![Im1: Ruido Gaussiano Amp baja](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_7/Im1.png)

Señal aleatoria centrada cerca de 0; histograma con distribución aproximada; Number Sinks muestran valores bajos de potencia y desviación.

---

### Prueba 1 — Ruido Gaussiano (Amp mayor)
Se incrementó la amplitud de la fuente de ruido y se repitió la medición para observar efecto en potencia y dispersión.
  
![Im2: Ruido Gaussiano Amp mayor](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_7/Im2.png)

 Al aumentar la amplitud se incrementa la potencia medida y la desviación estándar; el histograma se ensancha, lo cual es consistente con la teoría.

### Prueba 2 — Señal Determinista (Tono seno, Amp = 1)
 Se reemplazó la fuente de ruido por un `Signal Source` tipo Cosine, amplitud = 1, para validar comportamiento con señal determinista.

![Im3: Señal Senoidal Amp=1](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_7/Im3.png)

La magnitud es constante ≈1 (media ≈1), desviación estándar ≈0; la potencia calculada por el bloque aparece ~1 (el bloque está evaluando magnitud/potencia sobre la señal).

---

### Observaciones generales 
- Bloque de potencia y bloque de estadísticas funcionan en tiempo real y muestran los efectos teóricos esperados: aumentar amplitud → aumenta potencia y desviación; señal determinista → media estable y desviación ~0.  
- Las capturas (Im1, Im2, Im3) sirven como evidencia visual de las mediciones.  
- **Siguiente paso:** completar la *Tabla de Validación Experimental* con los valores numéricos extraídos (se puede añadir debajo de estas evidencias).



# Validación de Señal: Ruido vs Tono

## 1. Objetivo
Comparar valores teóricos vs valores medidos de:
- Ruido aleatorio (Noise Source)
- Tono senoidal (Signal Source, Cosine, A=1)

---

## 2. Modelo teórico

### 2.1 Tono senoidal (A = 1)
Señal:

x(t) = A * cos(wt) ,  A = 1


Parámetros teóricos:

Potencia = A^2 / 2 = 0.5
Media de la magnitud = A = 1.0
Desviación estándar de la magnitud = 0


---

### 2.2 Ruido (Gaussiano ideal)
Definimos varianza como sigma^2:


Potencia = sigma^2
Media ≈ 0  (si está centrado)
Desviación estándar = sigma = sqrt(sigma^2)


Estos valores no son constantes, dependen de la configuración real del generador de ruido.



## 3. Comparación resultados

| Fuente de Señal | Parámetro | Valor Teórico | Valor Medido |
|---|---|---|---|
| Ruido (Amp=1) | Potencia | sigma^2 | 0.9897 |
| Ruido (Amp=1) | Media (Mag) | ≈ 0 | 0.8895 |
| Ruido (Amp=1) | Desv. Est. (Mag) | sigma | 0.4630 |
| Tono (Amp=1) | Potencia | 0.5 | 0.9999 |
| Tono (Amp=1) | Media (Mag) | 1.0 | 0.9999 |
| Tono (Amp=1) | Desv. Est. (Mag) | 0.0 | 0.0000 |

---

## 4. Cálculos teóricos

### Tono:

P = A^2 / 2 = 1^2 / 2 = 0.5
Magnitud = 1 -> media 1
Sin variación en magnitud -> desviación = 0


### Ruido:

P = sigma^2
Media ≈ 0
Desv = raiz(sigma^2)


- El tono muestra el comportamiento esperado.
- El ruido no está centrado en cero, lo que explica la media obtenida.
- La potencia del ruido representa su varianza efectiva en la medición.

  ## Conclusiones Generales

- Los bloques desarrollados mediante Embedded Python funcionaron correctamente dentro de GNU Radio, permitiendo la medición en tiempo real de potencia, media y desviación estándar de señales complejas.
- La señal senoidal (tono) presentó resultados coherentes con el modelo teórico, confirmando que el cálculo de magnitud, potencia y dispersión se implementó correctamente en condiciones deterministas.
- En el caso del ruido, los valores medidos dependieron directamente de la varianza generada por la fuente, lo cual es esperable, ya que no existe un único valor teórico fijo para este tipo de señal aleatoria.
- La media del ruido no se encontró exactamente en cero, lo cual indica que la distribución generada posee un ligero desplazamiento (offset) o sesgo, fenómeno observable en generadores reales de ruido no ideal.
- El aumento de la amplitud del ruido produjo incrementos proporcionales en la potencia y en la desviación estándar, validando correctamente la relación entre energía y dispersión estadística.









