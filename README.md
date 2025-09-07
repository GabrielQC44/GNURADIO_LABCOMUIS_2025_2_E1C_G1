# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I. Presentado por: Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

## Misión 2: El Enlace Crítico

## Objetivo General:
Determinar y cuantificar la atenuación (pérdida de señal) introducida por diferentes cables coaxiales a varias frecuencias, para identificar un componente defectuoso mediante la medición precisa de potencia con un generador de señal y un analizador de espectro.

## Fase 1

![Fase 1](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_1.jpg)

Figura 1: Configuración experimental para medir la atenuación de los cables coaxiales en diferentes frecuencias.

## Fase 2

![Fase 2 – 140 pies](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_2_140FT.jpg)

Figura 2: Medición de atenuación con cable de 140 pies.


![Fase 2 – 80 pies](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/f928230a88c684a549bf4596c29c666983b65f80/imagenes/Mision_2/F_2_80FT.jpg)

Figura 3: Medición de atenuación con cable de 80 pies.

## Fase 3


# 📡 Cálculo de Atenuación en Cables de RF

Este proyecto muestra el cálculo de la **atenuación teórica** y la **atenuación práctica** de un cable coaxial a distintas frecuencias y longitudes (80 ft y 140 ft).

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

##  Conclusión

- La atenuación aumenta con la **frecuencia** y con la **longitud del cable**.  
- Los valores prácticos siempre resultan ligeramente mayores que los teóricos debido a pérdidas adicionales (conectores, tolerancias del cable, etc.).  
- Los resultados experimentales son **coherentes** con la teoría.









