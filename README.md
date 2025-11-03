# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

# Misión 5: Creando nuestra propia antena

## Contexto

En esta práctica se desarrolla el diseño, simulación, construcción y validación de una antena Biquad direccional operando en la banda ISM de 915 MHz.  
El objetivo es mejorar la recepción de señal en un nodo de una red **IoT** dentro del campus universitario, sin aumentar la potencia de transmisión.

A través del uso de MATLAB Online y la Antenna Toolbox, se realiza el modelado y análisis electromagnético de la antena, determinando parámetros como la impedancia y el patrón de radiación.  
Posteriormente, se construye el prototipo físico utilizando materiales de bajo costo y se validan sus características mediante un Analizador Vectorial de Redes (VNA) y un Analizador de Espectro, verificando su desempeño en la frecuencia de operación seleccionada.

## Fase 1: Diseño y Simulación (La Física detrás de la Forma)

### Selección de frecuencia
Se seleccionó una frecuencia de 915 MHz, correspondiente a la banda ISM de libre uso, utilizada frecuentemente en aplicaciones de RFID y comunicaciones de corto alcance.  

### Cálculos
A partir de la frecuencia se determinó la longitud de onda:

- λ = c / f = 327.87 mm → 0.32786 m  
- λ / 4 = 0.08197 m  
- λ / 8 = 0.04098 m  

Estos valores se emplearon para definir las dimensiones físicas de la antena tipo Biquad, donde cada brazo tiene una longitud cercana a λ/4 y la separación al reflector se aproxima a λ/8.

### Diseño en MATLAB
Con los valores anteriores, se diseñó la antena Biquad en MATLAB Online mediante la herramienta Antenna Designer.  
Se modeló el dipolo doblado sobre un plano reflector y se analizó su impedancia y directividad.

**Antena - diseño:**  
![Antena diseño MATLAB](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_diseño_matlab.jpg)

**Antena - simulación:**  
![Antena simulación MATLAB](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_simulación_matlab.jpg)

**Patrón de radiación:**  
![Patrón de radiación MATLAB](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/patron_radiación_matlab.jpg)

El patrón de radiación obtenido muestra una respuesta direccional, concentrando la energía hacia el frente del reflector, lo cual confirma el comportamiento esperado de una antena Biquad en esta banda de frecuencia.


## Fase 2: Construcción

Se realizó el montaje y soldadura de la antena, siguiendo las medidas obtenidas en la simulación de la fase 1.  
Se utilizó alambre de cobre rígido para formar los dos cuadrados del diseño Biquad, cuidando que las longitudes de los lados y la separación con el reflector coincidieran con las calculadas en MATLAB.  

Durante la construcción se preparó el plano reflector y se instaló el conector SMA en el centro para conectar la antena al equipo de medición.  
Posteriormente, se soldaron los puntos del alambre al conector, asegurando un buen contacto eléctrico y una estructura estable.  

Finalmente, se revisó la rigidez de la antena y la correcta distancia entre el elemento radiante y el reflector antes de continuar con las mediciones.

**Antena terminada (vista 1):**  
![Antena biquad terminada 1](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_terminada.jpg)

**Antena terminada (vista 2):**  
![Antena biquad terminada 2](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_terminada_2.jpg)

## Fase 3: Medición y Validación

Se realizó la medición de la antena Biquad utilizando el Analizador Vectorial de Redes Rohde & Schwarz ZVL6, observando el parámetro S11.  

**Medición del parámetro S11:**  
![Antena S11 1](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_S11.jpg)  
![Antena S11 2](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_S11_foto.jpg)

Durante la medición se observó que la antena presentó una frecuencia de resonancia entre 1272 y 1274 MHz, lo que indica que hubo una desviación respecto a la frecuencia esperada de 915 MHz.  
Esto sugiere que hubo pequeños errores en las dimensiones físicas o en la distancia del reflector durante la construcción, afectando la frecuencia de resonancia.  

Debido a que la antena operó por encima de 1 GHz, no se pudo utilizar el analizador de espectro directamente, por lo que el profesor realizó el ajuste de canal en el VNA para observar el espectro de la señal.  

**Espectro de la antena Biquad creada:**  
![Espectro antena Biquad](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_Analizador_espectro.jpg)

Posteriormente, se comparó el comportamiento con una antena comercial WA5VJB (850–6500 MHz) para observar diferencias en el espectro y la respuesta de señal.  

**Antena WA5VJB:**  
![Antena WA5VJB comparada](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/WA5VJB_Antena_comparada.jpg)  

**Espectro WA5VJB:**  
![WA5VJB espectro](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/WA5VJB_Analizador_Espectrojpg.jpg)


## Resultados y Evidencias

### Tabla de diseño
| Parámetro | Valor aproximado |
|------------|------------------|
| Frecuencia de diseño | 915 MHz |
| Longitud de onda (λ) | 0.327 m |
| Lado del Quad (λ/4) | 0.0819 m |
| Distancia al reflector (λ/8) | 0.0409 m |

---

### Simulación en MATLAB

