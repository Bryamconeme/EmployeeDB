<<<<<<< HEAD
REQUERIMIENTOS.md
=======
# REQUERIMIENTOS DEL SISTEMA DE INTERCAMBIO Y VENTA DE CARTAS COLECCIONABLES

**Versión:** 1.0  
**Fecha:** 14 de octubre de 2025  
**Autores:** Equipo de desarrollo – Proyecto Cartas Coleccionables  


---

<<<<<<< HEAD
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
=======
## 1. Descripción del Cliente y Problema Principal

El cliente corresponde a un grupo de emprendedores dedicados al **coleccionismo e intercambio de cartas** de distintos juegos reconocidos a nivel mundial, tales como **Pokémon**, **Mitos y Leyendas** y **Yu-Gi-Oh!**.  
Actualmente, este grupo administra comunidades en redes sociales y foros donde los usuarios publican cartas para vender, intercambiar o subastar.
>>>>>>> 03ec2c9 (Reemplazado archivo REQUERIMIENTOS.md)

Durante las reuniones iniciales, el cliente manifestó que el principal problema radica en la falta de una **plataforma unificada y segura** que centralice todas las actividades relacionadas con la compra, venta y validación de cartas.  
En los espacios actuales, las transacciones se realizan de manera informal, lo que genera múltiples dificultades:

<<<<<<< HEAD
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

=======
- Riesgo de fraudes o falsificaciones de cartas.  
- Dificultad para verificar la autenticidad y el estado de los artículos.  
- Falta de historial o trazabilidad de los intercambios.  
- Desconfianza entre compradores y vendedores.
>>>>>>> 03ec2c9 (Reemplazado archivo REQUERIMIENTOS.md)

El objetivo principal del cliente es consolidar una **comunidad digital confiable** donde los usuarios puedan realizar transacciones de manera **transparente, eficiente y segura**, fortaleciendo el mercado del coleccionismo y mejorando la experiencia de los participantes.

---

## 2. Lista de Usuarios del Sistema

### Administrador
- Supervisa y gestiona la plataforma en su totalidad.  
- Valida la autenticidad de las cartas publicadas.  
- Monitorea transacciones, subastas y trueques para garantizar seguridad.  
- Gestiona cuentas de usuarios y resuelve conflictos o reportes.

### Vendedor
- Publica cartas disponibles para la venta o intercambio.  
- Administra su inventario y actualiza información de las cartas.  
- Participa en subastas y trueques con otros usuarios.  
- Recibe retroalimentación y calificaciones de los clientes.

### Cliente
- Accede a la plataforma para adquirir cartas (compra o intercambio).  
- Participa en subastas o trueques supervisados.  
- Valora y califica las transacciones realizadas con los vendedores.  
- Mantiene un historial de compras y colecciones adquiridas.

### Usuario General
- Registra un perfil en la plataforma para interactuar con la comunidad.  
- Participa en intercambios, subastas o foros de discusión.  
- Puede agregar cartas a su colección personal sin realizar compras.

---

## 3. Funciones Necesarias

- Registro de nuevos usuarios con validación de rol (cliente o vendedor).  
- Autenticación segura mediante hash de contraseñas.  
- Gestión básica de usuarios (crear, modificar, eliminar, suspender).  
- Gestión de cartas (crear, editar, eliminar, verificar).  
- Publicación y visualización de cartas disponibles.  
- Comunicación directa entre cliente y vendedor.

---

## 4. Datos a Guardar

| Entidad | Campos principales |
|----------|--------------------|
| **Usuarios** | ID, nombre, correo, rol, permisos, contraseña (hash) |
| **Clientes** | ID, nombre, RUT, contacto, historial de compras, método de pago |
| **Vendedores** | ID, nombre, RUT, contacto, historial de ventas, estado de suscripción |
| **Cartas** | ID, juego (Pokémon, Yu-Gi-Oh, etc.), valor estimado, calidad (grading), autenticación/estado de verificación |

---

## 5. Reglas de Negocio

1. Los vendedores solo serán visibles públicamente si tienen una suscripción activa.  
2. Los clientes pueden publicar o comprar un máximo de **2 cartas por semana**.  
3. Toda carta debe ser **verificada por un administrador** antes de publicarse.  
4. Si un cliente reserva una carta y no paga en un plazo de **1 día**, la reserva se anula automáticamente.  
5. Los trueques deben contar con acuerdo mutuo entre ambas partes.  
6. Las subastas deben ser **supervisadas por un administrador** antes de su ejecución.

