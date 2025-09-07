# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I. Presentado por: Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias.

---

## Misión 1 - Exploración del Espectro con GNU Radio

### Fase 1: Exploración y Descubrimiento
Se conectó la antena al receptor SDR y, utilizando GNU Radio, se realizó un barrido del espectro radioeléctrico en el rango de 50 a 2200 MHz.

#### Señales Identificadas:
- Radiodifusión FM (88–108 MHz)  
- Servicio de telefonía móvil (~830 MHz) 
- Posibles transmisiones de datos (>1200 MHz)  

#### Señal Seleccionada:
- **Frecuencia central:** ~830 MHz  
- **Observación:** Al realizar una llamada al centro de atención de **Claro**, se evidenció una alteración en el espectro, confirmando actividad en la red.  

#### Conclusión:
El uso del SDR permitió identificar servicios activos dentro del espectro y observar en tiempo real cómo una acción (llamada móvil) genera variaciones en una frecuencia específica.

# **Fase 2 – Misión 1: Análisis con Analizador de Espectro**

## **Enfoque**
Se conectó la antena al analizador de espectro para capturar la señal previamente identificada mediante el SDR.

## **Configuración Fina**
- **Frecuencia de referencia inicial:** 96.9 MHz  
- **Frecuencia central real medida:** 95.6 MHz  
- **SPAN:** Ajustado a **1 MHz** para realizar un “zoom” en la señal.  
- **RBW:** Configurado a un valor bajo para mejorar la resolución y distinguir claramente la portadora y sus componentes adyacentes.  

## **Recolección de Datos (Dominio de la Frecuencia)**
- Frecuencia Central (pico de portadora): 95.6 MHz  
- Marcadores de ancho de banda:  
  - Extremo izquierdo: -140.44 kHz  
  - Extremo derecho: +184.433 kHz  
  - **Ancho de banda total: ≈ 324.873 kHz  

  - Potencia de la señal: 
  - Pico central: ≈ -53.32 dBm (promedio)  
  - Extremo izquierdo: -31.22 dB  
  - Extremo derecho: -30.64 dB  

## **Estrategia de Configuración**
- RBW (Resolución): Se seleccionó un RBW reducido para mejorar la capacidad de distinguir detalles finos en la señal.  
- SPAN: Se estableció en 1 MHz, permitiendo observar la señal completa con margen para identificar sus límites.  

## Evidencia
![Captura del espectro](captura_fase2.png)

## **Conclusión**
La señal originalmente identificada en 96.9 MHz fue detectada con mayor precisión en **95.6 MHz**. Mediante un ajuste adecuado de SPAN y RBW se logró aislar, medir y analizar la portadora, determinando un **ancho de banda aproximado de 325 kHz** y una **potencia pico promedio de -53.32 dBm**, cumpliendo con los objetivos de la práctica.
