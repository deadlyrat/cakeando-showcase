<div align="center">

<img src="assets/screenshots/01-inicio.png" width="80%" alt="Página de inicio de Cakeando Sweets Bar con el mensaje principal, el botón Ver Menú y la navegación">

# Cakeando Sweets Bar

![Privado](https://img.shields.io/badge/C%C3%B3digo-Privado%20%C2%B7%20Proyecto%20Cliente-red?style=flat)
![React](https://img.shields.io/badge/React%2019-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite%206-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS%204-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)

**Sitio web full-stack para una boutique de repostería artesanal en Panamá, con catálogo interactivo, constructor de tortas personalizado y sistema de reservas para eventos.**

**[Ver el sitio en producción](https://cakeandosweetsbar.sytes.net/)**

</div>

> Este es un **portafolio showcase**: el código fuente es propietario y no está incluido.

---

## Contenido

- [El Problema](#el-problema)
- [La Solución](#la-solución)
- [Funcionalidades](#funcionalidades)
- [Vista Previa](#vista-previa)
- [Arquitectura](#arquitectura)
- [Stack Tecnológico](#stack-tecnológico)
- [Instalación local](#instalación-local)
- [Roadmap](#roadmap)
- [Contacto](#contacto)

---

## El Problema

Una pastelería artesanal en Panamá necesitaba una presencia digital que transmitiera el nivel premium de sus productos y le permitiera:

- Mostrar su catálogo con disponibilidad actualizada sin depender de un desarrollador.
- Recibir pedidos personalizados de tortas sin gestión manual de chats.
- Gestionar reservas para su servicio de CakeBar en eventos.
- Actualizar inventario y próximos eventos desde un panel simple.

---

## La Solución

Un sitio web full-stack con React 19 y un backend Express ligero que maneja los correos, la persistencia de inventario y eventos, y el flujo de pedidos hacia WhatsApp, todo integrado en una experiencia de navegación fluida con transiciones animadas entre páginas.

---

## Funcionalidades

| Funcionalidad | Descripción |
|---------------|-------------|
| Constructor de Tortas | Asistente de 5 pasos (Base, Frosting, Relleno, Toppings, Drizzle) que genera un pedido prellenado por WhatsApp |
| Catálogo de Menú | 5 pestañas (Todo, Exclusivo, Cakeando tu Dulce, Cake 8x8, Por Temporada) con disponibilidad desde el inventario |
| Pa' Tu Evento | Paquetes CakeBar (Básico / Premium / Luxury), orden personalizada y formulario de reserva |
| Inicio dinámico | Hero, feed de próximos eventos, colecciones destacadas y registro al newsletter |
| Contacto | Formulario por correo y chat directo por WhatsApp, con botón flotante en todo el sitio |
| Newsletter | Registro de suscriptores con confirmación por correo |
| Panel de Admin | Editor de inventario y eventos, con acceso protegido solo para administradores |
| Páginas informativas y legales | Nuestra Historia, Política de Privacidad y Términos |

---

## Vista Previa

### Inicio

La portada presenta la propuesta de la marca con un titular grande. El **Mensaje principal** (1) resume la idea de elegancia artesanal, el **Botón Ver Menú** (2) lleva directo al catálogo y la **Navegación** (3) da acceso a todas las secciones.

<img src="assets/screenshots/01-inicio.png" width="100%" alt="Página de inicio con el mensaje principal, el botón Ver Menú y la navegación resaltados">

En móvil la navegación se recoge en un menú compacto. El **Mensaje principal** (1) y el **Botón Ver Menú** (2) siguen visibles sin desplazarse.

<img src="assets/screenshots/01-inicio-mobile.png" width="40%" alt="Página de inicio en móvil con el mensaje principal y el botón Ver Menú resaltados">

### Menú

El catálogo muestra los productos en tarjetas. El **Título del menú** (1) abre la página, los **Filtros de categoría** (2) permiten ver solo una línea de productos y cada **Tarjeta de producto** (3) incluye precio, descripción y un enlace para consultar.

<img src="assets/screenshots/02-menu.png" width="100%" alt="Página del menú con el título, los filtros de categoría y una tarjeta de producto resaltados">

### Especialidades

Esta página reúne los pedidos especiales. El **Título de la página** (1) presenta la sección, la **Imagen de la obra** (2) muestra el producto y el **Pastel de bodas** (3) abre la descripción detallada de cada especialidad.

<img src="assets/screenshots/03-especialidades.png" width="100%" alt="Página de especialidades con el título, la imagen de la obra y el encabezado del pastel de bodas resaltados">

### Cake Bar

El Cake Bar es la estación interactiva para eventos. El **Título del Cake Bar** (1) presenta la experiencia y la sección de **Montaje a medida** (2) muestra cómo se arma la barra para cada celebración.

<img src="assets/screenshots/04-cake-bar.png" width="100%" alt="Página del Cake Bar con el título y la sección de montaje a medida resaltados">

### Pa' Tu Evento

Aquí se solicita el servicio para una celebración. El **Título** (1) abre la solicitud, la opción **Orden personalizada** (2) se elige junto a la de CakeBar en tu evento y el **Paquete popular** (3) destaca la opción más elegida entre los tres paquetes.

<img src="assets/screenshots/05-pa-tu-evento.png" width="100%" alt="Página de reservas con el título, la opción de orden personalizada y el paquete popular resaltados">

### Contacto

La página de contacto ofrece dos vías. El **Título de contacto** (1) abre la sección, el enlace **Chat por WhatsApp** (2) da respuesta inmediata y el botón **Enviar mensaje** (3) envía el formulario.

<img src="assets/screenshots/06-contacto.png" width="100%" alt="Página de contacto con el título, el chat por WhatsApp y el botón de enviar mensaje resaltados">

---

## Arquitectura

```mermaid
graph LR
    CLIENT["Navegador<br/>React 19 · TypeScript · Vite 6<br/>Tailwind CSS 4 · Motion"]
    SERVER["Backend Express<br/>Node.js · Nodemailer"]
    DATA[("Archivos JSON<br/>inventario · eventos")]
    WA["WhatsApp Business<br/>Pedidos directos"]
    EMAIL["Gmail SMTP<br/>Confirmaciones"]

    CLIENT -->|"Pedido personalizado"| WA
    CLIENT -->|"Contacto · reserva · newsletter · admin"| SERVER
    SERVER -->|"Lectura y escritura"| DATA
    SERVER -->|"Correo de confirmación"| EMAIL
```

**API REST:** `POST /api/contact`, `POST /api/reservation`, `POST /api/newsletter`, `GET /api/inventory`, `GET /api/events`, y rutas de administración protegidas con HTTP Basic (verificación, inventario y eventos).

La navegación es por estado dentro de `App.tsx` (sin react-router), con transiciones de página mediante `AnimatePresence` de Motion.

---

## Stack Tecnológico

| Capa | Tecnología |
|------|-----------|
| Frontend | React 19 · TypeScript 5.8 · Vite 6 · Tailwind CSS 4 |
| Animaciones | Motion (Framer Motion v12) |
| Iconos | Lucide React · React Icons |
| Backend | Express 4 · Node.js 18+ |
| Correo | Nodemailer + Gmail SMTP |
| Datos | Archivos JSON en el servidor (sin base de datos) |
| Despliegue | Bluehost VPS · PM2 · Nginx |

---

## Instalación local

> **Aviso:** el código es privado y propietario. Estos pasos son solo para colaboradores autorizados con acceso al repositorio.

1. Instala Node.js 18 o superior.
2. Instala las dependencias:
   ```bash
   npm install
   ```
3. Copia `.env.example` a `.env` y completa tus propios valores.
4. Inicia el entorno de desarrollo:
   ```bash
   npm run dev
   ```
5. Para producción, compila y arranca el servidor:
   ```bash
   npm run build:all
   npm start
   ```

---

## Roadmap

- [ ] Reemplazar las imágenes de stock por fotos reales de producto.
- [ ] Carrito y sistema de pedidos en línea (hoy el icono de bolsa es un marcador de posición).
- [ ] Sección de Horarios en la página de Contacto.
- [ ] Cargar eventos reales desde el panel de administración.

---

## Contacto

El código fuente es propietario. Para consultas, visita el perfil de GitHub: [github.com/deadlyrat](https://github.com/deadlyrat).

---

*Parte del portafolio de [deadlyrat](https://github.com/deadlyrat)*
