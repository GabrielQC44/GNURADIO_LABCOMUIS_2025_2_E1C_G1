# GNURADIO_LABCOMUIS_2025_2_E1C_G1
Repositorio de laboratorio de Comunicaciones I . Presentado por : Gabriel Camilo Quijano Celis y Carlos Daniel Aguilera Iglesias


# Misión 6: Nuestra Propia Emisora FM Estéreo

### Contexto

La emisora local ha quedado impresionada con la demostración de la superioridad de la Frecuencia Modulada. Ahora, el siguiente desafío es llevar la transmisión a un nivel profesional. Se le ha encomendado al equipo de ingeniería implementar una transmisión FM estéreo completa, similar a la que cualquier radio comercial utiliza. El objetivo es crear un pequeño bloque de programación para ser transmitido en el campus universitario, que pueda ser sintonizado por cualquier receptor de radio FM estándar.


## Fase 1 – Creación del bloque de programación

### Objetivo general
Diseñar y producir un bloque de programación de entre 60 y 90 segundos que combine elementos de audio como introducción, locución y música, destinado a su posterior transmisión en FM estéreo.


### Contexto
En esta fase se desarrolla el material sonoro base para una emisora temática de fútbol llamada "Radio Gol Colombia FM".  
El propósito es crear un bloque de programación corto, con formato profesional, que combine voz, efectos y música, simulando una emisora deportiva real que transmite resúmenes y noticias del Fútbol Profesional Colombiano.

### Objetivo general
Diseñar y producir un bloque de programación de entre 60 y 90 segundos que combine elementos de audio como introducción, locución y música, destinado a su posterior transmisión en FM estéreo.

---

### Objetivos específicos

#### 1.1 Diseñar un guion para un bloque de programación de 60 a 90 segundos que incluya introducción (jingle), voz y pieza musical.

**Guion del bloque de programación:**

Arranca la emoción del fútbol profesional colombiano.  
Estás escuchando Radio Gol Colombia, 90.5 FM, donde la pasión del balón se vive al máximo.  

La fecha catorce de la Liga BetPlay 2-2025 nos deja a Atlético Bucaramanga como líder con veintisiete puntos, seguido de cerca por Junior de Barranquilla con veinticinco.  
La lucha por los ocho sigue encendida y cada partido cuenta. ¡Y qué jornada vivimos!  

El Bucaramanga se impuso dos a uno frente a Envigado con goles de Fabián Sambueza y Luciano Pons, asegurando el primer lugar del torneo.  
Mientras tanto, Millonarios venció al América de Cali y Nacional empató con Tolima en un duelo vibrante.  

Con estos resultados, los ya clasificados a los cuadrangulares son: Bucaramanga, Junior, Fortaleza, Medellín y Atlético Nacional.  
Pero Cali, Santa Fe y Once Caldas todavía sueñan con entrar al grupo de los ocho.  
Cada punto vale oro en este cierre de campeonato.  

Y atención a la próxima fecha.  
Medellín recibe a Fortaleza, Deportivo Pasto enfrenta a Atlético Nacional y el partido más esperado: Millonarios contra Bucaramanga, duelo directo por la cima.  

Síguenos en redes como @RadiogolColombia y revive cada jugada con nuestra señal.  
Radio Gol Colombia FM. La pasión del FPC se escucha aquí.

---

#### 1.2 Grabar y/o seleccionar los elementos de audio definidos en el guion.

Para la grabación de la voz principal se utilizó la plataforma ElevenLabs, empleando una voz con tono deportivo y ritmo natural de narrador radial.  
Posteriormente se añadieron efectos de transición y pistas musicales de fondo con temática futbolera para darle energía al bloque.  
El montaje se realizó cuidando la sincronización entre voz y música, manteniendo una duración total cercana a los 80 segundos.

---

#### 1.3 Utilizar un software de edición de audio para ensamblar, mezclar y masterizar los elementos.

Se utilizó Audacity para editar y ensamblar todos los componentes de audio.  
En este programa se aplicaron ajustes de ecualización, mezcla estéreo y control de volumen, con el fin de mantener claridad en la voz y presencia en la música.  
El resultado final fue exportado en formato .wav estéreo, con dos canales (izquierdo y derecho) para preservar la calidad de la señal y permitir su posterior transmisión en FM estéreo.



## Fase 2 – Generación de la señal MPX estéreo


El siguiente es el esquema completo del sistema:  
![Diagrama completo](https://github.com/GabrielQC44/GNURADIO_LABCOMUIS_2025_2_E1C_G1/blob/misión_6/imagenes/Misión_6/Diagrama_Completo.jpg)

A continuación se explicará, paso a paso, cada bloque del esquema siguiendo los objetivos específicos.



### Objetivos específicos

#### 2.1 Cargar el archivo de audio estéreo en el entorno de desarrollo (GNU Radio)





#### 2.2 Implementar los bloques o el código necesario para generar los componentes de la señal MPX




#### 2.3 Combinar (sumar) las tres señales anteriores para formar la señal MPX final




#### 2.4 Analizar el espectro de la señal MPX resultante y verificar la correcta ubicación y amplitud relativa de cada uno de sus componentes




## Fase 3:

### Objetivos específicos


#### 3.2 Configurar los parámetros del USRP (frecuencia central de transmisión, ganancia, tasa de muestreo) para emitir la señal en una frecuencia libre dentro de la banda FM comercial (88-108 MHz).


#### 3.3: Iniciar la transmisión y utilizar un receptor de radio FM comercial para sintonizar la señal.


#### 3.4: Validar cualitativamente la calidad del audio recibido y confirmar que el indicador "Stereo" del receptor se activa, lo que prueba la correcta generación y detección del piloto de 19 kHz.







