# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias

# Misión 4: Vigilancia del Espectro Legal  

## Contexto  
Usted ha sido designado como un inspector de campo de la **Agencia Nacional del Espectro (ANE)**.  
Hemos recibido reportes de posibles interferencias en la banda de radiodifusión comercial en Bucaramanga.  
Su misión es realizar una auditoría del **espectro FM** para verificar que todas las transmisiones activas operen con una licencia válida y en sus parámetros autorizados, identificando cualquier posible transmisión ilegal.  

## Objetivo General  
Auditar el espectro de radiodifusión sonora en **Frecuencia Modulada (FM)** de Bucaramanga, comparando las señales detectadas en campo con los registros oficiales del **Ministerio de Tecnologías de la Información y las Comunicaciones (MinTIC)** y la **ANE**, para identificar transmisiones no autorizadas.  

# Misión 4: Vigilancia del Espectro Legal  

## Fase 1: Inteligencia y Preparación (Investigación Regulatoria)

Se consultó la base de datos oficial del Sistema de Gestión del Espectro (SGE) y el CNABF del MinTIC.  
A continuación se listan las emisoras de FM registradas en Bucaramanga y su área metropolitana:

| Municipio       | Nombre comercial de la Emisora                              | Frecuencia Asignada | Distintivo de Llamada | Clase de emisora según área de servicio | Clase de emisora según gestión de servicio | Clase de emisora según el PTNRS | Clase de emisora según área de servicio |
|-----------------|-------------------------------------------------------------|---------------------|-----------------------|-----------------------------------------|---------------------------------------------|---------------------------------|-----------------------------------------|
| Bucaramanga     | Emisora Cultural Luis Carlos Galán Sarmiento               | 100.7 MHz           | HJC95                 | Zonal                                   | Directa                                     | B                               | Zonal                                   |
| Bucaramanga     | UTS - Tu Radio Stereo                                       | 101.7 MHz           | HJC99                 | Zonal                                   | Directa                                     | C                               | Zonal                                   |
| Bucaramanga     | La Mega Estéreo                                             | 102.5 MHz           | HJQ66                 | Zonal                                   | Indirecta                                   | B                               | Zonal                                   |
| San Juan de Girón | Rumba Estéreo                                             | 103.7 MHz           | HJA83                 | Zonal                                   | Indirecta                                   | C                               | Zonal                                   |
| Floridablanca   | Bésame                                                      | 104.7 MHz           | HJYF                  | Zonal                                   | Indirecta                                   | C                               | Zonal                                   |
| Bucaramanga     | La Guapachosa 105.1                                         | 105.1 MHz           | HUJ95                 | Local Restringido                       | Indirecta                                   | D                               | Local Restringido                       |
| Piedecuesta     | Radio Uno                                                   | 106.7 MHz           | HJYC                  | Zonal                                   | Indirecta                                   | C                               | Zonal                                   |
| Floridablanca   | La U Radio                                                  | 107.1 MHz           | HKL21                 | Zonal Restringido                       | Indirecta                                   | D                               | Zonal Restringido                       |
| San Juan de Girón | Emisora Comunitaria San Juan de Girón                     | 88.2 MHz            | HKL24                 | Zonal Restringido                       | Indirecta                                   | D                               | Zonal Restringido                       |
| Floridablanca   | Emisora Comunitaria en Floridablanca                        | 88.8 MHz            | HJS57                 | Zonal                                   | Indirecta                                   | C                               | Zonal                                   |
| Bucaramanga     | W Radio                                                     | 90.7 MHz            | HJQ34                 | Zonal                                   | Indirecta                                   | B                               | Zonal                                   |
| Lebrija         | La Voz de Lebrija                                           | 91.2 MHz            | HKL36                 | Zonal Restringido                       | Indirecta                                   | B                               | Zonal Restringido                       |
| Bucaramanga     | Policía Nacional Bucaramanga                                | 91.9 MHz            | HJQ93                 | Zonal                                   | Directa                                     | B                               | Zonal                                   |
| Lebrija         | Radionica                                                   | 92.3 MHz            | HJZM                  | Zonal                                   | Directa                                     | C                               | Zonal                                   |
| Bucaramanga     | Colombia Estéreo                                            | 92.9 MHz            | HJA87                 | Zonal                                   | Directa                                     | A                               | Zonal                                   |
| Bucaramanga     | Emisora Comunitaria La Brújula - Área de Servicio No. 1     | 93.4 MHz            | HUJ94                 | Local Restringido                       | Indirecta                                   | D                               | Local Restringido                       |
| Bucaramanga     | Tropicana                                                   | 95.7 MHz            | HJNH                  | Zonal                                   | Indirecta                                   | B                               | Zonal                                   |
| Bucaramanga     | Santo Tomás Estéreo                                         | 96.2 MHz            | HJB91                 | Zonal                                   | Directa                                     | B                               | Zonal                                   |


