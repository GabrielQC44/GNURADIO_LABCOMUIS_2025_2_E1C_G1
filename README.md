# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I. Presentado por: Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

## Misión 2: El Enlace Crítico

## Objetivo General:
Determinar y cuantificar la atenuación (pérdida de señal) introducida por diferentes cables coaxiales a varias frecuencias, para identificar un componente defectuoso mediante la medición precisa de potencia con un generador de señal y un analizador de espectro.

## Fase 1: Configuración Experimental y Potencia de Referencia

**Parámetros del analizador de la Figura 1:** 
- RBW: 30 kHz  
- VBW: 30 kHz  
- Sweep time (SWT): 20 ms  
- Center: 50 MHz  
- Span: 1 MHz

En esta fase se estableció la línea base de medición conectando directamente el generador de señales RF al analizador de espectro mediante un cable coaxial corto de referencia, con el fin de minimizar la atenuación introducida por el sistema de conexión.

El objetivo de esta etapa es obtener la **potencia de entrada (P_in)** antes de insertar los cables a evaluar, de manera que cualquier diferencia posterior se asocie únicamente a la atenuación introducida por dichos cables.

En la medición realizada se obtuvo:

- **P_in = -10.36 dBm a 50 MHz**

Este valor servirá como referencia en las fases posteriores para calcular la atenuación de cada uno de los cables probados.

![Fase 1](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_1.jpg)

Figura 1: Configuración experimental para medir la atenuación de los cables coaxiales en diferentes frecuencias.


## Fase 2: Pruebas de Campo (Medición de Componentes)

En esta fase se sustituyó el cable de referencia de la fase 1 por los cables coaxiales a evaluar, con el objetivo de determinar la potencia de salida (**P_out**) que entrega cada uno a la misma frecuencia de referencia (50 MHz).  

Los resultados obtenidos fueron:  

- **Cable de 140 ft:** P_out = -15.41 dBm  (Figura 2)
- **Cable de 80 ft:** P_out = -13.28 dBm   (Figura 3)


Estos valores muestran una reducción de potencia en comparación con la potencia de referencia medida en la Fase 1 (**P_in = -10.36 dBm a 50 MHz**).  

La diferencia entre P_in y P_out representa la atenuación introducida por cada cable, la cual será calculada y analizada en la Fase 3.


![Fase 2 – 140 pies](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_2_140FT.jpg)

Figura 2: Medición de atenuación con cable de 140 pies.


![Fase 2 – 80 pies](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_2_80FT.jpg)

Figura 3: Medición de atenuación con cable de 80 pies.

## Fase 3 Diagnóstico y Análisis


#  Cálculo de Atenuación en Cables de RF

Acontinuación se muestra el cálculo de la atenuación teórica y la atenuación práctica de un cable coaxial a distintas frecuencias y longitudes (80 ft y 140 ft).

---

## Fórmulas

### Atenuación Teórica
La atenuación teórica depende de la frecuencia, la longitud del cable y el coeficiente de atenuación por 100 ft:

A_teo(L,f) = α_100(f) * (L/100)

donde:
- A_teo(L,f) = atenuación teórica (dB)  
- α_100(f) = atenuación por 100 ft a la frecuencia f  
- L = longitud del cable (ft)

---

### Atenuación Práctica
La atenuación práctica se calcula a partir de las mediciones de potencia de entrada y salida:

A_pract(L,f) = Pin(dBm) - Pout(dBm)

donde:
- Pin = potencia de entrada (dBm)  
- Pout = potencia de salida (dBm)  

---

##  Ejemplo de Cálculo

**Caso: Cable de 80 ft a 50 MHz**

- Atenuación especificada: 3.1 dB/100ft  
- Longitud: L = 80 ft  
- Medido: Pin = -10.36 dBm, Pout = -13.28 dBm  

### Teórica:
A_teo = 3.1 * (80/100) = 2.48 dB

### Práctica:
A_pract = Pin - Pout = (-10.36) - (-13.28) = 2.92 dB

**Resultados:**
- Atenuación teórica = 2.48 dB  
- Atenuación práctica = 2.92 dB


---

## Resultados Completos

### Cable de 140 ft

| Frecuencia (MHz) | Pin (dBm) | Pout (dBm) | Atenuación teórica (dB) | Atenuación práctica (dB) |
|-----------------:|----------:|-----------:|-------------------------:|--------------------------:|
| 50  | -10.36 | -15.42 | 4.34  | 5.06  |
| 100 | -9.48  | -18.45 | 6.30  | 8.97  |
| 200 | -8.95  | -22.26 | 9.24  | 13.31 |
| 400 | -12.64 | -34.82 | 14.00 | 22.18 |
| 700 | -16.45 | -42.81 | 19.88 | 26.36 |

---

### Cable de 80 ft

