Requerimientos

Descripción del cliente y problema principal:
La empresa ficticia Technoblade enfrenta actualmente una serie de deficiencias relacionadas con la gestión de su personal, principalmente debido a la ausencia de un sistema centralizado que permita llevar un control adecuado sobre sus empleados y los recursos asignados a estos. Esta falta de organización ha generado diversas complicaciones operativas, como la imposibilidad de contar con un inventario actualizado de trabajadores, lo que dificulta la identificación clara del personal activo, sus roles, los dispositivos o equipos que se les han asignado, así como los horarios en los que desempeñan sus funciones.

Uno de los principales problemas radica en la baja seguridad en el control de accesos, ya que, al no disponer de un registro confiable de entradas y salidas del personal, la empresa no puede garantizar que únicamente los empleados autorizados tengan acceso a áreas sensibles o información empresarial confidencial. Esta situación representa un riesgo importante tanto para la seguridad de los datos internos como para la operatividad general de la organización.

Además, la falta de un sistema que permita gestionar los permisos de edición y eliminación de información genera vulnerabilidades en la integridad de los datos. Actualmente no existe una forma de verificar quién modifica o elimina información dentro de los registros, lo que podría dar lugar a errores o manipulaciones no autorizadas.

Por otro lado, Technoblade carece de una herramienta eficaz para el registro de horas laborales, lo que impide una correcta gestión del tiempo trabajado por cada empleado y, en consecuencia, dificulta la elaboración precisa de las nóminas y el cálculo de salarios. Esta ausencia de control impacta directamente en la eficiencia administrativa y en la transparencia hacia los trabajadores.

En vista de esta problemática, se propone el desarrollo de un sistema de gestión basado en MongoDB que permita almacenar y organizar de manera eficiente la información de los empleados, controlar el acceso a los recursos y datos según el rol de cada usuario, registrar las jornadas laborales y, en general, optimizar los procesos relacionados con la administración del capital humano de la empresa. Esta solución no solo mejorará la seguridad y la integridad de la información, sino que también facilitará la toma de decisiones operativas a partir de datos fiables y estructurados



Lista de usuarios del sistema:
-Jefe de empresa
-Jefe Programadores
-Programadores
-jefe de diseñadores
-Diseñadores
-Guardias
-Gerencia
-Desarrolladores
-Juniors
-conserjes


Tipos de usuarios y perfiles
(roles) con permisos por rol (mínimo: Administrador, Usuario/Cliente,Vendedor).
-Jefe de empresa (administrador general)
-Jefe Programadores (Admin tecnico)
-Programadores (Usuario tecnico)
-Diseñadores (empleado estandar)
-Guardias (empleado estandar)
-Gerencia (empleado estandar)
-Desarrolladores (Admin tecnico)
-Juniors (Soporte basico)
-conserjes (empleado estandar)



Funciones indispensables por perfil (lista priorizada).

1. Jefe de empresa (Administrador general)
Alta prioridad:
Crear, editar y eliminar usuarios.
Asignar roles y permisos a todos los empleados.
Visualizar todos los datos y reportes de asistencia y productividad.
Aprobar salarios y revisar horas trabajadas.
Media prioridad:
Generar reportes avanzados (para futuras versiones).
Supervisar auditorías de cambios en el sistema.

2. Jefe de programadores / Desarrolladores (Administrador técnico)

Alta prioridad:
Gestionar programadores y desarrolladores asignados.
Asignar y actualizar tareas técnicas.
Ver progreso de proyectos y tareas.
Media prioridad:
Generar reportes técnicos y métricas de productividad.

3. Programadores y Diseñadores (Empleado estándar / Usuario técnico)

Alta prioridad:
Registrar tareas completadas.
Actualizar estado de proyectos.
Media prioridad:
Consultar reportes básicos de sus propias tareas.
Recibir notificaciones de asignaciones (futuro).

4. Guardias y Conserjes (Empleado estándar)
Alta prioridad:
Registrar entrada y salida de empleados.
Validar accesos a las instalaciones.
Media prioridad:
Generar alertas de accesos no autorizados (futuro).

5. Gerencia (Empleado estándar)

Alta prioridad:
Ver reportes de asistencia y horas trabajadas.
Supervisar horarios y productividad del personal.
Media prioridad:
Generar reportes estadísticos avanzados (futuro).

6. Juniors (Soporte básico)
Alta prioridad:
Apoyar en el registro de datos de empleados.
Actualizar información básica bajo supervisión.
Media prioridad:
Consultar tareas asignadas y estado de proyectos




Datos básicos a almacenar (entidades y atributos).

Jefe de empresa: ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Jefe de programadores:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Programadores:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Diseñadores: ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Guardias:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Gerencia:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Desarrolladores:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

Juniors:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado

conserjes:
ID,Nombre,RUT,Cargo,Area,fecha_ingreso,Dirección,Sueldo,Telefono,Correo,Estado


Lista de Requisitos funcionales y No funcionales
.Obtenga datos de manera rapida y eficiente, administre a los empleados, genere un soporte de datos, que verifique que empleado no asistió quien no cumplió con las horas estimadas, que pase lista de los empleados, que tengan permisos diferentes de acuerdo al rol que tienen, actualize los datos automaticamente.




Definición del
MVP
(qué incluye / qué queda para futuras versiones).

El MVP de nuestro sistema consiste en una plataforma básica para registrar y gestionar empleados, controlar sus horarios de entrada y salida, asignar roles y permisos según su perfil, y garantizar la seguridad de los datos. Esta versión permite que la empresa lleve un control efectivo del personal y sus accesos, evitando modificaciones no autorizadas y facilitando la gestión de salarios.
futuras versiones: reportes avanzados, nómina automática, auditoría de cambios, notificaciones, estadísticas de productividad y mejoras en la interfaz.