**Fuente de respaldo (imagen oficial):**  
![Tabla Fase 1](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/main/imagenes/Mision_4/Tabla_Fase1.PNG)



## Fase 2: Monitoreo de Campo (Escaneo del Espectro)


## Fase 2: Monitoreo de Campo (Escaneo del Espectro)

Durante el barrido del espectro FM (88 – 108 MHz) con el SDR se detectaron las siguientes señales:

Como observación se añadió la señal encontrada en 96.9 que no se encontraba en la lista de la fase 1 pero apareció.

| Frecuencia nominal (MHz) | Frecuencia exacta (MHz) | Potencia relativa (dB) |
|---------------------------|--------------------------|-------------------------|
| 88.2 | No detectada | – |
| 88.8 | No detectada | – |
| 90.7 | 90.7 | -38.36 |
| 91.2 | No detectada | – |
| 91.7 | 91.7 | -24.37 |
| 92.3 | 92.3 | -54.82 |
| 92.9 | 92.9 | -45.24 |
| 93.4 | 93.4 | -47.35 |
| 94.7 | 94.7 | -65.51 |
| 95.7 | 95.7 | -43.59 |
| 96.2 | 96.2 | -68.14 |
| 96.9 | 96.9 | -46.91 |
| 100.7 | 100.7 | -55.56 |
| 101.7 | 101.7 | -64.35 |
| 102.5 | 102.5 | -53.60 |
| 103.7 | 103.7 | -56.36 |
| 104.7 | 104.7 | -55.25 |
| 105.1 | 105.1 | -73.47 |
| 106.7 | 106.7 | -65.95 |
| 107.7 | No detectada | – |

---


### Evidencias gráficas del barrido

#### 88.2 MHz
![88.2](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/88.2.jpg)  

#### 90.7 MHz
![90.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/90.7.jpg)  

#### 91.2 MHz
![91.2](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/91.2.jpg)  

#### 91.7 MHz
![91.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/91.7.jpg)  

#### 92.3 MHz
![92.3](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/92.3.jpg)  

#### 92.9 MHz
![92.9](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/92.9.jpg)  

#### 93.4 MHz
![93.4](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/93.4.jpg)  

#### 94.7 MHz
![94.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/94.7.jpg)  

#### 95.7 MHz
![95.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/95.7.jpg)  

#### 96.2 MHz
![96.2](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/96.2.jpg)  

#### 96.9 MHz
![96.9](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/96.9.jpg)  

#### 100.7 MHz
![100.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/100.7.jpg)  

#### 101.7 MHz
![101.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/101.7.jpg)  

#### 102.5 MHz
![102.5](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/102.5.jpg)  

#### 103.7 MHz
![103.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/103.7.jpg)  

#### 104.7 MHz
![104.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/104.7.jpg)  

#### 105.1 MHz
![105.1](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/105.1.jpg)  

#### 106.7 MHz
![106.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/106.7.jpg)  

