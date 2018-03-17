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

Este proyecto tiene como objetivo principal desarrollar un sistema software para la gestión de un centro médico
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

- **Resumen de los implicados**

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

- **Principales necesidades de los implicados**

| Necesidad | Prioridad | Problema | Solución actual | Solución propuesta |
| --------- | --------- | -------- | --------------- | ------------------ |
| Gestión de citas | Alta | Tenemos que mantener la información en la base de datos sin errores así como ofertar la posibilidad de gestionar citas. | Registro llevado en papel | Ofrecer un registro informatizado completo |
| Registro de pacientes | Alta | Tenemos que constituir una base de datos completa y detallada del estado e historial de cada paciente que pueda ser modificada con facilidad por el personal sanitario. | Información situada en un único lugar en formato físico, muy vulnerable además de restrictiva a la hora de modificar la información. | Información muy actualizada con fácil acceso y posibilidad de recuperación de datos con copias de seguridad e información distribuida.|
| Registro y gestión de personal | Media | Tenemos que crear y mantener registros sobre los turnos, especialidad o función así como su información administrativa del personal que facilite y optimice la organización de los mismos. | Información no disponible o registrada en papel por el propio personal. | Registro informatizado disponible desde cualquier dispositivo inteligente con posibilidad de modificar el registro.  Información actualizada con fácil acceso y protección de datos. |
| Registro y gestión de los recursos y/o materiales | Media | Tenemos que crear y mantener actualizados registros sobre el material y recursos del hospital, que facilite su gestión y mediante el cual se puedan hacer pedidos o solicitudes de material y/o reparaciones. | Información registrada en libros de administración con control de registros en agendas o calendarios físicos. Muy vulnerables y sin facilidad de acceso a la información. | Registro informatizado disponible desde cualquier dispositivo inteligente con posibilidad de modificar el registro además de crear nuevos recordatorios y hacer solicitudes. Información actualizada con fácil acceso y protección de datos.



## 2. Requisitos del sistema

### 2.1 Requisitos funcionales

1. **Gestión de citas**. El sistema deberá realizar una gestión de las diferentes citas médicas.
  - El sistema debe llevar un control de todas las citas que han sido concedidas, incluyendo paciente, personal sanitario y material necesarios, lugar y horario en el que se llevará a cabo. Esto incluye:
    - Citas médicas generales
    - Citas médicas con especialistas
    - Rehabilitación y fisioterapia
    - Citas de enfermería
    - Citas para pruebas médicas
    - Cirugía
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
sepa que debe de hacer para conseguir su objetivo (obtener una cita,etc).

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
**RN-12.** Se deberá usar el lenguaje Java compatible con jsdk1.4.2 y SQL para
la base de datos.

**RN-13.** El sistema deberá interactuar y recoger datos de los proveedores vía Internet,
conectándose a las páginas que éstos ofrecen.

#### Requisitos físicos
**RN-14.** Bunker de servidores contenedores de toda la base de datos.

#### Empaquetado
**RN-15.** El número de instalaciones que se preveén ronda entorno a las 200 000.

#### Legales
**RN-16.** El tiempo medio de descarga e instalación no debe superar los 7 minutos.

**RN-17.** El sistema utilizara software libre en todo momento accesible para cualquier
usuario.

**RN-18.** El software se deberá ajustar a la ley de privacidad de los datos vigente en todo momento.

#### Seguridad
**RN-19.** Determinados datos de la base de datos deben estar almacenados de tal forma
que garanticen su privacidad en todo momento. Así como estará prohibido usar
información privada para fines no autorizados.


