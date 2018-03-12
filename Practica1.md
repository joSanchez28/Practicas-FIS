# Practica 1. Ingeniería de requisitos. Lista inicial de requisitos

<!---
Partiendo de la descripción inicial del problema que se acaba de dar, se realizarán
las siguientes actividades:
1. Estudio del dominio del problema y descripción general del sistema.
2. Obtención de una lista estructurada de requisitos.
3. Glosario de términos.
-->

<!---
proporcionar atención médica completa a sus abonados,
incluyendo servicios de atención básica (consulta de médico de familia, farmacia,
consulta de enfermería, gestión de tratamientos de larga duración, …), atención
especializada (consulta de médicos especialistas, realización de pruebas médicas),
servicio de urgencias, …
El sistema debe
Entre otras funciones se debe permitir gestionar, como mínimo:

Gestión de enfermos y médicos.
Control de citas.
Gestión de pruebas médicas.
Gestión de instalaciones y aparatos de prueba médica.
Control de tratamientos.

-->


## 1. Descripción general del sistema

Este proyecto tiene como objetivo principal desarollar un sistema software para la gestión de un centro médico
privado. El sistema debe encargarse de la gestión de los pacientes, los distintos tipos de personal sanitario, y las
instalaciones existentes tanto a nivel médico como administrativo (empleados, horarios, registros, citas…).
El sistema acelerará el proceso de solicitud de servicios por parte del cliente y la organización y ejecución de los tratamientos oportunos por parte del personal sanitario. Por último facilitará un control óptimo sobre los recursos tanto humanos como técnicos.
La aplicación resultante se instalará en un hospital concreto y podrá ser usado por todo su personal y pacientes a través de diferentes plataformas (ordenador, smartphone, tablet...). Tras su prueba y correcto y óptimo funcionamiento podría plantearse la posibilidad de usarse en otros hospitales e incluso usarse como sistema generalizado en una red de hospitales.

A modo de resumen, los principales objetivos que se pretenden alcanzar con el producto son los siguientes:

  **OBJ-1**. El sistema deberá almacenar y gestionar la información relativa a los pacientes, registro de citas, horario de todo el personal del centro y control de recursos.

  **OBJ-2**. El sistema automatizará el proceso de solicitud de citas y realizará el control y planificación de servicios por parte del personal del centro.

  **OBJ-3**. Las actividades realizadas por los usuarios en el sistema podrán ser llevadas a cabo en tiempo real a través de la aplicación en su dispositivo móvil.



**Descripción de los implicados**

- **Entorno de usuario**

Los usuarios del producto a desarrollar son varios: paciente, médico, enfermero, auxiliar, celador, fisioterapeuta, personal de mantenimiento y personal administrativo. Su nivel cultural es medio-alto y tienen algo de experiencia en el uso de aplicaciones informáticas pero bastante experiencia en el negocio.

- ** Resumen de los implicados **

| Usuario | Descripción | Tipo | Responsabilidad |
| ------- | ----------- | ---- | --------------- |
| Paciente | Representa un paciente | Usuario sistema | Requerir y hacer uso responsable de servicios. Solicitar citas y/o tratamientos. |
| Médico | Representa un médico | Usuario producto | Dar citas, recetar medicamentos, llevar a cabo tratamientos. |
| Enfermero | Representa un enfermero | Usuario producto | Realizar curas, dar tratamiento directo, asistir a médicos. |
| Auxiliar | Representa un auxiliar | Usuario producto | Realizar mantenimiento del paciente.|
| Celador | Representa un celador | Usuario sistema | Realizar el transporte de pacientes. |
| Fisioterapeuta | Representa un fisioterapeuta | Usuario producto | Da sesiones, realiza rehabilitaciones. |
| Personal de mantenimiento | Representa un proveedor o un técnico | Usuario sistema | Realiza reparaciones y/o revisiones técnicas, suministra materiales. |
| Personal administrativos | Representa un administrativo | Usuario producto | Se encarga del gestión de recursos y/o materiales

- ** Principales necesidades de los implicados **

| Necesidad | Prioridad | Problema | Solución actual | Solución propuesta |
| --------- | --------- | -------- | --------------- | ------------------ |
| Gestión de citas | Alta | Tenemos que mantener la información en la base de datos sin errores | Registro llevado en papel | Ofrecer un registro informatizado completo |
| Mantener información respecto a los pacientes | Alta | Tenemos que constituir una base de datos completa y detallada del estado e historial de cada paciente | Información situada en un único lugar en formato físico, muy vulnerable. | Información muy actualizada con fácil acceso y posibilidad de recuperación de datos con copias de seguridad e información distribuida.|



