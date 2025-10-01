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

| Municipio       | Nombre comercial de la Emisora                              | Frecuencia Asignada | Distintivo de Llamada | Clase de Emisora (Área de Servicio) | Clase de Emisora (Gestión de Servicio) | Clase de Emisora (PTNRS) |
|-----------------|-------------------------------------------------------------|---------------------|-----------------------|--------------------------------------|----------------------------------------|--------------------------|
| Bucaramanga     | Emisora Cultural Luis Carlos Galán Sarmiento               | 100.7 MHz           | HJC95                 | Zonal                                | Directa                                | B                        |
| Bucaramanga     | UTS - Tu Radio Stereo                                       | 101.7 MHz           | HJC99                 | Zonal                                | Directa                                | C                        |
| Bucaramanga     | La Mega Estéreo                                             | 102.5 MHz           | HJQ66                 | Zonal                                | Indirecta                              | Zonal                    |
| San Juan de Girón | Rumba Estéreo                                             | 103.7 MHz           | HJA83                 | Zonal                                | Indirecta                              | C                        |
| Floridablanca   | Bésame                                                      | 104.7 MHz           | HJYF                  | Zonal                                | Indirecta                              | C                        |
| Bucaramanga     | La Guapachosa 105.1                                         | 105.1 MHz           | HUJ95                 | Local Restringido                    | Indirecta                              | D                        |
| Piedecuesta     | Radio Uno                                                   | 106.7 MHz           | HJYC                  | Zonal                                | Indirecta                              | C                        |
| Floridablanca   | La U Radio                                                  | 107.1 MHz           | HKL21                 | Zonal Restringido                    | Indirecta                              | D                        |
| San Juan de Girón | Emisora Comunitaria San Juan de Girón                     | 88.2 MHz            | HKL24                 | Zonal Restringido                    | Indirecta                              | D                        |
| Floridablanca   | Emisora Comunitaria en Floridablanca                        | 88.8 MHz            | HJS57                 | Zonal                                | Indirecta                              | C                        |
| Bucaramanga     | W Radio                                                     | 90.7 MHz            | HJQ34                 | Zonal                                | Indirecta                              | Zonal                    |
| Lebrija         | La Voz de Lebrija                                           | 91.2 MHz            | HKL36                 | Zonal Restringido                    | Indirecta                              | B                        |
| Bucaramanga     | Policía Nacional Bucaramanga                                | 91.9 MHz            | HJQ93                 | Zonal                                | Directa                                | Zonal                    |
| Lebrija         | Radionica                                                   | 92.3 MHz            | HJZM                  | Zonal                                | Directa                                | C                        |
| Bucaramanga     | Colombia Estéreo                                            | 92.9 MHz            | HJA87                 | Zonal                                | Directa                                | A                        |
| Bucaramanga     | Emisora Comunitaria La Brújula - Área de Servicio No. 1     | 93.4 MHz            | HUJ94                 | Local Restringido                    | Indirecta                              | D                        |
| Bucaramanga     | Tropicana                                                   | 95.7 MHz            | HJNH                  | Zonal                                | Indirecta                              | B                        |
| Bucaramanga     | Santo Tomás Estéreo                                         | 96.2 MHz            | HJB91                 | Zonal                                | Directa                                | B                        |

---

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

Tabla maestra comparativa entre la lista oficial (Fase 1) y el monitoreo de campo (Fase 2).

| Frecuencia Oficial (MHz) | Nombre Emisora (Oficial)                                     | Frecuencia Detectada (Campo) | Potencia relativa (dB) | Clasificación |
|--------------------------:|--------------------------------------------------------------|------------------------------:|------------------------:|---------------|
| 88.2                      | Emisora Comunitaria San Juan de Girón                        | No detectada                  | –                       | No detectada  |
| 88.8                      | Emisora Comunitaria en Floridablanca                         | No detectada                  | –                       | No detectada  |
| 90.7                      | W Radio                                                      | 90.7                          | -38.36                  | Coincidencia Legal (CL) |
| 91.2                      | La Voz de Lebrija                                            | No detectada                  | –                       | No detectada  |
| 91.9                      | Policía Nacional Bucaramanga                                 | No detectada                  | –                       | No detectada  |
| 92.3                      | Radiónica                                                    | 92.3                          | -54.82                  | Coincidencia Legal (CL) |
| 92.9                      | Colombia Estéreo                                             | 92.9                          | -45.24                  | Coincidencia Legal (CL) |
| 93.4                      | Emisora Comunitaria La Brújula                               | 93.4                          | -47.35                  | Coincidencia Legal (CL) |
| 95.7                      | Tropicana                                                    | 95.7                          | -43.59                  | Coincidencia Legal (CL) |
| 96.2                      | Santo Tomás Estéreo                                          | 96.2                          | -68.14                  | Coincidencia Legal (CL) |
| 100.7                     | Emisora Cultural Luis Carlos Galán                           | 100.7                         | -55.56                  | Coincidencia Legal (CL) |
| 101.7                     | UTS - Tu Radio Stereo                                        | 101.7                         | -64.35                  | Coincidencia Legal (CL) |
| 102.5                     | La Mega Estéreo                                              | 102.5                         | -53.60                  | Coincidencia Legal (CL) |
| 103.7                     | Rumba Estéreo                                                | 103.7                         | -56.36                  | Coincidencia Legal (CL) |
| 104.7                     | Bésame                                                       | 104.7                         | -55.25                  | Coincidencia Legal (CL) |
| 105.1                     | La Guapachosa 105.1                                          | 105.1                         | -73.47                  | Coincidencia Legal (CL) |
| 106.7                     | Radio Uno                                                    | 106.7                         | -65.95                  | Coincidencia Legal (CL) |
| 107.1                     | La U Radio                                                   | No detectada                  | –                       | No detectada  |

**Señales detectadas en campo sin registro oficial** (añadidas a la tabla como TNI):

| Frecuencia Detectada (MHz) | Potencia relativa (dB) | Clasificación |
|---------------------------:|------------------------:|---------------|
| 91.7                       | -24.37                 | Transmisión No Identificada (TNI) |
| 94.7                       | -65.51                 | Transmisión No Identificada (TNI) |
| 96.9                       | -46.91                 | Transmisión No Identificada (TNI) |

