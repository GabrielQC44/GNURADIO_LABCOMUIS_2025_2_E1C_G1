# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

# Mision 3: Modulacion de onda continua

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



## Fase 2

### Conexión Segura
Conecte la salida de transmisión (TX1 / RX1) de su SDR al atenuador, y la salida del atenuador a la entrada del canal 1 del osciloscopio.  
**Nota:** recuerde que la amplitud máxima de la envolvente compleja debe ser menor a 0.5.

### Modulación con Señales Periódicas
- Ejecute su diagrama de flujo de AM con la señal sinusoidal. Observe la forma de onda en el osciloscopio. Capture una imagen de la pantalla.  
- Sin detener la transmisión, cambie la señal moduladora a la onda cuadrada. Observe cómo se modifica la envolvente. Capture una imagen.  
- Repita el procedimiento con las señales diente de sierra y triangular.

**Señal senoidal (1 kHz):**  
![Fase2_1](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_1.jpg)  *  


Se le aplico un KP de 1 y esto ocasiono que el offset se duplicara, siendo de 10.76.

**Señal senoidal con KP 1 (1 kHz):** 
![Fase2_3](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_3.jpg)  


**Señal senoidal con KP 0 (1 kHz):**
![Fase2_4](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_4.jpg)  

**Señal cuadrada (1 kHz):**  
![Fase2_5](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_5.jpg)  
![Fase2_8](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_8.jpg)  

**Señal diente de sierra (1 kHz):**  

![Fase2_10](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_10.jpg)  

**Señal triangular (1 kHz):**  
![Fase2_9](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_9.jpg)  

### Modulación con Audio
- Seleccione el diagrama de flujo de AM.  
- Utilice la fuente de audio (micrófono) y hable o reproduzca sonido.  
- Observe cómo la amplitud de la portadora sigue la forma de onda de la voz.

**Señal de audio (voz/micrófono):**
![Fase2_6](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase2_6.jpg)  



---



## Fase 3: Análisis de Espectro y Comparación

### Tabla Comparativa de Señales Moduladoras

| Tipo de Señal Moduladora | Descripción de la Señal | Características en el Dominio de la Frecuencia | Efecto de la Modulación |
|--------------------------|--------------------------|------------------------------------------------|--------------------------|
| Senoidal                | Una señal sinusoidal pura, sin distorsión. | La señal modulada se muestra como una variación pequeña alrededor de la frecuencia portadora. Aparecen picos nítidos cercanos a la portadora (espectro estrecho). | La modulación con onda senoidal genera un espectro simple y definido, con mayor fidelidad y poca distorsión. |
| Cuadrada                | Una señal cuadrada ideal, con transiciones abruptas. | La señal modulada muestra una estructura con más armónicos (múltiplos de la frecuencia fundamental). El espectro es más amplio alrededor de la portadora. | La modulación con onda cuadrada produce mayor dispersión de armónicos y distorsión debido a las transiciones rápidas. |
| Triangular              | Una señal triangular periódica. | Presenta armónicos impares, pero con amplitudes que decrecen más rápido que la cuadrada. El espectro es más “suave” que el de la onda cuadrada. | La modulación triangular genera menos distorsión que la cuadrada, pero mantiene un contenido armónico moderado. |
| Diente de sierra        | Una señal periódica con pendiente lineal y reinicio abrupto. | Contiene armónicos de mayor amplitud y más densos que la triangular. El espectro se dispersa de manera notable alrededor de la portadora. | La modulación diente de sierra produce un espectro con fuerte contenido armónico, más complejo y con mayor dispersión. |
| Sonora (Audio)          | Una señal de audio (voz/música). | El espectro es irregular y mucho más amplio, reflejando variaciones en amplitud y frecuencia del sonido. | La modulación con audio genera un espectro rico en frecuencias, que refleja la complejidad de la señal de voz/música. |

---

### Descripción Técnica

1. **Senoidal:** Genera un espectro limpio con mínima distorsión.  
2. **Cuadrada:** Introduce muchos armónicos, lo que puede llevar a distorsión significativa.  
3. **Triangular:** Tiene armónicos, pero de menor intensidad que la cuadrada; modulación más suave.  
4. **Diente de sierra:** Produce un espectro más denso en armónicos y mayor dispersión.  
5. **Audio:** Captura la complejidad del sonido con un espectro amplio y variable.

---

### Evidencia Experimental

**Señal medida en el analizador de espectro:**  

![Señal de espectro Fase 3](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_3/Fase3_1.jpg)


##  Conclusiones

- Se comprobó que el modulador AM del SDR responde correctamente a diferentes tipos de señales moduladoras, reflejando en la envolvente los cambios de amplitud y frecuencia de cada una.  
- La señal sinusoidal generó un espectro limpio y simétrico, con alta fidelidad y mínima distorsión.  
- La señal cuadrada mostró una envolvente con transiciones bruscas y un espectro más ancho debido a la presencia de múltiples armónicos.  
- La triangular presentó un comportamiento más estable que la cuadrada, con un espectro más “suave” y menor contenido armónico.  
- La diente de sierra evidenció un espectro amplio y denso en armónicos, demostrando mayor complejidad en la modulación.  
- La señal de audio produjo una envolvente irregular y un espectro variable, dependiente del contenido sonoro, mostrando la capacidad del sistema para modular información real.  
- En general, se observó que a medida que aumenta la complejidad de la señal moduladora, el **ancho de banda ocupado** también crece, y la envolvente se vuelve menos uniforme.  
- El uso del SDR permitió visualizar claramente la relación entre el dominio del tiempo y el de la frecuencia, reforzando los principios teóricos de la modulación AM.