### 2.3 Requisitos de información
#### RI-1 Clientes dados de alta
Toda la información que necesitaremos del cliente para tratarlo y gestionarlo de forma efectiva.  
Contenido: Nº de cliente, nombre, DNI, Nº de la Seguridad social, domicilio, historial médico(enfermedades diagnosticadas, pruebas realizadas, ingresos, alergias), médico de familia asignado(el que preferiblemente le pasará consulta), e-mail, teléfono, cuenta bancaria y deuda con la compañía(si no ha hecho algún pago).  
Requisitos asociados:RF-3, RF-2, RF-5.
#### RI-2 Empleados administrativos
Información de los profesionales administrativos que trabajan para la compañía/hospital.  
Contenido: Nombre de la profesión, sueldo, cuenta del banco, teléfono, e-mail, DNI y Nº de trabajador.
#### RI-3 Médicos
Información de cada uno de los médicos que trabajan para la compañía/hospital.  
Contenido: Especialidad, sueldo, cuenta del banco, teléfono, e-mail, DNI, Nº de médico,
operaciones y consultas pendientes.
#### RI-4 Enfermeros
Información de cada uno de los enfermeros que trabajan para la compañía/hospital.  
Contenido: Sueldo, cuenta del banco, teléfono y e-mail, DNI, seccion en la que trabaja, Nº de enfermero.
#### RI-5 Auxiliar
Información de cada uno de los auxiliares que trabajan para la compañía/hospital.  
Contenido: Sueldo, cuenta del banco, teléfono y e-mail, DNI, Nº de auxiliar.
#### RI-6 Celador
Información de cada uno de los celadores que trabajan para la compañía/hospital.  
Contenido: Sueldo, cuenta del banco, teléfono y e-mail, DNI, Nº de celador.
#### RI-7 Fisioterapeuta
Información de cada uno de los fisioterapeutas que trabajan para la compañía/hospital.  
Contenido: Sueldo, cuenta del banco, teléfono y e-mail, DNI, Nº de fisioterapeuta.
#### RI-8 Personal de mantenimiento
Información de cada uno de los empleados de mantenimiento que trabajan para la compañía/hospital.  
Contenido: Nombre de profesión, sueldo, cuenta del banco, teléfono y e-mail, DNI, Nº de empleado.
#### RI-9 Hospitales
Información necesaria para la gestión del hospital.  
Contenido: Nombre de hospital, gerente del hospital, cantidad de camas y habitaciones total y disponibles,Nº de pacientes internados, horario de urgencias(si es que tiene), Nº de consultas y quirófanos.
#### RI-10 Operaciones y consultas
Información relativa a las operaciones, consultas y sus implicados.  
Contenido: Fecha determinada, tipo de operación o consulta, Nº de médico que la realiza, DNI de paciente y Nº de quirófano o consulta.  
Requisitos asociados: RF-1.
#### RI-11 Consultas
Información relativa a las habitaciones en las que se hacen las consultas.  
Contenido: Hospital, planta, Nº de consulta, horario, Nº de médico(s) asociado a esta consulta(si es que tiene alguno).  
Requisitos asociados: RF-1.
#### RI-12 Quirófanos
Información relativa a los quirófanos.  
Contenido: Hospital, planta, tipo de quirófano, Nº de quirófano.  
Requisitos asociados: RF-1.
#### RI-13 Ambulancias
Información relativa a las ambulancias y vehículos de emergencia.  
Contenido: Hospital al que pertenece, tipo de ambulancia, Nº de ambulancia, Nº de auxiliar(s) asociado a esta ambulancia(si es que tiene alguno).
#### RI-14 Medicamentos
Información sobre los medicamentos con los que se trabaja.  
Contenido:Tipo, descripción, cantidad de la que se dispone, pedidos realizados.  
Requisitos asociados: RF-2.
#### RI-15 Proveedores
Información sobre los distintos proveedores a los que se pueden pedir medicamentos o utensilios varios necesarios para un hospital.  
Contenido: Nombre del proveedor, NIF, productos que proveen, Nº de cuenta y pedidos.
#### RI-16 Pedidos
Pedidos que se han realizado y que todavía no han llegado.  
Contenido: Nº de pedido, fecha de entrega prevista.
#### RI-17 Incidencias
Información sobre los partes de incidencias que pueden ocurrir en el hospital.  
Contenido: Hospital, empleado que la rellena, asunto, descripción de la incidencia.  
Requisitos asociados: RF-4.



## 3. Glosario de términos
- ***Actores***
  - **Pacientes:** Persona enferma que es o va a ser atendido por un profesional.
de la salud
  - **Médico:** Persona legalmente autorizada para profesar y ejercer la medicina.
  - **Especialista:** Médico u otro profesional de la salud que está capacitado y autorizado
  en un área especial de la medicina.
  - **Enfermero:** Persona que tiene por oficio asistir o atender a enfermos, heridos o lesionados
  bajo las prescripciones de un médico, o ayudar al médico o cirujano.
  - **Auxiliar de enfermería:** Profesional sanitario encargado de proporcionar cuidados auxiliares
  al paciente y actuar sobre las condiciones sanitarias de su entorno bajo la supervisión del
  diplomado en enfermería o el facultativo médico.
  - **Celador sanitario:** Persona encargada del translado de pacientes y la vigiliancia
  de estos y, el transporte de materiales e información.
  - **Fisioterapeuta:** Persona especializada en aplicar la fisioterapia.
  - **Personal de mantenimiento:** Personal encargado del montaje, ajuste, revisión,
  acondicionamiento y reparación de las instalaciones y maquinaria de un local.
