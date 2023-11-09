# Incident Investigation

![img01](https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/25a8cfdcae5fa66e616d52d7da0f388bb8ef03b5/Pr%C3%A1cticas/img/img01.jpeg)

Trabajo realizado por: Antonio Peñalver Caro

# Índice

1. [Introducción](#introducción)
2. [Descripción del Incidente](#descripción_del_incidente)
3. [Proceso de Recolección de Evidencias](#proceso_de_recolección_de_evidencias)
4. [Proceso de Almacenamiento de Evidencias](#proceso_de_almacenamiento_de_evidencias)
5. [Cadena de Custodia](#cadena_de_custodia)
6. [Metodología Seguida](#metodología_seguida)

# Introducción

En este proyecto, nos encontramos ante un incidente de seguridad ocurrido en una empresa particular. Desde ¿Ciberseguros? G4. nos encargaremos de averiguar lo que ha ocurrido siguiendo nuestra metodología, empezando por la adquisición de las distintas evidencias y terminando por el almacenamiento y el análisis de las mismas.

# Descripción del Incidente

Al llegar al lugar del incidente, nos encontramos con un equipo encendido. Lo primero que hicimos, fue desconectar el cable de red de la máquina para evitar que el problema se siguiese propagando por los distintos equipos de la red. Acto seguido, despejamos la zona de personas ajenas al caso y fotografiamos la escena para luego poder realizar una reconstrucción del caso. Y por último, nos sentamos frente al equipo para ver qué es lo que había ocurrido.

En el "Escritorio" del equipo, salía un mensaje que nos pedía reiniciar para poder aplicar unos cambios en el equipo. Evidentemente, clickamos sobre "Reiniciar más tarde" para no perder los datos volátiles de la máquina.

![img02]()

Una vez quitado el mensaje, sacamos nuestras herramientas forenses para poder comenzar con el proceso de recolección de evidencias.

# Proceso de Recolección de Evidencias

En este proceso, nos regiremos por nuestra propia metodología: APINA G4. Según el apartado 2.1 de esta, el orden de volatilidad que debemos de seguir a la hora de realizar adquisiciones en dispostivos informáticos, es el siguiente:

- Registros y contenido de la caché.
- Tabla de enrutamiento, caché ARP, tabla de procesos, estadísticas del kernel y memoria.
- Información temporal del sistema.
- Disco.
- Logs del sistema.
- Configuración física y topología de la red.
- Documentos.

Pero en este caso, vamos a realizar adquisiciones de la memoria RAM del sistema y del disco físico del equipo.

## Adquisición de Memoria

Para esta parte del proceso, escogeremos la herramienta Magnet Forensics, la cual es sencilla de utilizar y cumple con su cometido.

Lo único que le tenemos que indicar a esta herramienta, es la ruta donde queremos almacenar la captura de RAM. En nuestro caso, la almacenaremos en un disco duro externo. Una vez le hayamos indicado la ruta al programa, le daremos a "Start" para que comience con la adquisición.

![img03]()

Una vez haya finalizado, el programa nos mostrará la siguiente ventana:

![img04]()

(**CONTINUAR**)

## Triage

## Adquisición de Disco

Para esta parte del proceso, escogeremos la herramienta FTK Imager, la cual nos servirá para recopilar toda la información contenida en el disco de la máquina vulnerada. 

(**CONTINUAR**)



# Proceso de Almacenamiento de Evidencias

# Cadena de Custodia

# Metodología Seguida