**Gráfico de S11 (simulación):**  
![Simulación S11 MATLAB](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_simulación_matlab.jpg)

**Patrón de radiación:**  
![Patrón de radiación MATLAB](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/patron_radiación_matlab.jpg)

---

### Mediciones experimentales

**Medición con el VNA (S11 real):**  
![Medición S11](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_S11.jpg)

**Medición del espectro con la antena Biquad:**  
![Espectro Biquad](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_Analizador_espectro.jpg)

---

### Prototipo final

**Antena Biquad construida:**  
![Antena biquad terminada](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Misión_5/Antena_biquad_terminada.jpg)


### Análisis y Discusión

La antena Biquad fue diseñada para operar a una frecuencia central de 915 MHz según la simulación realizada en MATLAB.

Sin embargo, al medir el parámetro S₁₁ con el analizador de redes, la frecuencia de resonancia real se observó aproximadamente en 1274 MHz, lo cual representa un desplazamiento hacia frecuencias más altas (incremento de alrededor del 39 % respecto a la simulada).

#### Posibles causas del corrimiento
- Tolerancias de construcción: pequeñas variaciones en la longitud de los lados o en la separación entre elementos reducen la longitud eléctrica efectiva.  
- Irregularidades físicas: se observaron ligeras imperfecciones en el doblado de los cables y en las soldaduras, que modifican la geometría del dipolo.  
- Efectos del entorno: durante la medición, la antena estaba cerca de objetos metálicos y se manipuló manualmente, lo que pudo alterar el campo electromagnético.  
- Conector no modelado: el conector SMA y los cables coaxiales no fueron considerados en la simulación, introduciendo diferencias adicionales.

Durante las mediciones con el analizador de espectro, se observó un mínimo pronunciado de reflexión en torno a 1274 MHz, confirmando la presencia de resonancia.  
Al rotar la antena respecto a la fuente emisora, la potencia recibida varió con el ángulo, mostrando un máximo cuando la cara del biquad estaba orientada hacia el transmisor.

Este comportamiento confirma que la antena presenta un patrón direccional, tal como se esperaba del diseño simulado en MATLAB, donde el patrón de radiación es de tipo broadside, con máxima radiación perpendicular al plano de los cuadros.  
El patrón medido fue coherente con la simulación, aunque con un leve desplazamiento en frecuencia debido al cambio en la resonancia real.

En el proceso de diseño en MATLAB, se ajustaron las dimensiones geométricas (lado del cuadro, separación entre elementos y grosor del conductor) hasta lograr un mínimo en S₁₁ cercano a 916 MHz.  
Este ajuste se realizó de manera paramétrica, observando cómo la frecuencia de resonancia varía inversamente con el tamaño de la antena:

- Aumentar las dimensiones desplaza la frecuencia hacia valores menores.  
- Reducirlas la mueve hacia frecuencias más altas.

Por tanto, para corregir el desajuste observado experimentalmente, se recomienda incrementar las dimensiones lineales de la antena en aproximadamente un 39 %, o bien incluir el modelo del conector SMA y el entorno real en la simulación para obtener resultados más precisos.



## Conclusiones:

- El diseño y simulación en MATLAB Antenna Toolbox permitió comprender la relación entre las dimensiones físicas de la antena Biquad y su frecuencia de resonancia.  
  Los resultados simulados mostraron una frecuencia de operación en 915 MHz, dentro de la banda ISM, con un patrón de radiación direccional tipo broadside, como se esperaba teóricamente.

- Durante la construcción del prototipo, se verificó la importancia de la **precisión mecánica**: pequeñas variaciones en las longitudes, en el ángulo de los dobleces o en la separación con el reflector modifican la longitud eléctrica efectiva, provocando un corrimiento en la frecuencia de resonancia.

- En la medición con el Analizador Vectorial de Redes (VNA) se observó un mínimo en S₁₁ alrededor de 1274 MHz, lo que representa un desplazamiento del ~39 % respecto a la frecuencia simulada.  
  Este corrimiento confirma la sensibilidad de la antena a las tolerancias de fabricación, al entorno de prueba y a elementos no modelados (como el conector SMA y los cables coaxiales).

- Pese al desplazamiento en frecuencia, la antena mostró un patrón de radiación direccional coherente con la simulación, concentrando la energía hacia el frente del reflector y validando el principio de funcionamiento de la antena Biquad.

- Para mejorar la coincidencia entre simulación y medición, se recomienda:
  - Incluir el modelo del conector y entorno en futuras simulaciones.  
  - Ajustar las dimensiones físicas aumentando aproximadamente un **39 %** para compensar el corrimiento.  
  - Realizar mediciones en un entorno libre de objetos metálicos y con sujeción fija.

**Conclusión general:**  
La práctica permitió integrar teoría electromagnética, simulación y experimentación, demostrando cómo los parámetros físicos influyen directamente en el comportamiento real de una antena. Aun con el desplazamiento en frecuencia, el diseño cumplió su propósito de generar una antena direccional funcional, adecuada para aplicaciones IoT en la banda ISM.







