# Drug Trafficking

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5feaf4bfe47bfea95b4d214f7b784acc4b275e8b/Pr%C3%A1cticas/img/img17.png" alt="img17"/>
</p>

Trabajo realizado por: Antonio Peñalver Caro

# Análisis

1. **Describe el entorno de trabajo que has escogido para realizar la actividad:**

Para llevar a cabo el análisis de las evidencias proporcionadas en esta actividad, utilizaré un equipo con las siguientes características:
- Marca: Lenovo
- Modelo: Ideapad 330
- Procesador: Intel Core I3-7020U
- Memoria: 2 Modules 4GB PC4-21300 DDR4
- Sistema operativo: Windows 10 Pro (64 bits)

Es importante que le desconectemos el cable de red para mantener un contacto mínimo con cualquier vía de salida de información al exterior de la máquina.

Las herramientas que utilizaremos para dicho análisis, serán:
- Autopsy
- RegRipper 3.0 Master
- WRR
- DCode
- (**CONTINUAR**)

2. **Describe, como mínimo, la información siguiente, relacionada con el sistema operativo instalado en el sistema informático que estás analizando:**
- **¿Qué tamaño tiene la partición a analizar?:**
   
  Size (Bytes)	2623832064

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img19.png" alt="img19"/>
</p>
   
- **Sistema y versión del sistema operativo instalado:**
  
  Sistema: Microsoft Windows XP
  
  Versión: 5.1

 <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img20.png" alt="img20"/>
</p>

- **Nombre del usuario y organización registrados:**

  Usuario Administrador: Jhon
  
  Organización registrada: home

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img21.png" alt="img21"/>
</p>

- **"Product ID" asociado al sistema:**

  76487-341-1072684-22504

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img22.png" alt="img22"/>
</p>

- **"Service Pack" instalado:**
     
  Service Pack 3

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img23.png" alt="img23"/>
</p>
     
- **Fecha y hora de instalación del sistema operativo:**
  
  18/04/2013 15:17:02

 <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img24.png" alt="img24"/>
</p>

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img25.png" alt="img25"/>
</p>

- **Fecha y hora del último "shutdown":**

  Mi., 19 Junio 2013 02:11:46 UTC

  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img26.png" alt="img26"/>
</p>
  
  <p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img27.png" alt="img27"/>
</p>
  
3) **Determina qué usuarios hay definidos en el sistema (sin contar con los usuarios definidos por defecto). Para cada uno de ellos encuentra, como mínimo, la información siguiente:**

- **Fecha y hora del último "logon" del usuario:**

| Nombre de Usuari@ | John | Ian | Jessy |
|:---------:|:---------:|:---------:|:---------:|
| **Último "Logon"** | 2013-03-28 03:10:49Z | 2013-04-25 02:06:52Z | 2013-04-23 02:18:56Z |

- **Fecha y hora del último cambio de contraseña:**

| Nombre de Usuari@ | John | Ian | Jessy |
|:---------:|:---------:|:---------:|:---------:|
| **Último Cambio Contraseña** | 2013-04-18 15:18:44Z | 2013-04-18 15:18:44Z | 2013-04-18 15:18:44Z |

<img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img28.png" alt="img28" alt="Descripción imagen 1" width="25%"/> <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img29.png" alt="Descripción imagen 2" width="25%"/> <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/5c02e601254eeb007980162f6712c87aca92acd5/Pr%C3%A1cticas/img/img30.png" alt="Descripción imagen 3" width="25%"/>

- **¿Existe alguna contradicción entre las fechas halladas en este apartado y el anterior?. En caso afirmativo, ¿a qué crees que puede ser debido?:**

Si, ya que la fecha de instalación del sistema, es posterior a la del último "logon" del usuario Jhon. Es posible que dicho usuario haya intentado modificar el registro o reinstalar el sistema sin haber formateado del todo el disco duro del equipo.

<p align="center">
  <img src="https://github.com/AntonioPC94/Analisis-Forense-23-24/blob/014db12b7a87908d25d23884752d4917fb6c81c3/Pr%C3%A1cticas/img/img18.png" alt="img18"/>
</p>




