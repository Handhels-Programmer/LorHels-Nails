# LorHels-Nails

---

Actualmente tenemos una **Single Page Application (SPA)** de nivel profesional que integra desarrollo frontend moderno con base de datos en la nube en tiempo real.

### 1. Arquitectura del Sistema y Módulos Activos

* **Sistema de Navegación por Estado (SPA):** Controlado dinámicamente mediante la función `window.showView(viewId)`. Cambia entre Inicio, Reservas, Tienda y Panel de Administración de manera instantánea manipulando clases de Tailwind (`active-view` / `hidden-view`) sin recargar el navegador.
* **Tienda Supply Automatizada por Categorías:** Los productos se agrupan en tiempo real mediante un reductor en JavaScript según el campo `category` registrado. Cuenta con una barra de búsqueda reactiva (`oninput`) que filtra el catálogo localmente combinando texto y categorías activas.
* **Carrito de Compras Premium y Localizado:** Un sistema basado en un arreglo (`cart`) estructurado en dos columnas (`lg:grid-cols-12`) que sitúa el pedido al lado derecho en pantallas grandes. Realiza cálculos automáticos de subtotal y total general, renderiza dinámicamente el HTML e incluye el nuevo **Sistema de Notificaciones Flotantes (Toasts)** animado con Tailwind para dar feedback visual inmediato sin pausar la pantalla.
* **Integración de Pasarela de Despacho (WhatsApp):** La función `window.checkoutWhatsApp()` procesa el arreglo del carrito, desglosa cantidades, precios individuales y subtotales, e inyecta un recibo limpio y codificado mediante `encodeURIComponent` hacia la API de WhatsApp.
* **Panel Administrativo y Agenda (CMS):** Un módulo protegido por estados de autenticación que permite la inyección directa de nuevos Servicios, Especialistas y Productos (con especificación de stock, precio numérico y categoría) directamente a colecciones indexadas.

---

### 📦 Resumen de la Ficha Técnica actual

| Módulo | Componente Técnico | Propósito en el Código |
| --- | --- | --- |
| **Diseño** | Tailwind CSS + Lucide | Estética responsiva Cyberpunk/Luxury e iconografía SVG dinámica. |
| **Reactividad** | `onSnapshot` (Firebase) | Sincronización asíncrona bidireccional inmediata de inventario y citas. |
| **Estructura** | JavaScript ES6 Modules | Encapsulamiento de lógica avanzada (requiere vinculación explícita a `window`). |
| **UX Avanzado** | DOM Injection + CSS Keyframes | Renderizado de cuadrículas simétricas (`grid-cols-2`) y Toasts animados. |