---

## 6. Prioridades

| Nivel | Funcionalidades |
|-------|------------------|
| **Alta** | Gestión de usuarios, validación de cartas, procesamiento de pagos |
| **Media** | Reservas |
| **Baja** | Trueques y subastas |

---

## 7. Flujos Principales

1. Creación de usuario  
2. Asignación de rol (cliente o vendedor)  
3. Publicación o compra de carta  
4. Contacto entre cliente y vendedor  
5. Procesamiento de pago  
6. Carta adquirida/vendida  

---

## 8. Requisitos No Funcionales

- Seguridad en la gestión de usuarios y contraseñas (hash, login seguro).  
- Interfaz simple, responsiva y accesible desde dispositivos móviles.  
- Escalabilidad para múltiples subastas simultáneas.  
- Disponibilidad 24/7 con tiempo de inactividad < 1%.  
- Soporte para al menos 100 usuarios concurrentes.  
- Historial de pujas y transacciones consultable.  
- Cumplimiento con la **Ley 19.628** de protección de datos personales (Chile).

---

## 9. Plazo

**Primera versión funcional (MVP):** 6 de noviembre de 2025  
Incluye base de datos lista y apartado visual básico.

---

## 10. Presupuesto

- **Clientes:** acceso gratuito.  
- **Vendedores:** suscripción semanal de **$3.000 CLP (≈ USD 3,30)**.  
Incluye alojamiento, validación de cartas, soporte técnico y visibilidad pública.

---

## 11. Propuesta Formal y Cronograma de Trabajo

### Propuesta Formal

Se propone el desarrollo de una **plataforma web** (con potencial para futura aplicación móvil) enfocada en la **seguridad transaccional** y la **validación de autenticidad de cartas**.  
El enfoque es crear un **mercado digital vertical y especializado** en coleccionismo.

### Cronograma de Alto Nivel

| Fase | Fecha Límite | Objetivos Principales |
|------|---------------|-----------------------|
| **Fase I: MVP** | 6 de noviembre | Base de datos, Login/Registro, Gestión de usuarios, Publicación y Validación de cartas, Procesamiento de pagos |
| **Fase II: Expansión** | Posterior a 6 de noviembre | Trueques y subastas |
| **Fase III: Estabilización** | Continua | Pruebas, mejoras UX/UI y rendimiento |

---

## 12. Criterios de Aceptación y Valor de Negocio

### Criterios de Aceptación
- El flujo completo de registro y validación de rol se ejecuta correctamente en el 100% de las pruebas.  
- La interfaz es completamente responsiva y funcional en **Chrome**, **Firefox** y **Safari**.  
- El sistema soporta un mínimo de **100 usuarios concurrentes** sin degradación del rendimiento.

### Valor de Negocio
- **Valor para la comunidad:** plataforma digital confiable para coleccionistas, eliminando el riesgo de fraude.  
- **Ganancia financiera:** ingreso recurrente mediante suscripciones semanales de vendedores, garantizando sostenibilidad del proyecto.

<<<<<<< HEAD



=======
---

## 13. Soporte y Mantenimiento

- **Monitoreo:** supervisión constante del sistema para detectar fallos o problemas de seguridad.  
- **Mantenimiento correctivo:** resolución de bugs y problemas reportados por la comunidad.  
- **Mantenimiento evolutivo:** incorporación de nuevas funcionalidades y mejoras continuas.  
- **Actualizaciones de seguridad:** aplicación periódica de parches y auditorías para proteger la integridad de los datos.

---

## 14. Próximos Pasos

- **Estabilización y mantenimiento correctivo** en las primeras semanas tras el lanzamiento.  
- **Mejoras visuales y de experiencia de usuario (UI/UX)** según retroalimentación.  
- **Evaluación de futuras funcionalidades:**
  - Aplicación móvil nativa (iOS/Android).  
  - Motor de búsqueda avanzado con filtros por edición, rareza y valoración profesional de cartas.

---

© 2025 – Proyecto Cartas Coleccionables. Todos los derechos reservados.
>>>>>>> 03ec2c9 (Reemplazado archivo REQUERIMIENTOS.md)
