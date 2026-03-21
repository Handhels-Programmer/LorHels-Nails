# LorHels-Nails

---

## 🏗️ Arquitectura del Proyecto

### 1. Núcleo de Datos (Firebase Backend)
* **Base de Datos (Firestore):** Utilizas una base de datos NoSQL para almacenar el catálogo de productos (nombre, precio, imagen, descripción).
* **Autenticación:** Un sistema de login para separar la vista del cliente de las funciones críticas de administración.
* **Sincronización:** El catálogo se actualiza automáticamente en la web cada vez que haces un cambio en la base de datos, sin necesidad de refrescar.

### 2. Interfaz de Usuario (Frontend)
* **Estética "Cyberpunk/Luxury":** Un diseño oscuro con acentos en azul neón (`#00D4FF`) y fuentes modernas, construido totalmente con **Tailwind CSS**.
* **Navegación Dinámica:** Un sistema que oculta y muestra secciones (Inicio, Catálogo, Admin) manipulando el DOM con JavaScript, lo que hace que la carga sea instantánea.
* **Diseño Responsivo:** Menús y rejillas de productos que se adaptan perfectamente a celulares y computadoras.

### 3. Sistema de Ventas (Carrito de Compras)
* **Lógica de Estado:** Un arreglo (`array`) en JavaScript que rastrea qué productos elige el usuario y sus cantidades.
* **Cálculos en Tiempo Real:** Suma automática de subtotales y total general.
* **Feedback Visual:** El sistema de **Toasts** (notificaciones flotantes) que acabamos de añadir para confirmar acciones al usuario.

### 4. Panel Administrativo (CMS)
* **Gestor de Inventario:** Un formulario para subir nuevos productos directamente a Firebase.
* **Control de Catálogo:** Funciones para editar o eliminar productos existentes en tiempo real.
* **Seguridad Básica:** Protección de la vista administrativa mediante validación de credenciales.

---

### 📊 Resumen de Flujo de Datos

| Componente | Función Principal | Tecnología |
| :--- | :--- | :--- |
| **Almacenamiento** | Guardar fotos y datos de productos | Firebase Firestore |
| **Estilos** | Dar el aspecto neón y moderno | Tailwind CSS |
| **Iconografía** | Símbolos visuales (carrito, check, login) | Lucide Icons |
| **Lógica** | Sumar precios, abrir modales, enviar datos | JavaScript (Vanilla) |
