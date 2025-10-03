# Misión 1 - Exploración del Espectro con GNU Radio y Equipos de Medida

---

## Fase 1: Exploración con SDR (USRP + GNU Radio)

Se conectó la antena al receptor SDR y se realizó un barrido del espectro radioeléctrico en el rango de 94 a 106 MHz, dentro de la banda de radiodifusión FM.  
La visualización en GNU Radio permitió identificar varias emisoras activas, entre ellas señales destacadas alrededor de 95.7 MHz, 99.7 MHz y 04 MHz.  

Adicionalmente, se configuró el receptor SDR en la banda de 830 MHz (servicios de telefonía móvil).  
Durante esta prueba, al realizar una llamada a la línea de atención móvil de Claro, se observó una alteración inmediata en el espectro, lo que evidencia la actividad generada por el establecimiento de la comunicación.  

#### Evidencia
![Espectro en GNU Radio](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_1/Analisis_en_frecuencia_GNU_usando_USRP_con_antena_SDR.png)

#### Conclusión
El SDR brindó una visión panorámica en tiempo real del espectro, mostrando qué frecuencias estaban activas de forma continua.  
Además, permitió verificar experimentalmente cómo una acción del usuario (como iniciar una llamada móvil) genera tráfico radioeléctrico visible en la banda de 830 MHz.  
Esta exploración permitió seleccionar la frecuencia de 99.7 MHz como señal de interés para el análisis posterior en equipos de laboratorio.

---

## Fase 2: Análisis en el Analizador de Espectro

Posteriormente, se utilizó el analizador de espectro Rohde & Schwarz FPC1000 para centrar la atención en la emisora de 99.7 MHz.  
Se configuraron los parámetros de medición para mejorar la resolución:  

- Frecuencia central: 99.7 MHz  
- SPAN: 5 MHz  
- RBW/VBW: 100 kHz  
- Nivel de potencia pico: ≈ -64 dBm  
- Ancho de banda total: ≈ 325 kHz  

#### Evidencia
![Espectro ajustado a 99.7 MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_1/Espectro_ajustado_para_99.7Mhz.jpeg)

#### Conclusión
El analizador permitió confirmar con precisión la frecuencia central de la emisora y medir su potencia relativa.  
Se obtuvo un ancho de banda de aproximadamente 325 kHz, valor típico de FM comercial.  
La resolución ajustada (RBW) permitió distinguir claramente la portadora y sus componentes laterales.

---

## Fase 3: Validación en Osciloscopio con FFT

Finalmente, se conectó la señal al osciloscopio digital Rohde & Schwarz RTB2004 y se activó la función de FFT para comparar la medición en el dominio del tiempo con su representación en frecuencia.  

- Frecuencia central: 99.7 MHz  
- SPAN: 5.72 MHz  
- RBW: 28.6 kHz  
- Potencia pico estimada: ≈ -56 dBm  
- Ancho de banda observado: ~300 kHz  

#### Evidencia
![Señal del Osciloscopio con FFT a 99.7 MHz](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_1/Señal_del_Osciloscopio_usando_la_FFT_para_99.7MHz.jpeg)

#### Conclusión
El osciloscopio confirmó la misma frecuencia central observada en el analizador, validando además la forma espectral en el dominio de tiempo y frecuencia.  
Aunque su estimación de potencia es menos precisa, permitió comprobar la coherencia de la señal medida.

---

## Conclusión General 

La misión permitió identificar, aislar y analizar señales reales del espectro radioeléctrico.  
Mediante el uso de SDR, analizador de espectro y osciloscopio se logró:  

1. Explorar el espectro y detectar múltiples emisoras FM y servicios móviles.  
2. Medir con precisión frecuencia central, ancho de banda y potencia de la señal seleccionada (99.7 MHz).  
3. Validar la coherencia en el dominio temporal y espectral.  

Esto evidencia la importancia del uso complementario de herramientas de software (SDR) y hardware (analizador y osciloscopio) en el estudio práctico de las comunicaciones.
