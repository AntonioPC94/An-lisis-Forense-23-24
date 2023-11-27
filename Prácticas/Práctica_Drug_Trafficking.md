# Drug Trafficking

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5feaf4bfe47bfea95b4d214f7b784acc4b275e8b/Pr%C3%A1cticas/img/img17.png" alt="img17"/>
</p>

Trabajo realizado por: Antonio Peñalver Caro

#

# Índice
1. [Especificaciones Equipo Perito](#especificaciones-equipo-perito)
2. [Información General Equipo Decomisado](#información-general-equipo-decomisado)
3. [Caso 1: Tráfico de Drogas](#caso-1-tráfico-de-drogas)
4. [Caso 2: Pornografía](#caso-2-pornografía)

# Especificaciones Equipo Perito

1. **Describe el entorno de trabajo que has escogido para realizar la actividad:**

Para llevar a cabo el análisis de las evidencias proporcionadas en esta actividad, utilizaré un equipo con las siguientes características:
- Marca: Lenovo
- Modelo: Ideapad 330
- Procesador: Intel Core I3-7020U
- Memoria: 2 Modules 4GB PC4-21300 DDR4
- Sistema operativo: Windows 10 Pro (64 bits)

Nota: Es importante que le desconectemos el cable de red para mantener un contacto mínimo con cualquier vía de salida de información al exterior de la máquina.

# Información General Equipo Decomisado

2. **Describe, como mínimo, la información siguiente, relacionada con el sistema operativo instalado en el sistema informático que estás analizando:**

- **¿Qué tamaño tiene la partición a analizar?:**
   
  Mirando en las propiedades de la partición principal del sistema, pude encontrar el tamaño de la misma.

  Size (Bytes)	2623832064

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img19.png" alt="img19"/>
</p>

  **Herramienta utilizada**: Autopsy 4.21.0
   
- **Sistema y versión del sistema operativo instalado:**

  Analizando el registro SOFTWARE, conseguí sacar el sistema operativo instalado y la versión del mismo.
  
  Sistema: Microsoft Windows XP
  
  Versión: 5.1

 <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img20.png" alt="img20"/>
</p>

**Herramientas utilizadas**: Autopsy 4.21.0 y WRR 1.6.1.0

- **Nombre del usuario y organización registrados:**

  Analizando el registro SOFTWARE, conseguí sacar el usuario administrador del sistema y la organización registrada.

  Usuario Administrador: Jhon
  
  Organización registrada: home

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img21.png" alt="img21"/>
</p>

  **Herramientas utilizadas**: Autopsy 4.21.0 y WRR 1.6.1.0

- **"Product ID" asociado al sistema:**

  Analizando el registro SOFTWARE, conseguí sacar el "Product ID" asociado al sistema.

  76487-341-1072684-22504

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img22.png" alt="img22"/>
</p>

  **Herramientas utilizadas**: Autopsy 4.21.0 y WRR 1.6.1.0

- **"Service Pack" instalado:**

  Analizando el registro SOFTWARE, conseguí sacar el service pack instalado.
     
  Service Pack 3

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img23.png" alt="img23"/>
</p>

  **Herramientas utilizadas**: Autopsy 4.21.0 y WRR 1.6.1.0
     
- **Fecha y hora de instalación del sistema operativo:**

   Analizando el registro SYSTEM, conseguí sacar la fecha y hora de instalación del sistema operativo.
  
  18/04/2013 15:17:02

 <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img24.png" alt="img24"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img25.png" alt="img25"/>
</p>

**Herramientas utilizadas**: Autopsy 4.21.0 y WRR 1.6.1.0

- **Fecha y hora del último "shutdown":**

  Analizando el registro SYSTEM, conseguí sacar la fecha y hora del último "shutdown".

  Mi., 19 Junio 2013 02:11:46 UTC

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img26.png" alt="img26"/>
</p>

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img27.png" alt="img27"/>
</p>

**Herramientas utilizadas**: Autopsy 4.21.0 y DCode 4.02a
  
3) **Determina qué usuarios hay definidos en el sistema (sin contar con los usuarios definidos por defecto). Para cada uno de ellos encuentra, como mínimo, la información siguiente:**

- **Fecha y hora del último "logon" del usuario:**

| Nombre de Usuari@ | John | Ian | Jessy |
|:---------:|:---------:|:---------:|:---------:|
| **Último "Logon"** | 2013-03-28 03:10:49Z | 2013-04-25 02:06:52Z | 2013-04-23 02:18:56Z |

- **Fecha y hora del último cambio de contraseña:**

| Nombre de Usuari@ | John | Ian | Jessy |
|:---------:|:---------:|:---------:|:---------:|
| **Último Cambio Contraseña** | 2013-04-18 15:18:44Z | 2013-04-18 15:18:44Z | 2013-04-18 15:18:44Z |

Analizando el registro SAM, conseguí sacar la fecha y hora tanto del último "logon" de cada usuario, como del último cambio de contraseñas realizado en cada cuenta.

<p align="center">
<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img28.png" alt="img28" alt="Descripción imagen 1" width="25%"/> <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img29.png" alt="Descripción imagen 2" width="25%"/> <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img30.png" alt="Descripción imagen 3" width="25%"/>
</p>

**Herramientas utilizadas**: Autopsy 4.21.0 y RegRipper 3.0 Master

- **¿Existe alguna contradicción entre las fechas halladas en este apartado y el anterior?. En caso afirmativo, ¿a qué crees que puede ser debido?:**

Si, ya que la fecha de instalación del sistema, es posterior a la del último "logon" del usuario Jhon. Es posible que dicho usuario haya intentado modificar el registro o reinstalar el sistema sin haber formateado del todo el disco duro del equipo.

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/014db12b7a87908d25d23884752d4917fb6c81c3/Pr%C3%A1cticas/img/img18.png" alt="img18"/>
</p>

# Caso 1: Tráfico de drogas

4) **Localiza, extrae y relaciona los siguientes hallazgos, asociándose, si es posible, al usuario al cual pertenecen:**

- Localización y extracción de archivos eliminados.

  ## Deleted Files
  
  En los "Deleted Files" del sistema, encontré los siguientes archivos fotográficos relacionados con el caso que estoy investigando:
  
  - Imágenes nombradas como: "Almacen mataro 2.jpg", "Almacen mataro 3.jpg", "Almacen mataro.jpg, "Almacen terrassa 3.jpg", "Almacen terrassa 4.jpg", "Almacen terrassa.jpg",     "coca.jpg", "fabricando coca 2.jpg", "fabricando coca 3.jpg", "fabricando coca 4.jpg", "fabricando coca.jpg", "fiesta Jorge.jpg", "kasius 2.jpg", "kasius.jpg", "Maria en     negocio Jorge.jpg", "mercancia 2.jpg", "Mercancia terrassa.jpg", "mercancia.jpg", "pastillas.jpg" y "proceso final.jpg".

    En dichas imágenes, aparecen por ejemplo, varias personas consumiendo sustancias estupefacientes, un par de recetas que muestran el proceso de fabricación de la cocaína,     etcétera.

  **MIRAR METADATOS Y PONER INFORMACIÓN AL RESPECTO**

    **Véanse dichas imágenes en el anexo adjunto a este informe: **CREAR ENLACE AL DOCUMENTO** --> Anexo01DrugTrafficking.md, apartado "Deleted Files" (Imágenes 1-20)**

    Nota: Las imágenes también las podemos encontrar en los "$OrphanFiles" del sistema.
  
- Documentos y archivos fotográficos relacionados con presuntas conductas delictivas.

  ## Usuario: Jhon

  ## Carpeta RECYCLER

  En el directorio "RECYCLER", aparte de encontrar archivos fotográficos relacionados con el caso que estoy investigando, encontré también otros archivos          relacionados con otro caso, pero estos los analizaré más adelante.

  - Imágenes nombradas como: "20130329_140030.jpg", "20130329_140033.jpg" y "20130329_140035.jpg".

    Las imágenes anteriores muestran varias perspectivas de un mismo edificio, el cual parece ser su centro de operaciones.

  - Imagen nombrada como: "store plane.gif".

    La imagen anterior muestra el plano de un edificio, que posiblemente sea del edificio que mostré anteriormente.

========================================================================================================================================================================================

- ¿Los ficheros fotográficos contienen algún tipo de metadatos?. En caso afirmativo, ¿qué información te permiten obtener?
- Hojas de cálculo.
- Ficheros comprimidos.
- ¿Has localizado algún fichero con contraseña? ¿Has podido acceder a su contenido?
- Estudio de la navegación a través de internet: históricos de internet, URLs favoritas, búsquedas, etc.

# Caso 2: Pornografía

5) ¿Has podido localizar alguna otra evidencia relacionada con algún otro tipo delictivo?. En caso afirmativo, describe y extrae los hallazgos localizados, y determina y lleva a cabo aquellas acciones que realizarías en calidad de perito (puedes utilizar, coomo guión, los apartados de la pregunta 4).





