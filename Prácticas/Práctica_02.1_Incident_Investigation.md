# Incident Investigation

![img01](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/25a8cfdcae5fa66e616d52d7da0f388bb8ef03b5/Pr%C3%A1cticas/img/img01.jpeg)

Trabajo realizado por: Antonio Peñalver Caro

# Índice

1. [Introducción](#introducción)
2. [Descripción del Incidente](#descripción-del-incidente)
3. [Proceso de Recolección de Evidencias](#proceso-de-recolección-de-evidencias)
4. [Proceso de Almacenamiento de Evidencias](#proceso-de-almacenamiento-de-evidencias)
5. [Cadena de Custodia](#cadena-de-custodia)
6. [Metodología Seguida](#metodología-seguida)

# Introducción

En este proyecto, nos encontramos ante un incidente de seguridad ocurrido en una empresa particular. Desde ¿Ciberseguros? G4. nos encargaremos de averiguar lo que ha ocurrido siguiendo nuestra propia metodología, empezando por la adquisición de las distintas evidencias y terminando por el almacenamiento y el análisis de las mismas.

# Descripción del Incidente

Al llegar al lugar del incidente, nos encontramos con un equipo encendido. Lo primero que hicimos, fue desconectarle el cable ethernet para evitar que el problema se siguiese propagando por el resto de equipos de la red. Acto seguido, despejamos la zona de personas ajenas al caso y fotografiamos la escena para luego poder realizar una reconstrucción del mismo. Por último, nos sentamos frente al equipo para ver qué es lo que había ocurrido.

En el "Escritorio" del equipo se podían visualizar 3 cosas:

- Un mensaje que nos pedía reiniciar para poder aplicar unos cambios en el equipo. Evidentemente, clickamos sobre "Reiniciar más tarde" para no perder los datos volátiles de la máquina.

- Un par de ficheros, los cuales no abriremos hasta el proceso de análisis de las evidencias.

![img02](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img02.png)

A continuación, sacamos nuestras herramientas forenses y comenzamos con el proceso de recolección de evidencias.

# Proceso de Recolección de Evidencias

En este proceso, nos regiremos por nuestra propia metodología: APINA G4. Según el apartado 2.1 de esta, el orden de volatilidad que debemos de seguir a la hora de realizar adquisiciones en dispostivos informáticos, es el siguiente:

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

Lo único que le tenemos que indicar a esta herramienta, es la ruta donde queremos almacenar la captura de RAM. En nuestro caso, la almacenaremos en un disco duro externo. Una vez le hayamos indicado la ruta al programa, le daremos a "Start" para que comience con la adquisición.

![img03](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img03.png)

Una vez haya finalizado, el programa nos mostrará la siguiente ventana:

![img04](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img04.png)

Por último, hashearemos la evidencia con HashMyFiles, lo cual nos servirá para preservar la integridad de la misma y la cadena de custodia.

![img05](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/2decc698c6aa870ebe838c803bd180f1251e8647/Pr%C3%A1cticas/img/img05.png)

## Triage
Como en este caso nos interesa saber qué se hizo con la máquina antes, durante y después de la vulneración de la misma, utilizaremos LastActivityView para poder sacar datos como:

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

Lo primero que tendremos que indicarle al programa, (**CONTINUAR**)



# Proceso de Almacenamiento de Evidencias

# Cadena de Custodia

# Metodología Seguida