- ***Valoración:***
  - **Ingreso:** Es la aceptación formal de un paciente por el hospital  para su
  atención médica, observación, tratamiento y recuperación. Todo ingreso al hospital
  involucra la ocupación de una cama hospitalaria y la mantención de una historia
  clínica para el registro de todas las atenciones otorgadas.

    No deben considerarse ingresos los bebes nacidos vivos sanos o los nacidos muertos
    en el establecimiento, las personas que fallecen mientras son trasladadas al hospital
    y las personas que fallecen en la sala de espera de la Unidad de Emergencia del  establecimiento.
  - **Alta:** Certificado médico que autoriza al paciente para que vuelva a sus actividades normales.
  - **Exitus:** Término proveniente del latín que es usado en medicina para indicar
  que la enfermedad ha progresado hacia o desembocado en la muerte.
  - **Cita:** Asignación de día, hora y lugar para ver a cierto médico o especialista.
- ***Vías de administración:***
  - **Oral:** A través de la boca.
  - **Intravenosa:** A través de una vena.
  - **Subcutánea:** A través de los tejidos subcutáneos (hipodermis).
  - **Intramuscular:** Se pone en el interior de un músculo.
  - **Intradérmica:** A través de la dermis.
  - **Ótica:** A través del oido.
  - **Oftálmica:** A través de los ojos.
  - **Rectal:** A través del recto.
  - **Dérmica:** A través de la piel.
  - **Vaginal:** A través de la vagina.
  - **Inhalatoria:** a través de la nariz o la boca, y hacia los pulmones durante la
  inhalación respiratoria.
  - **Nasal:** A través de la nariz.
- ***Historial médico***
  - **Antecedentes:** Recopilación de la información sobre la salud de una persona
  lo cual permite manejar y darle seguimiento a su propia información de salud. Los antecedentes
  médicos personales pueden incluir información sobre alergias, enfermedades, cirugías y
  vacunas, así como los resultados de exámenes físicos, pruebas y exámenes de detección. Asimismo,
  contiene información sobre los medicamentos que se toman y sobre los hábitos de salud,
  como régimen de alimentación y ejercicio.S
  - **Enfermedad:** Alteración leve o grave del funcionamiento normal de un organismo o
  de alguna de sus partes debida a una causa interna o externa.
  - **Intervención quirúrgica:** u operación, es una acción mecánica sobre una estructura
  anatómica del cuerpo.
- ***Gráfica de constantes***
  - **Presión arterial:** Presión que ejerce la sangre en las paredes de las arterias.
  - **Frecuencia cardiaca:** Número de contracciones del corazón por unidad de tiempo.
  - **Saturación de oxígeno:** Medida de la cantidad de oxígeno disponible en la sangre.
  - **Glucemia:** Presencia de azúcar en la sangre, especialmente cuando excede de lo normal.
  - **Temperatura corporal:** Medida relativa de calor asociada al metabolismo del cuerpo humano.
- ***Gestión de pruebas***
  - **Prueba de imagen**
    - **Resonancia**: Técnica no invasiva que utiliza el fenómeno de la resonancia magnética nuclear para obtener información sobre la estructura y composición del cuerpo.
    - **Radiografía**: Técnica exploratoria que consiste en someter un cuerpo o un objeto a la acción de los rayos X para obtener una imagen sobre una placa fotográfica.
    - **Ecografía**: Técnica que utiliza ultrasonidos para generar imágenes bidimensionales o tridimensionales.
    - **Gastroscopia**: Observación del esófago, estómago y duodeno mediante una cámara controlable insertada en un aparato llamado gastroscopio.
    - **Colonoscopia**: Observación del intestino grueso y última parte del intestino delgado mediante el uso de colonoscopio, un tubo flexible que contiene una cámara y que además permite recogida biopsias.
  - **Espirometría:** es una prueba no invasiva que permite conocer la función pulmonar de una persona. Consiste en respirar por la boca a través de un pequeño tubo, y forzar la respiración para medir el flujo aéreo.
  - **Extracciones y vacunas:** Extracción de sangre o inyección de una vacuna mediante una jeringuilla. La vacuna es una sustancia compuesta por una suspensión de microorganismos atenuados o muertos que se introduce en el organismo para prevenir y tratar determinadas enfermedades infecciosas; estimula la formación de anticuerpos con lo que se consigue una inmunización contra estas enfermedades.
  - **Electrocardiograma:** Gráfico en el que se registran los movimientos del corazón y es obtenido por un electrocardiógrafo.
  - **Recogida de muestras (orina, frotis...):**  Recogida de muestras de secrecciones corporales como orina, heces o saliva.






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