#### 107.7 MHz
![107.7](https://raw.githubusercontent.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/main/imagenes/Mision_4/107.7.jpg)  


---


## Fase 3: Análisis y Cruce de Datos


**Señales detectadas en campo sin registro oficial** (añadidas a la tabla como TNI):

| Frecuencia Detectada (MHz) | Potencia relativa (dB) | Clasificación                      |
|---------------------------:|------------------------:|------------------------------------|
| 91.7                       | -24.37                 | Transmisión No Identificada (TNI)  |
| 94.7                       | -65.51                 | Transmisión No Identificada (TNI)  |
| 96.9                       | -46.91                 | Transmisión No Identificada (TNI)  |


Tabla comparativa entre la lista oficial (Fase 1) y el monitoreo de campo (Fase 2).

| Frecuencia Oficial (MHz) | Nombre Emisora (Oficial)               | Frecuencia Detectada (Campo) | Potencia relativa (dB) | Clasificación       | Código |
|--------------------------|----------------------------------------|------------------------------|------------------------|---------------------|--------|
| 88.2                     | Emisora Comunitaria San Juan de Girón  | No detectada                  | –                      | No detectada        | ND     |
| 88.8                     | Emisora Comunitaria en Floridablanca   | No detectada                  | –                      | No detectada        | ND     |
| 90.7                     | W Radio                                | 90.7                          | -38.36                 | Coincidencia Legal  | CL     |
| 91.2                     | La Voz de Lebrija                      | No detectada                  | –                      | No detectada        | ND     |
| 91.9                     | Policía Nacional Bucaramanga           | No detectada                  | –                      | No detectada        | ND     |
| 92.3                     | Radiónica                              | 92.3                          | -54.82                 | Coincidencia Legal  | CL     |
| 92.9                     | Colombia Estéreo                       | 92.9                          | -45.24                 | Coincidencia Legal  | CL     |
| 93.4                     | Emisora Comunitaria La Brújula         | 93.4                          | -47.35                 | Coincidencia Legal  | CL     |
| 95.7                     | Tropicana                              | 95.7                          | -43.59                 | Coincidencia Legal  | CL     |
| 96.2                     | Santo Tomás Estéreo                    | 96.2                          | -68.14                 | Coincidencia Legal  | CL     |
| 100.7                    | Emisora Cultural Luis Carlos Galán     | 100.7                         | -55.56                 | Coincidencia Legal  | CL     |
| 101.7                    | UTS - Tu Radio Stereo                  | 101.7                         | -64.35                 | Coincidencia Legal  | CL     |
| 102.5                    | La Mega Estéreo                        | 102.5                         | -53.60                 | Coincidencia Legal  | CL     |
| 103.7                    | Rumba Estéreo                          | 103.7                         | -56.36                 | Coincidencia Legal  | CL     |
| 104.7                    | Bésame                                 | 104.7                         | -55.25                 | Coincidencia Legal  | CL     |
| 105.1                    | La Guapachosa 105.1                    | 105.1                         | -73.47                 | Coincidencia Legal  | CL     |
| 106.7                    | Radio Uno                              | 106.7                         | -65.95                 | Coincidencia Legal  | CL     |
| 107.1                    | La U Radio                             | No detectada                  | –                      | No detectada        | ND     |

---

Durante el monitoreo de campo se detectaron tres señales inicialmente clasificadas como Transmisiones No Identificadas (TNI).  
Tras la verificación en fuentes externas, se identificó que corresponden a emisoras legalmente establecidas en Bucaramanga:

- **91.7 MHz – Radio Policía Bucaramanga**  
- **94.7 MHz – KV 94.7 FM**  
- **96.9 MHz – UIS Estéreo Bucaramanga**

Estas emisoras se incorporaron a la Tabla Maestra como **Coincidencias Legales (CL)**.  

---

### Tabla Maestra Comparativa

| Frecuencia Oficial (MHz) | Nombre Emisora (Oficial)               | Frecuencia Detectada (Campo) | Potencia relativa (dB) | Clasificación      | Código |
|--------------------------|----------------------------------------|------------------------------|------------------------|--------------------|--------|
| 88.2                     | Emisora Comunitaria San Juan de Girón  | No detectada                  | –                      | No detectada       | ND     |
| 88.8                     | Emisora Comunitaria en Floridablanca   | No detectada                  | –                      | No detectada       | ND     |
| 90.7                     | W Radio                                | 90.7                          | -38.36                 | Coincidencia Legal | CL     |
| 91.2                     | La Voz de Lebrija                      | No detectada                  | –                      | No detectada       | ND     |
| 91.7                     | Radio Policía Bucaramanga              | 91.7                          | -24.37                 | Coincidencia Legal | CL     |
| 91.9                     | Policía Nacional Bucaramanga (oficial) | No detectada                  | –                      | No detectada       | ND     |
| 92.3                     | Radiónica                              | 92.3                          | -54.82                 | Coincidencia Legal | CL     |
| 92.9                     | Colombia Estéreo                       | 92.9                          | -45.24                 | Coincidencia Legal | CL     |
| 93.4                     | Emisora Comunitaria La Brújula         | 93.4                          | -47.35                 | Coincidencia Legal | CL     |
| 94.7                     | KV 94.7 FM                             | 94.7                          | -65.51                 | Coincidencia Legal | CL     |
| 95.7                     | Tropicana                              | 95.7                          | -43.59                 | Coincidencia Legal | CL     |
| 96.2                     | Santo Tomás Estéreo                    | 96.2                          | -68.14                 | Coincidencia Legal | CL     |
| 96.9                     | UIS Estéreo Bucaramanga                | 96.9                          | -46.91                 | Coincidencia Legal | CL     |
| 100.7                    | Emisora Cultural Luis Carlos Galán     | 100.7                         | -55.56                 | Coincidencia Legal | CL     |
| 101.7                    | UTS - Tu Radio Stereo                  | 101.7                         | -64.35                 | Coincidencia Legal | CL     |
| 102.5                    | La Mega Estéreo                        | 102.5                         | -53.60                 | Coincidencia Legal | CL     |
| 103.7                    | Rumba Estéreo                          | 103.7                         | -56.36                 | Coincidencia Legal | CL     |
| 104.7                    | Bésame                                 | 104.7                         | -55.25                 | Coincidencia Legal | CL     |
| 105.1                    | La Guapachosa 105.1                    | 105.1                         | -73.47                 | Coincidencia Legal | CL     |
| 106.7                    | Radio Uno                              | 106.7                         | -65.95                 | Coincidencia Legal | CL     |
| 107.1                    | La U Radio                             | No detectada                  | –                      | No detectada       | ND     |



# 📡 Reporte de Misión – Monitoreo de Espectro FM Bucaramanga

## Resultados y Hallazgos

- Se realizó un cruce entre la **Lista Oficial de Emisoras (ANE)** y el **Monitoreo de Campo**, obteniendo la **Tabla Maestra Comparativa**.  
- Se detectaron **tres transmisiones inicialmente clasificadas como TNI**, pero tras verificación externa se confirmaron como **Coincidencias Legales (CL)**:  
  - 91.7 MHz – Radio Policía Bucaramanga  
  - 94.7 MHz – KV 94.7 FM  
  - 96.9 MHz – UIS Estéreo Bucaramanga  

**Tabla Maestra:**  
(Aquí insertas la tabla comparativa que ya hiciste en Fase 3).  

📷 **Captura de espectro panorámica:**  
*(Inserta aquí la imagen del escaneo de 88 a 108 MHz, señalando las principales emisoras detectadas).*  

---

## Análisis y Discusión

### Lista de Anomalías
- 88.2 MHz – Emisora Comunitaria San Juan de Girón  
- 88.8 MHz – Emisora Comunitaria en Floridablanca  
- 91.2 MHz – La Voz de Lebrija  
- 91.9 MHz – Policía Nacional Bucaramanga  
- 107.1 MHz – La U Radio  

### Análisis de Discrepancias
1. Transmisión fuera de operación temporalmente.  
2. Cobertura limitada o licencia en municipio cercano cuya señal no llega con suficiente potencia.  
3. Errores administrativos o registros desactualizados.  

### Análisis con Dispositivos Certificados
- Según el **Plan Técnico de Radiodifusión Sonora en FM**, cada emisora debe ocupar un ancho de canal de 200 kHz y mantener separación mínima de 400 kHz.  
- Las señales detectadas cumplen en general con estos parámetros.  
- Se recomienda verificar con analizador de espectro certificado el ancho de banda y potencia de las emisoras no detectadas.  

### Retos de la Misión
- Señales muy débiles (< -65 dB).  
- Ruido de fondo en la banda FM.  
- Monitoreo realizado en un solo horario (sin comparación entre franjas).  

---

## Conclusiones y Recomendaciones

### Conclusiones
- El espectro FM en Bucaramanga está mayormente en conformidad con los registros de la ANE.  
- Se identificaron cinco emisoras no detectadas, principalmente comunitarias o institucionales.  
- Las tres señales inicialmente clasificadas como TNI se verificaron como emisoras legales.  

### Recomendaciones
1. Realizar inspección en sitio para las frecuencias 88.2, 88.8, 91.2, 91.9 y 107.1 MHz.  
2. Repetir mediciones en distintos horarios para confirmar transmisiones intermitentes.  
3. Actualizar registros de emisoras comunitarias.  
4. Reportar a la Dirección de Vigilancia y Control de la ANE las emisoras no detectadas para posible investigación.  








