# Cakeando Sweets Bar

![Privado](https://img.shields.io/badge/Codigo-Privado%20%C2%B7%20Proyecto%20Cliente-red?style=flat)
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg" width="18" align="absmiddle" /> ![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" width="18" align="absmiddle" /> ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg" width="18" align="absmiddle" /> ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat&logo=google&logoColor=white)

> **Sitio web full-stack para una boutique de reposteria artesanal en Panama — con catalogo interactivo, constructor de tortas personalizado y sistema de reservas para eventos.**

> Este es un **portfolio showcase** — el codigo fuente es propietario y no esta incluido.

---

## El Sitio

**[cakeandosweetsbar.sytes.net](https://cakeandosweetsbar.sytes.net/)** — sitio en produccion.

---

## El Problema

Una pasteleria artesanal en Panama necesitaba una presencia digital que transmitiera el nivel premium de sus productos y les permitiera:

- Mostrar su catalogo con disponibilidad actualizada sin depender de un desarrollador
- Recibir pedidos personalizados de tortas sin gestion manual de chats
- Gestionar reservas para su servicio de CakeBar en eventos
- Actualizar inventario y proximos eventos desde un panel simple

---

## La Solucion

Sitio web full-stack con React 19 y un backend Express ligero que maneja emails, persistencia de inventario y un asistente IA conversacional integrado directamente en la experiencia del cliente.

---

## Funcionalidades

| Funcionalidad | Descripcion |
|--------------|-------------|
| Constructor de Tortas | Asistente de 5 pasos (Base, Frosting, Relleno, Toppings, Drizzle) — genera pedido directo por WhatsApp |
| Catalogo de Menu | 5 categorias de productos con disponibilidad en tiempo real |
| Pa Tu Evento | Paquetes CakeBar (Basico / Premium / Luxury) con formulario de reserva |
| Asistente IA | Chat con Google Gemini para consultas sobre menu y servicios |
| Newsletter | Registro de suscriptores con confirmacion por email |
| Panel de Admin | Editor de inventario y eventos — acceso protegido solo para administradores |

---

## Arquitectura

```mermaid
graph LR
    CLIENT["Navegador\nReact 19 · TypeScript · Vite 6\nTailwind CSS 4 · Motion"]
    SERVER["Express Backend\nNode.js · Nodemailer"]
    GEMINI["Google Gemini\nAsistente IA"]
    WA["WhatsApp Business\nPedidos directos"]
    EMAIL["Gmail SMTP\nConfirmaciones"]

    CLIENT -->|"Pedido personalizado"| WA
    CLIENT -->|"Formulario contacto / reserva"| SERVER
    CLIENT -->|"Chat IA"| GEMINI
    SERVER -->|"Email de confirmacion"| EMAIL
```

---

## Stack Tecnologico

| Capa | Tecnologia |
|------|-----------|
| Frontend | React 19 · TypeScript · Vite 6 · Tailwind CSS 4 |
| Animaciones | Motion (Framer Motion v12) |
| Backend | Express 4 · Node.js |
| Email | Nodemailer + Gmail SMTP |
| IA | Google Gemini API |
| Datos | JSON files en servidor (sin base de datos) |
| Despliegue | Bluehost VPS · PM2 · Nginx |

---

## Vista Previa

<img src="assets/preview.jpeg" width="100%" alt="Cakeando Sweets Bar — Elegancia en cada bocado" />

---

## Contacto

El codigo fuente es propietario. Para consultas: [pablozam1931@gmail.com](mailto:pablozam1931@gmail.com)

---

*Parte del portfolio [deadlyrat](https://github.com/deadlyrat).*