| Frecuencia (MHz) | Pin (dBm) | Pout (dBm) | Atenuación teórica (dB) | Atenuación práctica (dB) |
|-----------------:|----------:|-----------:|-------------------------:|--------------------------:|
| 50  | -10.36 | -13.28 | 2.48  | 2.92  |
| 100 | -9.48  | -14.51 | 3.60  | 5.03  |
| 200 | -8.95  | -16.79 | 5.28  | 7.84  |
| 400 | -12.64 | -22.89 | 8.00  | 10.25 |
| 700 | -16.45 | -29.73 | 11.36 | 13.28 |



---

## Evidencia de Mediciones

A continuación, se presentan las capturas de los resultados obtenidos en el laboratorio para cada cable y frecuencia.  
Estas imágenes corresponden a las lecturas del medidor de potencia y fueron la base para construir las tablas comparativas de atenuación.

---


### Cable Corto

- **50 MHz**  
  ![Cable corto 50MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_Corto_50MHZ.jpg)

- **100 MHz**  
  ![Cable corto 100MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_Corto_100MHZ.jpg)

- **200 MHz**  
  ![Cable corto 200MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_Corto_200MHZ.jpg)

- **400 MHz**  
  ![Cable corto 400MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_Corto_400MHZ.jpg)

- **700 MHz**  
  ![Cable corto 700MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_Corto_700MHZ.jpg)

---

### Cable de 140 ft

- **50 MHz**  
  ![Cable 140ft 50MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_140FT_50MHZ.jpg)

- **100 MHz**  
  ![Cable 140ft 100MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_140FT_100MHZ.jpg)

- **200 MHz**  
  ![Cable 140ft 200MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_140FT_200MHZ.jpg)

- **400 MHz**  
  ![Cable 140ft 400MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_140FT_400MHZ.jpg)

- **700 MHz**  
  ![Cable 140ft 700MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_140FT_700MHZ.jpg)

---

### Cable de 80 ft

- **50 MHz**  
  ![Cable 80ft 50MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_80FT_50MHZ.jpg)

- **100 MHz**  
  ![Cable 80ft 100MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_80FT_100MHZ.jpg)

- **200 MHz**  
  ![Cable 80ft 200MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_80FT_200MHZ.jpg)

- **400 MHz**  
  ![Cable 80ft 400MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_80FT_400MHZ.jpg)

- **700 MHz**  
  ![Cable 80ft 700MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/F3_Cable_80FT_700MHZ.jpg)

---




## Análisis y Discusión

### Identificación de anomalías
El cable de 140 ft presentó la mayor atenuación. Esto es coherente con la teoría, ya que una mayor longitud implica más pérdidas en el cable. Sin embargo, durante la práctica se observó que parte del exceso de atenuación se debía a problemas en los conectores.

---

### Análisis Causa-Raíz
Inicialmente, los conectores presentaban fallas (malos contactos o resistencia elevada), lo que incrementó la atenuación medida.  
Tras reemplazarlos por otros que proporcionó el profesor, las mediciones mejoraron, confirmando que los conectores eran una fuente de error.  

Aun así, se considera que el radio podría estar dañado, ya que seguía mostrando pérdidas mayores a las esperadas incluso con los conectores corregidos.

---

### Medición con Analizador de Redes
Además de las mediciones manuales de potencia de entrada y salida, se utilizó un **Analizador de Redes Rohde & Schwarz ZVL (9 kHz – 6 GHz)** para obtener la atenuación directamente en función de la frecuencia.

En la pantalla del equipo se observa la curva de **S12**, que corresponde a la transmisión a través del cable.

- A **50 MHz**, la máquina muestra una atenuación de aproximadamente **3.35 dB**, lo cual es consistente con los valores obtenidos experimentalmente.  
- Conforme aumenta la frecuencia, la curva desciende de manera más pronunciada, confirmando el comportamiento esperado de mayor pérdida a frecuencias más altas.

Esto permitió corroborar las anomalías y evidenciar que tanto los conectores como el radio introducían errores adicionales en las pruebas realizadas manualmente.

#### Figura – Medición con Analizador de Redes Rohde & Schwarz
![Analizador de Redes Rohde & Schwarz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_2/Analizador_ROHDE%26SCHWARZ.jpg)


Figura 4: Analizador de Redes Rohde & Schwarz

---

## Conclusiones
- La atenuación en los cables coaxiales depende directamente tanto de la **frecuencia** como de la **longitud** de la línea de transmisión: a mayor frecuencia y mayor longitud, se incrementan las pérdidas.  
- Durante la práctica se identificó que los conectores defectuosos y el posible daño en el radio generaban errores adicionales en las mediciones, lo que resalta la importancia de contar con elementos en buen estado para obtener resultados confiables.  
- La utilización del **analizador de redes** permitió confirmar con mayor precisión la atenuación en todo el rango de frecuencias, validando los resultados experimentales y mostrando con claridad el comportamiento esperado de los cables.  
- Medir la pérdida en las líneas de transmisión es fundamental para garantizar la integridad de un enlace de comunicaciones, ya que valores de atenuación por encima de lo esperado comprometen la calidad de la señal, reducen el alcance y pueden generar fallas en la transmisión de información.








