# REQUERIMIENTOS DEL SISTEMA DE INTERCAMBIO Y VENTA DE CARTAS COLECCIONABLES

**Versión:** 1.1  
**Fecha:** 14 de octubre de 2025  
**Autores:** Equipo de desarrollo – Proyecto Cartas Coleccionables  

---

## 1. Descripción del Cliente y Problema Principal

El cliente corresponde a un grupo de emprendedores dedicados al coleccionismo e intercambio de cartas de distintos juegos reconocidos a nivel mundial, tales como Pokémon, Mitos y Leyendas y Yu-Gi-Oh!. Actualmente, este grupo administra diversas comunidades en redes sociales y foros, donde los usuarios publican sus cartas para vender, intercambiar o subastar.

Durante las reuniones iniciales, el cliente manifestó que el principal problema radica en la falta de una plataforma unificada y segura que centralice todas las actividades relacionadas con la compra, venta y validación de cartas. En los espacios actuales, las transacciones suelen realizarse de manera informal, lo que genera múltiples dificultades, entre ellas:

- Riesgo de fraudes o falsificaciones de cartas.  
- Dificultad para verificar la autenticidad y el estado de los artículos.  
- Falta de un historial o trazabilidad de los intercambios.  
- Desconfianza entre compradores y vendedores.

Ante esta situación, el cliente solicitó el desarrollo de un sistema web especializado que permita a los coleccionistas:

- Crear un perfil personal con información básica y su inventario de cartas.  
- Publicar cartas disponibles para la venta o intercambio.  
- Participar en subastas y trueques de manera controlada.  
- Acceder a un sistema de validación y reputación que garantice la seguridad de las operaciones.

El objetivo principal del cliente es consolidar una comunidad digital confiable donde los usuarios puedan realizar transacciones de manera transparente, eficiente y segura, fortaleciendo el mercado del coleccionismo y mejorando la experiencia general de los participantes.

---

## 2. Usuarios del Sistema

| Tipo de usuario | Descripción | Permisos principales |
|------------------|-------------|----------------------|
| **Administrador** | Supervisa la plataforma y valida autenticidad de cartas. | Crear, editar y eliminar usuarios y publicaciones; aprobar ventas. |
| **Vendedor** | Publica cartas y gestiona sus ventas o intercambios. | Registrar productos, modificar precios, consultar ventas. |
| **Cliente** | Navega, compra e intercambia cartas. | Buscar cartas, realizar compras o intercambios, dejar reseñas. |

---

## 3. Alcance del Proyecto

### Incluye
- Registro y autenticación de usuarios.  
- Publicación y gestión de cartas.  
- Compra, venta e intercambio de cartas.  
- Validación de autenticidad por el administrador.  
- Notificaciones de estado de publicación y transacción.  

### No incluye
- Envío físico de cartas (solo gestión en línea).  
- Integración con pasarelas de pago reales (simulación).  
- Aplicación móvil nativa (solo versión web responsiva).

---

## 4. Requerimientos Funcionales (RF)

| Código | Requerimiento | Prioridad |
|--------|----------------|------------|
| **RF-01** | El sistema debe permitir el registro de nuevos usuarios con validación de rol (cliente, vendedor o administrador). | Alta |
| **RF-02** | El vendedor podrá publicar cartas con nombre, tipo de juego, condición, imagen y precio. | Alta |
| **RF-03** | El administrador debe revisar y aprobar las publicaciones antes de que sean visibles. | Alta |
| **RF-04** | Los clientes podrán realizar compras y reservas de cartas disponibles. | Alta |
| **RF-05** | El sistema debe enviar notificaciones automáticas (publicación aprobada, venta confirmada, pago recibido, etc.). | Media |
| **RF-06** | Los usuarios podrán comunicarse mediante mensajes internos. | Media |
| **RF-07** | El sistema debe registrar un historial de transacciones por usuario. | Alta |
| **RF-08** | El administrador podrá suspender cuentas o publicaciones que incumplan normas. | Alta |
| **RF-09** | El vendedor podrá actualizar o eliminar sus publicaciones. | Media |
| **RF-10** | El cliente podrá dejar reseñas y calificaciones después de una compra. | Baja |

---

## 5. Requerimientos No Funcionales (RNF)

| Código | Categoría | Requerimiento | Prioridad |
|---------|------------|----------------|------------|
| **RNF-01** | Seguridad | Las contraseñas deben almacenarse cifradas y la comunicación usar HTTPS. | Alta |
| **RNF-02** | Usabilidad | La interfaz debe ser responsiva y accesible desde PC, tablet o smartphone. | Alta |
| **RNF-03** | Rendimiento | El tiempo de respuesta máximo debe ser inferior a 2 segundos por solicitud. | Media |
| **RNF-04** | Disponibilidad | El sistema debe mantener un 99 % de disponibilidad mensual. | Alta |
| **RNF-05** | Escalabilidad | La aplicación debe permitir la incorporación futura de más juegos y categorías. | Media |
| **RNF-06** | Mantenibilidad | El código debe estar documentado y seguir buenas prácticas de desarrollo. | Media |

---

## 6. Datos a Guardar

