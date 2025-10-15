REQUERIMIENTOS.md

1. Descripción del cliente y problema principal

El cliente corresponde a un grupo de emprendedores dedicados al coleccionismo e intercambio de cartas de distintos juegos reconocidos a nivel mundial, tales como Pokémon, Mitos y Leyendas y Yu-Gi-Oh!. Actualmente, este grupo administra diversas comunidades en redes sociales y foros, donde los usuarios publican sus cartas para vender, intercambiar o subastar.

Durante las reuniones iniciales, el cliente manifestó que el principal problema radica en la falta de una plataforma unificada y segura que centralice todas las actividades relacionadas con la compra, venta y validación de cartas.
En los espacios actuales, las transacciones suelen realizarse de manera informal, lo que genera múltiples dificultades, entre ellas:
-Riesgo de fraudes o falsificaciones de cartas.
-Dificultad para verificar la autenticidad y el estado de los artículos.
-Falta de un historial o trazabilidad de los intercambios.
-Desconfinacia entre Compradores y vendedores.

Ante esta situación, el cliente solicitó el desarrollo de un sistema web especializado que permita a los coleccionistas:

-Crear un perfil personal con información básica y su inventario de cartas.
-Publicar cartas disponibles para la venta o intercambio.
-Participar en subastas y trueques de manera controlada.
-Acceder a un sistema de validación y reputación que garantice la seguridad de las operaciones.

Acceder a un sistema de validación y reputación que garantice la seguridad de las operaciones.

El objetivo principal del cliente es consolidar una comunidad digital confiable donde los usuarios puedan realizar transacciones de manera transparente, eficiente y segura, fortaleciendo el mercado del coleccionismo y mejorando la experiencia general de los participantes.

2. Lista de usuarios del sistema

El sistema contará con cuatro tipos principales de usuarios, cada uno con distintos permisos y responsabilidades:

Administrador

-Supervisa y gestiona la plataforma en su totalidad.
-Valida la autenticidad de las cartas publicadas.
-Monitorea transacciones, subastas y trueques para garantizar seguridad.
-Gestiona cuentas de usuarios y resuelve conflictos o reportes.

Vendedor

-Publica cartas disponibles para la venta o intercambio.
-Administra su inventario y actualiza información de las cartas.
-Participa en subastas y trueques con otros usuarios.
-Recibe retroalimentación y calificaciones de los clientes.

Usuario

-Registra un perfil en la plataforma para interactuar con la comunidad.
-Participa en intercambios, subastas o foros de discusión sobre cartas.
-Puede agregar cartas a su colección personal, sin realizar compras.

Cliente

-Accede a la plataforma con el objetivo de adquirir cartas (compra o intercambio).
-Puede participar en subastas o trueques supervisados.
-Valora y califica las transacciones realizadas con los vendedores.
-Mantiene un historial de compras y colecciones adquiridas.


3.Funciones necesarias

Registrar usuarios nuevos en el sistema.
Validación del rol del usuario, ya sea cliente o vendedor.
Gestion básica de usuarios.
Gestión de cartas publicadas en el sistema.
Contacto entre cliente/vendedor.

4.Datos a guardar


Usuarios: Nombre, rol, permisos, hash de contraseña
Clientes: ID, nombre, RUT/identificación, contacto, historial de compras, método de pago
Tipo de Carta: Juego (e.g., Pokémon, Yu-Gi-Oh), valor estimado, calidad (grading), autentificación/estado de verificación
Vendedor: ID, nombre, RUT/identificación, contacto, historial de ventas, estado de suscripción

5.Reglas de negocio

El vendedor sólo podrá estar a la visibilidad de todos si paga una suscripción semanal.
Los clientes solo pueden publicar y comprar 2 cartas a la semana.
Las cartas tienen que ser verificadas para poder publicarse.
Si el cliente reserva y no paga en 1 día se anulará la reserva.
Los trueques tienen que tener un acuerdo mútuo para realizarse.
Las subastas tienen que estar supervisadas por algún administrador antes de realizarse.



6.Prioridades

Alta: Gestión usuarios, validar cartas, procesar pagos
Media: Reservas
Baja:  Trueques,subastas