## 2. Requisitos del sistema

### 2.1 Requisitos funcionales

1. **Gestión de citas**. El sistema deberá realizar una gestión de las diferentes citas médicas.
  - El sistema debe llevar un control de todas las citas que han sido concedidas, incluyendo paciente, personal sanitario y material necesarios, lugar y horario en el que se llevará a cabo. Esto incluye:
    - Citas médicas generales
    - Citas médicas con especialistas
    - Rehabilitación y fisioterapia
    - Citas de enfermería
    - Citas para pruebas médicas
    - Cirugía.
  - El sistema permitirá una gestión de las citas existentes permitiendo anularlas, aplazarlas o modificar cualquiera de sus datos.
  - El sistema debe permitir la solicitud de citas.
  - El sistema debe permitir la creación de nuevas citas a partir de una solicitud.
2. **Gestión de medicación**. El sistema debe permitir un control de la medicación para cada paciente.
  - El sistema debe controlar los medicamentos disponibles en el centro médico.
  - Debe permitir a un médico recetar una medicación.
  - Debe permitir gestionar la medicación que un paciente ingresado debe consumir.
3. **Historial del paciente**. El sistema debe permitir la gestión del historial de cada paciente.
  - El sistema debe permitir consultar y añadir información sobre el historial de enfermedades del paciente.
  - El sistema debe permitir consultar y añadir incidencias médicas ocurridas a un paciente en el centro sanitario.
  - El sistema debe permitir la expedición de valoraciones por tarde de médicos en caso de
    - Ingreso
    - Alta
    - Exitus (muerte del paciente)
  - El sistema debe permitir la gestión de los resultados de pruebas médicas y la consulta por parte del personal sanitario de las mismas (análisis, radiografías, espirometrías...)
4. **Incidencias técnicas**. El sistema debe permitir la gestión de incidencias técnicas en el material e instalaciones del centro médico.
  - El sistema debe permitir la comunicación entre el resto de usuarios y personal técnico.
  - El sistema debe permitir la creación de incidencias técnicas, incluyendo donde se producen y una descripción de las mismas.
  - El usuario debe permitir al personal técnico cerrar incidencias técnicas una vez solucionadas.
5. **Gestión de dietas**. El sistema debe permitir la gestión de dietas alimenticias en el centro.
  - Incluye gestión de dietas para pacientes ingresados, teniendo en cuenta alergias e incompatibilidades con medicación o enfermedades.
  - Incluye dietas para trabajadores del centro.
  - Debe permitir la solicitud de comidas, así como la notificación de que están listas.
6. **Gráfica de constantes**. El sistema debe permitir la gestión de datos vitales de los pacientes.
  - Seguimiento de temperatura del paciente.
  - Seguimiento de frecuencia cardiaca del paciente.
  - Seguimiento de tensión arterial del paciente.
  - Seguimiento de saturación de oxígeno del paciente.
  - Seguimiento de glucemia.
  - Debe permitir el acceso a estos datos por parte del personal sanitario.
7. **Agenda del trabajador**. El sistema debe permitir la gestión de una agenda para cada trabajador incluyendo
  - Turnos de trabajo de cada trabajador.
  - Tareas a realizar diariamente por el trabajador.


### 2.2 Requisitos no funcionales
#### Usabilidad
**RN-1.** Se deberá proporcionar ayuda en línea para que el usuario en todo momento
sepa que debe de hacer para conseguir su objetivo (obtener una cita,etc)

**RN-2.** Ya que para acceder se necesitará estar registrado deben aparecer avisos,
recomendaciones... para que el paciente no olvide su cita, recordar plazos de pago,
alertar sobre requerimientos de información personal por parte del hospital...

**RN-3.** El sistema en general debe de ser suficientemente sencillo para el usuario
de forma que cualquier persona sea capaz de familiarizarse con el entorno del
sistema en menos de 2 horas.

#### Fiabilidad
**RN-4.** Cada vez que cualquier información sea modificada en la base de datos debe
de ser actualizada a su vez para el usuario en menos de 5 segundos.

**RN-5.** Para prevenir la pérdida de datos de vital importancia se harán copias de
seguridad en determinados intervalos de tiempo en función de la cantidad de
información que sea modificada.

