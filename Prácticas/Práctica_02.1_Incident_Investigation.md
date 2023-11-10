# Incident Investigation

![img01](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/25a8cfdcae5fa66e616d52d7da0f388bb8ef03b5/Pr%C3%A1cticas/img/img01.jpeg)

Trabajo realizado por: Antonio Peñalver Caro

# Índice

1. [Introducción](#introducción)
2. [Descripción del Incidente](#descripción-del-incidente)
3. [Proceso de Recolección de Evidencias por Orden de Volatilidad](#proceso-de-recolección-de-evidencias-por-orden-de-volatilidad)
4. [Proceso de Almacenamiento de Evidencias](#proceso-de-almacenamiento-de-evidencias)
5. [Metodología Seguida](#metodología-seguida)

# Introducción

En este proyecto, nos encontramos ante un incidente de seguridad ocurrido en el departamento de IT de nuestra empresa. Desde el departamento de CSIRT, nos encargaremos de averiguar lo que ha ocurrido siguiendo nuestra propia metodología, empezando por la adquisición de las distintas evidencias y terminando por el almacenamiento y el análisis de las mismas.

# Descripción del Incidente

Al llegar al lugar del incidente, nos encontramos con un equipo encendido. Lo primero que hicimos, fue desconectarle el cable ethernet para evitar que el problema se siguiese propagando por el resto de equipos de la red. Acto seguido, despejamos la zona de personas ajenas al caso y fotografiamos la escena para luego poder realizar una reconstrucción del mismo. Por último, nos sentamos frente al equipo para ver qué es lo que había ocurrido.

En el "Escritorio" del equipo se podían visualizar 3 cosas:

- Un mensaje que nos pedía reiniciar para poder aplicar unos cambios en el equipo. Evidentemente, clickamos sobre "Reiniciar más tarde" para no perder los datos volátiles de la máquina.

- Un par de ficheros, los cuales no abriremos hasta el proceso de análisis de las evidencias.

![img02](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img02.png)

A continuación, sacamos nuestras herramientas forenses y comenzamos con el proceso de recolección de evidencias.

# Proceso de Recolección de Evidencias por Orden de Volatilidad

En este proceso, nos regiremos por nuestra propia metodología: APINAG4. Según el apartado 2.1 de esta, el orden de volatilidad que debemos de seguir a la hora de realizar adquisiciones en dispostivos informáticos, es el siguiente:

- Registros y contenido de la caché.
- Tabla de enrutamiento, caché ARP, tabla de procesos, estadísticas del kernel y memoria.
- Información temporal del sistema.
- Disco.
- Logs del sistema.
- Configuración física y topología de la red.
- Documentos.

En este caso, vamos a realizar adquisiciones de la memoria RAM del sistema y del disco físico del equipo.

## Adquisición de Memoria

Para esta parte del proceso, escogeremos la herramienta Magnet Forensics, la cual es sencilla de utilizar y cumple con su cometido.

Lo único que le tenemos que indicar a esta herramienta, es la ruta donde queremos almacenar la captura de RAM. Una vez le hayamos indicado la ruta al programa, le daremos a "Start" para que este comience con la adquisición.

![img03](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img03.png)

Una vez haya finalizado, el programa nos mostrará la siguiente ventana:

![img04](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img04.png)

Por último, hashearemos la evidencia con HashMyFiles, lo cual nos servirá para preservar la integridad de la misma y la cadena de custodia.

![img05](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img05.png)

## Triage

En este proceso, nos interesa saber qué se hizo con la máquina antes, durante y después de la vulneración de la misma, por ello utilizaremos LastActivityView para poder sacar datos como:

- Inicios de sesión
- Instalación y ejecución de programas
- Carpeta Prefetch
- Creación de puntos de restauración
- Creación de archivos
- Etcétera

![img06](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img06.png)

Por último, hashearemos la evidencia con HashMyFiles, lo cual nos servirá para preservar la integridad de la misma y la cadena de custodia.

![img07](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img07.png)

## Adquisición de Disco

Para esta parte del proceso, escogeremos la herramienta FTK Imager, la cual nos servirá para recopilar toda la información contenida en el disco de la máquina vulnerada.

Lo primero que tendremos que indicarle al programa, es el tipo de fuente de evidencia del cual vamos a crear la imagen. En nuestro caso, nuestro tipo de fuente, es un dispositivo físico.

![img08](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img08.png)

A continuación, elegiremos el dispositivo físico del cual vamos a crear la imagen. En nuestro caso, la vamos a crear del disco duro de la máquina vulnerada.

![img09](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img09.png)

Ahora tendremos que elegir el tipo de imagen que queremos que se nos genere. En nuestro caso, vamos a generar una imagen completa del disco, bit a bit, por lo que elegiremos la primera opción.

![img10](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img10.png)

Ahora elegiremos un destino y un nombre para nuestra evidencia y clickaremos en "Finish".

![img11](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img11.png)

Por último, haremos check en las tres opciones que nos aparecen y clickaremos en "Start".

![img12](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img12.png)

A continuación, mostraremos al programa funcionando y mostrando como resultado los hashes de la imagen obtenida.

### Creando

![img13](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/12183b247d4d84e1c009ae9b3b17a8162389a246/Pr%C3%A1cticas/img/img13.png)

### Verificando

![img14](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/84f59d298a3b7172fac7c87d6671eb362c7de7de/Pr%C3%A1cticas/img/img14.png)

### Visualizando los hashes

![img15](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/373667f27acf16627947c22969d5dc1be435ade1/Pr%C3%A1cticas/img/img15.png)

# Proceso de Almacenamiento de Evidencias

En este proceso, también nos regiremos por nuestra propia metodología. Según el apartado 3 de esta, el proceso de almacenamiento es el siguiente:

- Copia de respaldo de la evidencia.
- Almacenar las evidencias en dispositivos cuya seguridad haya sido demostrada y que permita detectar intentos de acceso no autorizados.
- Cadena de custodia

## Copia de respaldo

A la hora de realizar la copia de respaldo de las distintas evidencias obtenidas, debemos de tener en cuenta lo siguiente:

- Asegurarnos de que la copia sea bit a bit.
- Usar algoritmos de hash, como SHA1 o MD5, para verificar la integridad de la segunda copia. Si los valores hash de ambas copias coinciden, entonces la integridad de la segunda copia está asegurada.
- Almacenar la segunda copia en un lugar seguro, tal y como haremos con la primera.
- Mantener un registro detallado de la cadena de custodia de las evidencias.

## Almacenamiento de las evidencias

Para el almacenamiento de las evidencias y de las copias de las mismas, utilizaremos un par de discos de 1TB. En el primer disco almacenenaremos las evidencias que sacamos directamente del equipo vulnerado y en el segundo, las copias de las mismas.

Ambos discos se almacenarán en una caja fuerte bajo llave hasta que llegue el momento de analizar las evidencias o haya que presentarlas en un juicio.

## Cadena de Custodia

### Identificación del Caso

| Entidad administrativa | Numero de caso | Lugar del incidente | Fecha y hora del incidente | Fotografía(s) |
|:---:|:---:|:---:|:---:|:---:|
| ¿Ciberseguros? G4.  | 01 | Departamento de IT | 06 de Noviembre de 2023 a las 08:00 GMT+1 | ![img16](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/3c9f94db203389c847c26cc5b05b813079c0948e/Pr%C3%A1cticas/img/img16.jpeg)  |

### Integridad de las Evidencias

|      Archivo       |      MD5 (Hash original)      |      MD5 (Hash verificado)      |      SHA1 (Hash original)      |      SHA1 (Hash verificado)      |      Verificado      |
|:------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|:--------------------:|
| Evidencia Memoria  | 25bd6c29839cf490c63ee4acdf84d38c |       No verificado       | f976e8df7e87bc2e2259bf5961b30750eff34ec4 |      No verificado      |         No         |
| Evidencia Triage   | ce190ec572528c9f19ae47a26aff5d00 |       No verificado       | 6002f665cbdab2dd0756defd17d913b4f1d50 |      No verificado      |         No         |
| Evidencia Disco    | 9efa101c907da0bc8de1021d3905bb1e | 9efa101c907da0bc8de1021d3905bb1e | 38b92851d3c8fb3d1be72d4ab21a72b0c87f2f64 | 38b92851d3c8fb3d1be72d | Sí |

### Acta de Adquisición

| Adquisición | Herramienta Usada    | Versión |
| :-:         | :-                   | :-      |
| RAM         | Magnet Forensics     | V 1.2.0  |
| Triage      | LastActivityView     | V 1.36   |
| Disco Duro  | FTK Imager           |         |

|         Adquisiciones              |                    Información                     |
|:----------------------------------:|:--------------------------------------------------:|
| Ubicación de las adquisiciones     |            Disco duro WD Blue SN570 1TB            |
| Fecha de las adquisiciones         |            08 de Noviembre de 2023                 |
| Método de adquisición              | Herramientas ejecutadas en live desde un USB.      |
| Método de traslado                 | Terrestre |
| ¿Se requieren condiciones especiales para su traslado? | No |
| Recomendaciones | No extraer el disco duro que contiene las evidencias hasta que no se encuentre en el laboratorio forense |
| Responsable de las adquisiciones | Antonio Peñalver Caro |

### Traspaso de Cadena de Custodia

| Identificación de la persona que entrega | Firma | Nombre de la persona que recibe | Firma | Propósito de la transferencia | Método de transferencia | Fecha de transferencia |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Antonio Peñalver Caro | ![Firma](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/c67c7f808b490d15925920471d573e24e0b397fa/Pr%C3%A1cticas/img/Firma.png)  | Manuel Rivas Sández | ![FirmaM](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/c67c7f808b490d15925920471d573e24e0b397fa/Pr%C3%A1cticas/img/FirmaM.png)  | Análisis de las evidencias en laboratorio forense  | Subida de evidencias a la nube (OneDrive) | 10 de Noviembre de 2023 |

# Metodología Seguida

La metodología seguida en esta fase del proyecto es la APINAG4, desarrollada por la propia empresa que ha sufrido el incidente. Su objetivo es proporcionar a los investigadores una guía para la recolección, almacenamiento y análisis de las diversas evidencias que pueden obtenerse de un dispositivo informático en una escena forense.
