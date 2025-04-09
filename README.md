# VentaConecta - Documentación

## Descripción General

VentaConecta es una aplicación que conecta negocios locales con vendedores comisionistas. Permite a los negocios subir productos estancados y a los vendedores elegir qué productos quieren ofrecer, generando una comisión cuando se concreta una venta.

## Estructura del Proyecto

```
VentaConecta/
├── src/
│   ├── components/         # Componentes reutilizables
│   │   ├── CompartirProducto.jsx
│   │   ├── LoadingSpinner.jsx
│   │   ├── Navbar.jsx
│   │   └── ProtectedRoute.jsx
│   ├── views/              # Vistas principales
│   │   ├── CatalogoVendedor.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Estadisticas.jsx
│   │   ├── Login.jsx
│   │   ├── Perfil.jsx
│   │   ├── ProductosNegocio.jsx
│   │   ├── Registro.jsx
│   │   └── VentasPendientes.jsx
│   ├── firebase.js         # Configuración y funciones de Firebase
│   ├── App.jsx             # Componente principal y rutas
│   ├── main.jsx            # Punto de entrada
│   └── index.css           # Estilos globales
├── public/                 # Archivos públicos
├── index.html              # HTML principal
├── package.json            # Dependencias y scripts
├── tailwind.config.js      # Configuración de Tailwind CSS
├── vite.config.js          # Configuración de Vite
├── vercel.json             # Configuración para despliegue en Vercel
├── DEPLOYMENT.md           # Guía de despliegue
└── README.md               # Este archivo
```

## Funcionalidades Implementadas

### 1. Gestión de Productos
- Registro de productos con nombre, precio, descripción, comisión, stock e imagen
- Subida de imágenes a Firebase Storage
- Edición y eliminación de productos
- Visualización de productos en catálogo

### 2. Vista del Vendedor
- Visualización de todos los productos disponibles
- Funcionalidad para ofrecer productos con un solo clic
- Catálogo personal con productos ofrecidos
- Marcado de productos como vendidos

### 3. Confirmación de Ventas
- Registro de ventas por parte del vendedor
- Lista de "ventas pendientes" para el negocio
- Confirmación de ventas por parte del negocio
- Asignación oficial de ventas a vendedores

### 4. Panel de Estadísticas
- Visualización de total de ventas realizadas
- Visualización de total de comisiones acumuladas
- Estadísticas por producto y por mes

### 5. Compartir Productos
- Compartir por WhatsApp
- Compartir por Facebook
- Compartir nativo (usando Web Share API)

### 6. Conexión con Firebase
- Firestore para almacenamiento de productos y ventas
- Storage para imágenes
- Autenticación (pendiente de configuración)

## Tecnologías Utilizadas

- React 19 con Vite
- Firebase 11.6.0 (Firestore, Storage, Auth)
- React Router para navegación
- Tailwind CSS para estilos
- Vercel para despliegue

## Estado Actual y Próximos Pasos

### Completado
- ✅ Estructura básica del proyecto
- ✅ Conexión con Firestore para productos
- ✅ Conexión con Firestore para ventas
- ✅ Funcionalidad para compartir por WhatsApp y Facebook
- ✅ Configuración para despliegue en Vercel

### Pendiente
- ⏳ Autenticación con Firebase (roles: negocio/vendedor)
  - Requiere habilitar autenticación por email/password en la consola de Firebase
- ⏳ Empaquetar como app móvil con Capacitor (opcional)

## Guías

### Despliegue
Ver el archivo [DEPLOYMENT.md](./DEPLOYMENT.md) para instrucciones detalladas sobre cómo desplegar la aplicación en Vercel.

### Configuración de Firebase
Para completar la configuración de Firebase:
1. Acceder a la [consola de Firebase](https://console.firebase.google.com/)
2. Seleccionar el proyecto "ventaconecta-76283"
3. Ir a la sección "Authentication"
4. Habilitar el proveedor de autenticación "Email/Password"

## Contacto

Para cualquier consulta o soporte adicional, por favor contacta al equipo de desarrollo.
