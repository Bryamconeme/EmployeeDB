# 🃏 Proyecto: Plataforma de Intercambio y Venta de Cartas Coleccionables

**Versión:** 1.1  
**Autores:** Carlos Sepúlveda, Bryam Beltrán  
**Fecha:** Octubre 2025  

---

## 📖 Descripción General

Este proyecto busca desarrollar una **plataforma web especializada** para la compra, venta, intercambio y subasta de cartas coleccionables de juegos reconocidos como **Pokémon**, **Yu-Gi-Oh!** y **Mitos y Leyendas**.

El objetivo principal es **centralizar las transacciones de los coleccionistas** en un entorno seguro, transparente y confiable, reduciendo el riesgo de fraudes y mejorando la experiencia de los usuarios.

---

## 🧩 Problema a Resolver

Actualmente, las comunidades de coleccionistas operan mediante redes sociales y foros, lo que genera problemas como:

- Falta de trazabilidad de las transacciones.  
- Riesgo de falsificaciones o fraudes.  
- Ausencia de reputación validada entre usuarios.  
- Procesos informales de compra, venta y subasta.  

Este sistema propone una **plataforma unificada** con validación, reputación y auditoría de las operaciones.

---

## 🎯 Objetivos del Proyecto

- Desarrollar un **sistema web seguro y escalable** para coleccionistas.  
- Implementar un **sistema de validación de autenticidad** de cartas.  
- Facilitar **compras, intercambios y subastas** dentro de un entorno controlado.  
- Promover una **comunidad confiable** con roles definidos (Administrador, Vendedor, Cliente, Usuario).

---

## 👥 Roles de Usuario

| Rol | Descripción | Permisos principales |
|-----|--------------|----------------------|
| **Administrador** | Supervisa la plataforma y valida autenticidad | Crear/editar/eliminar usuarios y publicaciones |
| **Vendedor** | Publica y gestiona cartas | Subir cartas, fijar precios, revisar ventas |
| **Cliente** | Compra e intercambia cartas | Comprar, reservar, calificar vendedores |
| **Usuario** | Acceso básico | Registrarse, explorar catálogo |

---

## ⚙️ Funcionalidades Principales

- Registro y autenticación de usuarios con roles.  
- Publicación y gestión de cartas.  
- Compra, venta, reservas e historial de transacciones.  
- Validación de autenticidad de cartas por administrador.  
- Notificaciones automáticas de estado.  
- Sistema de reputación y calificaciones.  

---

## 🧱 Arquitectura Técnica

**Backend:** Node.js + Express + JWT + Redis  
**Base de datos:** MongoDB  
**Frontend:** React.js / Vue.js  
**Infraestructura:**  
- Servidor: Azure / AWS  
- Cache: Redis  
- Control de versiones: Git + GitHub  
**Arquitectura:** Cliente–Servidor (API REST)

---

## 🔐 Requerimientos No Funcionales (RNF)

- Seguridad: Contraseñas cifradas y HTTPS obligatorio.  
- Disponibilidad: ≥ 99 % mensual.  
- Rendimiento: < 2 segundos por solicitud.  
- Escalabilidad: Soporte para nuevos juegos y categorías.  
- Mantenibilidad: Código documentado y modular.  

---

## 🧮 Presupuesto Estimado

**Desarrollo MVP:** $3.400.000 CLP (~US$3.740)  
**Infraestructura mensual:** $185.000 CLP (~US$203)  
**Mantenimiento mensual:** $250.000 CLP (~US$275)  
**Total primer mes:** ~$3.835.000 CLP (~US$4.218)

**Monetización:**  
- Usuarios/Clientes: Gratis  
- Vendedores: $3.000 CLP por semana  

---

## 🗓️ Cronograma General

| Fase | Periodo | Entregables |
|------|----------|-------------|
| **I. MVP (Alta prioridad)** | Hasta 6 de noviembre | Login, gestión de usuarios, publicación y validación de cartas, pagos |
| **II. Expansión** | Post 6 de noviembre | Trueques y subastas |
| **III. Estabilización** | Continuo | Pruebas, optimización, experiencia de usuario |

---

## ✅ Criterios de Aceptación

- Registro y autenticación 100% funcional.  
- Interfaz responsiva en Chrome, Firefox y Safari.  
- Mínimo 100 usuarios concurrentes sin pérdida de rendimiento.  

---

## 🛠️ Instrucciones de Ejecución (modo desarrollo)

```bash
# Clonar el repositorio
git clone https://github.com/usuario/cartas-coleccionables.git

# Entrar a la carpeta del proyecto
cd cartas-coleccionables

# Instalar dependencias backend y frontend
npm install

# Iniciar servidor backend
npm run dev

# Iniciar frontend (en otra terminal)
npm run start
