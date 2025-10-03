# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

# Fase 1: Diseño y Configuración del Modulador (Preparación Técnica)

## Montaje del Entorno
Se configuró el entorno en GNU Radio Companion (GRC).


## Diagrama de Flujo
Se diseñó un esquema para generar una señal en **Amplitud Modulada (AM)**.  

![Diagrama GNU Radio](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase1_diagrama.png)

## Señales Moduladoras
Se utilizaron diferentes señales como entrada en el bloque `Signal Source`:  
- Onda senoidal .  
- Onda cuadrada .  
- Onda triangular .  
- Onda diente de sierra .  
- Fuente de audio.

## Parámetros Iniciales
- **Frecuencia de portadora:** 433 MHz (banda experimental).  
- **Sample Rate:** 1.5625 MSps.  
- **Ganancia de transmisión (TX Gain):** 0 dB (para proteger el equipo).



# Fase 2: Conexión y Modulación

## Conexión Segura
- TX1/RX1 del USRP conectado al atenuador.  
- Atenuador conectado al canal 1 del osciloscopio.  
- La amplitud de la envolvente compleja se mantuvo menor a **0.5**.  

## Modulación con Señales Periódicas

- **Onda sinusoidal (1 kHz):**  
![Figura 1 - AM con onda sinusoidal](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_1.jpg)

- **Onda cuadrada (1 kHz):**  
![Figura 2 - AM con onda cuadrada](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_2.jpg)

- **Onda triangular:**  
![Figura 3 - AM con onda triangular](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_3.jpg)

- **Onda diente de sierra:**  
![Figura 4 - AM con onda diente de sierra](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_4.jpg)

*(se pueden agregar más capturas si corresponde: `Fase2_5.jpg` a `Fase2_10.jpg`)*  

## Modulación con Audio
- Fuente: `Audio Source` (micrófono).  
- La envolvente de la portadora siguió las variaciones de la voz/sonido.  

![Figura 5 - AM con señal de audio](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_5.jpg)

