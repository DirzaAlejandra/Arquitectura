# Anexo 1


### Estructura por proyecto: 
Debemos crear nuestro código con las capas del proyecto bien separadas e indicadas, comúnmente estas capas irán en forma de “librería” y deberán contener el nombre completo. ¿Esto que quiere decir?
En nuestro ejemplo, estamos trabajando en un proyecto llamado CNF y dentro de la web cnf, la API está dentro de lo que hemos denominado como “WebApi” por lo tanto el nombre completo de la api será Cnf.WebApi.
Y esto lo debemos hacer con TODOS nuestros proyectos, da igual en que “subproyecto” o apartado estemos ya que, de esa forma, introducimos una mayor claridad a la aplicación
![Ejemplo de la Estructura del Proyecto]
(./Images/Imagen1.png)

## Model
Principalmente debemos crear nuestro código que sea lo menos dependiente posible.
Por lo que debemos crear nuestro modelo, el modelo es la parte central de nuestro proyecto, donde definimos los tipos y debemos intentar que NO contenga dependencias externas, sobre todo a librerías de terceros. 
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará Cnf.Domain y dentro de este proyecto se creará la carpeta Modelo o Model, estas carpetas serán creadas acorde a necesidad del proyecto.
## DTO
Un objeto de transferencia de datos (en inglés: data transfer object, DTO) es un objeto que sirve para transportar datos entre procesos. Por lo que es necesario utilizar los DTO’s para representar los datos que queremos que los clientes de nuestra Web API reciban para no proporcionar información que representa el model y no es relevante para nuestros clientes que consumen los servicios de Banco Sol s.a.
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará Cnf.Application y dentro de este proyecto se creará la carpeta DTO, estas carpetas serán creadas acorde a necesidad del proyecto.
## Seguridad
Proyecto que se encargara de cifrar y descifrar las llaves configuradas en los archivos de configuración o appsettings.
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará Cnf.Seguridad y dentro de este proyecto se creará las clases respectivas.

## Shared Kernel
Núcleo compartido de código en común, el cual puede ser utilizado por los diferentes subproyectos del proyecto, es decir son objetos genéricos que no son modificadas en el tiempo.
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará SharedKernel y dentro de este proyecto se creará las carpetas, clases respectivas.
## Services
Proyecto que se encargara de invocar a los servicios de los cuales depende este proyecto para poder completar el flujo transaccional respectivo, como ejemplo en este proyecto deben estar las solicitudes al BtServices, NSBT, logs, otros.
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará Cnf.Services y dentro de este proyecto se creará las carpetas necesarias de acuerdo con la cantidad se integraciones entre servicios.
## Logs
Proyecto que se encarga de gestionar el registro de logs de la aplicación.
En nuestro ejemplo, este proyecto de biblioteca de clases se denominará Cnf.Logs y dentro de este proyecto se creará las carpetas, clases respectivas.
## Test
Es necesario la implementación de prueba unitarias de todo el proyecto, las pruebas unitarias o unit testing son una forma de comprobar que un fragmento de código funciona correctamente. Es un procedimiento más de los que se llevan a cabo dentro de una metodología ágil de trabajo.
- Las pruebas unitarias deberían ser independientes. Si se produce cualquier tipo de mejora o cambio en los requerimientos, las pruebas unitarias no deberían verse afectados.
- Prueba sólo un código a la vez.
- Sigue un esquema claro. Puede parecer algo secundario, pero no lo es. Sé también consistente a la hora de nombrar tus unit tests.
- Cualquier cambio necesita pasar el test. En el caso de producirse un cambio en el código de cualquier módulo, asegúrate de que hay una prueba unitaria que se corresponda con ese módulo y que este pasa las pruebas antes de cambiar la implementación.
- Corrige los bugs identificados durante las pruebas antes de continuar. Asegúrate de realizar esta corrección antes de proseguir con la siguiente fase del ciclo de vida del desarrollo de software.
- Acostúmbrate a realizar pruebas regularmente mientras programas. Cuanto más código escribas sin testar, más caminos tendrás que revisar para encontrar errores.


### Guía de Microsoft para la implementación de unit test en VS.
(https://learn.microsoft.com/es-es/visualstudio/test/getting-started-with-unit-testing?view=vs-2022&tabs=dotnet%2Cmstest)

En nuestro ejemplo, este proyecto de prueba unitarias se denominará Cnf.Test y dentro de este proyecto se creará las carpetas y clases respectivas.

## Message
Trata de la implementación de un servicio de mensajería que funciona como un middleware de mensajería, trabajando sobre el patrón productor / consumidor, para la implementación de este servicio se trabajara con RabbitMq que Implementa el estándar Advanced Message Queuing Protocol (AMQP).
En nuestro ejemplo, este proyecto de prueba unitarias se denominará Cnf.Message y dentro de este proyecto se creará las carpetas y clases respectivas.
## Web
Proyecto que contiene los controladores (métodos) de la API respectivamente.
En nuestro ejemplo, este proyecto de prueba unitarias se denominará Cnf.WebApi y dentro de este proyecto se creará las carpetas y clases respectivas.


[Volver &ldca;](/README.md "Regresar a página principal")