# LorHels-Nails

---

## 🏗️ Arquitectura y Tecnologías Core

La aplicación está diseñada bajo un enfoque de **Desarrollo Serverless Moderno**:

* **Frontend Estilizado:** Uso de **Tailwind CSS** con configuración extendida para una estética premium y oscura (`#0F172A`) con acentos en luces neón, optimizado para ser 100% responsivo.
* **Motor Base de Datos (Firebase Firestore):** Conexión activa en tiempo real (`onSnapshot`) que sincroniza instantáneamente el inventario, las citas y el equipo sin necesidad de recargar las páginas.
* **Capa de Seguridad (Firebase Auth):** Separación estricta entre las vistas públicas y el panel administrativo mediante autenticación por correo y contraseña.
* **Pasarela de Despacho (WhatsApp API):** Integración nativa para que tanto las reservas como las compras se envíen con plantillas de texto formateadas directamente al número del negocio.

---

## 📄 Desglose Funcional de las 4 Páginas

Hemos segmentado las responsabilidades del sistema en cuatro archivos independientes:

| Archivo | Rol en el Ecosistema | Lógica e Integraciones JavaScript Incorporadas |
| --- | --- | --- |
| **`index.html`** | **Página de Aterrizaje (Home)** | Presentación de la marca, catálogo estático de servicios principales, navegación fluida a través de enlaces reales y menú móvil interactivo. |
| **`reserva.html`** | **Subsistema de Citas Web** | Carga dinámica de servicios y especialistas desde Firebase. **Bloqueo dinámico de horarios ocupados** por fecha para evitar duplicados. Envío de la reserva a la base de datos y apertura automática de comprobante en WhatsApp. |
| **`tienda.html`** | **E-commerce (Supply Shop)** | Buscador reactivo de productos, **generador automático de filtros por categoría**, control de stock disponible en vivo, gestión de estado del carrito de compras (subtotales/totales) y pasarela de pedido vía WhatsApp. |
| **`admin.html`** | **Panel de Control y POS** | **Filtro de seguridad por Login**. Monitoreo financiero en tiempo real (ingresos del día y contador de movimientos), **Punto de Venta integrado (POS)** para registrar cobros en el local, y consolas de administración (CRUD) para modificar servicios, inventario (con alertas de stock bajo) y staff. |

---

## ⚡ Componentes Globales Reutilizados

En cada archivo mantienes la misma consistencia de interfaz gracias a:

1. **Sistema de Notificaciones Premium (Toasts):** Alertas flotantes personalizadas en la esquina de la pantalla que avisan de forma sutil al usuario cuando un producto se agrega, una cita se confirma o hay un error.
2. **Biblioteca de Iconos Uniforme:** Uso de **Lucide Icons** para mantener la iconografía limpia y moderna en todas las barras de navegación, botones y tablas.