7.Flujos principales

Creación usuario -> obtener rol -> publicar/comprar carta -> contactar al vendedor -> procesar pago -> carta adquirida/vendida

8. Requisitos no funcionales

-Seguridad en la gestión de usuarios y contraseñas (hash, login seguro).
-Interfaz simple y responsiva.
-Escalabilidad para múltiples subastas simultáneas.
-Disponibilidad 24/7.
-Historial de pujas y subastas consultable.

9.Plazo 

Primera versión funcional el seis de noviembre con base de datos lista y apartado visual.

10.Presupuesto

Creación base de datos, sitio web, creacion de usuarios y perfiles, publicación de cartas
el presupuesto si eres cliente comprador es totalmente gratis, para los vendedores de cartas es una suma de $3.000 pesos chilenos $3,30 US semanales.

11. Propuesta Formal y Cronograma de Trabajo
Propuesta Formal: Proponemos el desarrollo de una plataforma web (con potencial para una futura aplicación móvil) para la comunidad de coleccionistas. La clave de esta propuesta radica en la seguridad transaccional y la validación de la autenticidad de las cartas, diferenciándonos de plataformas de venta general. El enfoque es crear un mercado vertical y especializado.

Cronograma de Alto Nivel:

Fase I: MVP Hasta 6 de Noviembre  Módulos de Prioridad Alta y Media: Base de datos, seguridad (Login/Registro), Gestión de Usuarios, Publicación y Validación de Cartas, Procesamiento de Pagos.
 Fase II: Expansión Post 6 de Noviembre Módulos de Prioridad Baja: Implementación y optimización de Trueques y Subastas. 
Fase III: Estabilización Continua Pruebas de carga, mejoras de experiencia de usuario y optimización de rendimiento. 

12. Criterios de Aceptación y Ganancia
Criterios de Aceptación (Medibles y Verificables):

El flujo completo de registro de usuario y validación de rol debe ejecutarse correctamente en el 100% de las pruebas.

La interfaz debe ser completamente responsiva y funcional en Chrome, Firefox y Safari.

El sistema debe soportar un mínimo de 100 usuarios concurrentes sin degradación de rendimiento.

Ganancia / Valor de Negocio:

Valor para la Comunidad: Establecer la plataforma como el mercado digital de confianza para coleccionistas, eliminando el riesgo de fraude.

Ganancia Financiera: Generación de un ingreso predecible y recurrente a través del modelo de suscripción semanal para los vendedores, asegurando la sostenibilidad del proyecto.

13. Soporte y Mantenimiento
Nuestro compromiso con la plataforma es de desarrollo y monitoreo constante. El soporte y mantenimiento se basará en:

Monitoreo: Implementación de administradores para asegurar la disponibilidad y detectar errores de rendimiento o problemas de seguridad de forma proactiva.

Mantenimiento correctivo: Equipo dedicado a la resolución de bugs y problemas reportados por la comunidad.

Mantenimiento evolutivo: La plataforma se mantendrá en constante evolución, incorporando nuevas funcionalidades y adaptándose a las necesidades cambiantes del mercado coleccionista.

Actualizaciones de Seguridad: Aplicación periódica de parches y auditorías de seguridad para proteger la integridad de los datos de los usuarios y las transacciones financieras.

14. Próximos Pasos
Una vez lanzada la versión inicial, el enfoque se desplazará hacia la optimización y expansión:

Estabilización y Mantenimiento Correctivo: El foco inicial estará en resolver cualquier bug o problema de rendimiento detectado en las primeras semanas de uso real.

Mejoras visuales y experiencia de usuario: Se realizarán mejoras más detalladas en la interfaz (UI) para crear una experiencia más fluida e intuitiva, basándose en la retroalimentación de los usuarios.

Evaluación de futuras funcionalidades: Se comenzará a planificar el desarrollo de funcionalidades avanzadas como:

Una aplicación móvil nativa (iOS/Android) para la gestión y compra/venta en movimiento.

Integración de un motor de búsqueda avanzado con filtros por edición, rareza y valoración profesional de cartas.