- **Usuarios:** ID, nombre, correo, contraseña cifrada, rol, estado de cuenta.  
- **Cartas:** ID, nombre, juego, estado, rareza, precio, vendedor, imágenes.  
- **Transacciones:** ID, comprador, vendedor, carta, monto, fecha, estado.  
- **Mensajes:** ID, emisor, receptor, contenido, fecha.  
- **Calificaciones:** ID, comprador, vendedor, puntuación, comentario.  

### Modelo conceptual (simplificado)
Usuario (1) --- (N) Carta
Usuario (1) --- (N) Transacción --- (1) Carta
Usuario (1) --- (N) Mensaje --- (1) Usuario


---

## 7. Reglas de Negocio

1. El vendedor sólo podrá estar visible al público si paga una suscripción semanal.  
2. Los clientes solo pueden publicar y comprar 2 cartas a la semana.  
3. Las cartas deben ser verificadas por un administrador antes de publicarse.  
4. Si un cliente reserva y no paga en 1 día, se anulará la reserva.  
5. Los trueques deben ser aceptados por ambas partes.  
6. Las subastas deben ser supervisadas por un administrador.  
7. Toda publicación rechazada debe indicar el motivo.  
8. El sistema registrará cada cambio de estado (auditoría básica).  

---

## 8. Flujos Principales

### 8.1. Flujo de Publicación de Carta
1. El vendedor inicia sesión.  
2. Publica una carta con sus detalles.  
3. El administrador revisa la publicación.  
4. Si la aprueba → la carta se muestra en el catálogo.  
5. Si la rechaza → se notifica al vendedor con el motivo.  

### 8.2. Flujo de Compra
1. El cliente selecciona una carta disponible.  
2. Realiza la compra o reserva.  
3. Se notifica al vendedor y al administrador.  
4. Se actualiza el inventario y el historial del usuario.

---

## 9. Requisitos Técnicos

- **Lenguaje backend:** C# (.NET) o Node.js.  
- **Base de datos:** Microsoft SQL Server.  
- **Frontend:** React.js o Vue.js (interfaz responsiva).  
- **Servidor:** Azure / AWS / Localhost en desarrollo.  
- **Control de versiones:** Git y GitHub.  
- **Arquitectura:** Cliente–Servidor con API REST.  

---

## 10. Cronograma de Desarrollo

| Fase | Actividades | Duración estimada |
|------|--------------|------------------|
| **Fase 1 – MVP** | Registro, login, publicación de cartas, validación por admin. | 4 semanas |
| **Fase 2 – Intercambio y reseñas** | Módulo de intercambio, mensajería, calificaciones. | 3 semanas |
| **Fase 3 – Optimización** | Seguridad, auditorías, pruebas de carga, documentación. | 2 semanas |
| **Fase 4 – Mantenimiento** | Corrección de errores, mejoras, soporte. | Continua |

---

## 11. Riesgos y Mitigaciones

| Riesgo | Impacto | Probabilidad | Mitigación |
|--------|----------|---------------|-------------|
| Falsificación de cartas | Alto | Media | Validación obligatoria del administrador con evidencias visuales. |
| Fallo del servidor | Alto | Baja | Respaldos automáticos diarios. |
| Error de pago o transacción duplicada | Medio | Media | Simulación de pagos con verificación previa. |
| Desinterés de usuarios iniciales | Medio | Alta | Campaña de prueba gratuita con recompensas por feedback. |
| Problemas de rendimiento | Medio | Media | Pruebas de carga y optimización de consultas SQL. |

---

## 12. Criterios de Aceptación

- El sistema permite registrar usuarios y roles correctamente.  
- Las cartas solo se publican tras aprobación del administrador.  
- Los usuarios pueden realizar compras e intercambios exitosos.  
- El tiempo de respuesta no supera los 2 segundos.  
- El sistema es accesible desde dispositivos móviles.  

---

## 13. Valor de Negocio

- Aumentar la **confianza y seguridad** en el intercambio de cartas.  
- Disminuir fraudes y pérdidas económicas.  
- Mejorar la visibilidad de coleccionistas y vendedores.  
- Promover una comunidad sólida de intercambio digital.  

---

## 14. Soporte y Mantenimiento

- **Monitoreo:** Detección temprana de errores o problemas de rendimiento.  
- **Mantenimiento correctivo:** Resolución de bugs reportados.  
- **Mantenimiento evolutivo:** Incorporación de nuevas funcionalidades.  
- **Actualizaciones de seguridad:** Aplicación periódica de parches.  

---

## 15. Próximos Pasos

- Estabilización y pruebas post lanzamiento.  
- Mejoras visuales y experiencia de usuario.  
- Desarrollo de aplicación móvil nativa (iOS/Android).  
- Integración de un motor de búsqueda avanzado con filtros por edición, rareza y valoración profesional.  

---

## 16. Trazabilidad de Requerimientos

| Problema detectado | Requerimiento que lo soluciona |
|---------------------|--------------------------------|
| Falta de control y validación de cartas | RF-03, RNF-01 |
| Riesgo de fraude | RF-07, RNF-01 |
| Dificultad de comunicación | RF-06 |
| Baja visibilidad de vendedores | RF-02, RF-09 |
| Lentitud y poca accesibilidad | RNF-02, RNF-03 |

---

**Documento completo y listo para entrega institucional o repositorio GitHub.**