#### Rendimiento
**RN-6.** El sistema tiene que ser capaz de procesar N transaciones de cualquier tipo por
segundo.

**RN-7.** Cualquier funcionalidad del sistema debe responder a la petición del usuario
en menos de 5 segundos.

**RN-8.** El sistema debe de ser capaz de operar de forma correcta con 50 000 usuarios
con sesiones concurrentes.

**RN-9.** Para peticiones de mayor importancia que requieran respuesta inmediata como petición de
citas... el sistema proporcionará acceso rápido a dichas acciones.

**RN-10.** El tamaño del almaciento de datos será entre 10 y 25 TeraBytes, con posibilidad
de ampliación si es necesario.

#### Soporte
**RN-10.** El sistema debe adaptarse para poder ser utlizado desde distintos dispositivos
desde los mas básicos hasta los mas complejos.

**RN-11.** Habrá personal técnico cualificado encargado de mantener el sistema para
mantenerlo renovado y evitar o solucionar posibles fallos.

#### Implementación
**RN-12.** Se deberá usar el lenguaje Java compatible con jsdk1.4.2 y SQL (Oracle) para
la base de datos.

**RN-13.** El sistema deberá interactuar y recoger datos de los proveedores vía Internet,
conectándose a las páginas que éstos ofrecen.

#### Requisitos físicos
**RN-14.** Bunker de servidores contenedores de toda la base de datos.

#### Empaquetado
**RN-15.** El número de instalacines que se preveén ronda enterno a las 200 000.

#### Legales
**RN-16.** El tiempo medio de descarga e instalación no debe superar los 7 minutos.

**RN 17.** El sistema utilizara software libre en todo momento accesible para cualquier
usuario.

#### Seguridad
**RN-18.** Determinados datos de la base de datos deben estar almacenados de tal forma
que garanticen su privacidad en todo momento. Así como estará prohibido usar
información privada para fines no autorizados.


### 2.3 Requisitos de información
#### RI-1 Clientes dados de alta
Toda la información que necesitaremos del cliente para tratarlo y gestionarlo de forma efectiva.
Contenido: Datos de identificación del cliente(DNI, Nombre y Nº de la Seguridad social),
información en cuanto a su estado de salud y su historial médico(enfermedades y datos de pruebas realizadas),
médico de familia asignado(el que preferiblemente le pasará consulta),
formas de contacto(e-mail y teléfono), cuenta bancaria y deuda con la compañía(si no ha hecho algún pago).
#### RI-2 Empleados administrativos
Información de los profesionales administrativos que trabajan para la compañía/hospital.
Contenido: Sueldo, cuenta del banco, telefono y e-mail, DNI y
nombre de su profesión.
#### RI-3 Médicos
Información de cada uno de los médicos que trabajan para la compañía/hospital.
Contenido: Sueldo, cuenta del banco, telefono y e-mail, DNI, especialidad, Nº de médico,
operaciones y consultas pendientes.
#### RI-3 Enfermeros
Información de cada uno de los enfermeros que trabajan para la compañía/hospital.
Contenido: Sueldo, cuenta del banco, telefono y e-mail, DNI, planta en la que trabaja, Nº de enfermero.
#### RI-5 Hospitales
Información necesaria para la gestión del hospital.
Contenido: Personal empleado en el hospital, número de camas y habitaciones (tanto el total como las disponibles),
pacientes internados, horario de urgencias(si es que tiene), consultas y quirófanos.
#### RI-6 Operaciones y consultas
Información relativa a las operaciones y sus implicados.
Contenido: Tipo de operación o consulta, Nº de médico que la realiza, DNI de paciente y Nº de quirófano o consulta.
#### RI-7 Medicamentos
Información sobre los medicamentos con los que se trabaja.
Contenido:Tipo, descripción, cantidad de la que se dispone, pedidos realizados.
#### RI-8 Proveedores
Información sobre los distintos proveedores a los que se pueden pedir medicamentos o utensilios.
Contenido: Productos que proveen, datos de identificación(NIF) y bancarios(Nº de cuenta) y pedidos.



## 3. Glosario de términos







<!---Atención báscica:
        - consulta de médico de familia
        - farmacia
        - consulta  de  enfermería
        - gestión  de tratamientos  de  larga  duración
        - ...
     Atención especializada:
        - consulta de médicos especialistas
        - realización de pruebas médicas)
        - servicio de urgencias
        - ...
-->
