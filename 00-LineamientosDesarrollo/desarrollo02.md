# Construcción del software


### 1. Control de versiones de código 
- Las aplicaciones satélites a BANTOTAL, deben utilizar el repositorio oficial de código fuente del Banco.
- Para código fuente que no es Genexus (Core Bantotal). Se deberá utilizar el repositorio oficial del Banco: GITLAB.


### Calidad de código fuente 
En esta sección están descritos lineamientos con respecto a la calidad del código fuente. 
 
Manejo de errores y excepciones
Las excepciones deben ser identificadas y gestionadas mediante mecanismos del lenguaje (por ejemplo, throw*, try catch*), y evitar códigos de error internos y salidas del sistema no esperado.
Se debe desarrollar el sistema, de forma tal, que aplique el principio de “falla segura”. Esto quiere decir que el sistema debe ser capaz de recuperarse automáticamente ante problemas tales como la desconexión de una base de datos, de un servicio Web o ante entradas de datos incorrectas por parte del usuario.
Para todos los casos se debe:


[Volver &ldca;](/README.md "Regresar a página principal")