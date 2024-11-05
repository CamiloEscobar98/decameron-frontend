# Proyecto Hoteles Decameron - Frontend

Este proyecto es la interfaz de usuario desarrollada en Vue 3 para gestionar los hoteles de la cadena Decameron. La aplicación permite a los gerentes visualizar, agregar, editar y eliminar hoteles y sus habitaciones. Se conecta a la API REST desarrollada en Laravel.

## Tecnologías Utilizadas

- **Framework**: Vue 3 con Composition API
- **Enrutador**: Vue Router
- **Manejo de Estado**: Pinia (opcional, si se requiere estado global)
- **Estilos**: Tailwind CSS (o el framework CSS de tu elección)
- **Petición HTTP**: Axios para comunicación con la API
- **Autenticación**: JWT o Bearer Token (opcional, según configuración de la API)

## Configuración del Proyecto

1. **Clona el repositorio**:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd nombre_del_proyecto_frontend
   ```
2. **Instala las dependencias**:

   ```bash
   npm install

   ```

3. **Configura las variables de entorno**:
   Crea un archivo .env en la raíz del proyecto y agrega la URL base de la API

   ```bash
   VITE_API_BASE_URL=http://localhost:8000/api
   ```

## Ejecución del Proyecto

Para ejecutar la aplicación en un entorno de desarrollo, utiliza:

```bash
npm run dev
```

## Comandos Disponibles

- Iniciar el servidor de desarrollo: npm run dev
- Compilar para producción: npm run build

## Estructura del Proyecto

- src/components: Contiene componentes reutilizables como formularios de hoteles y habitaciones, tablas de listado, etc.
- src/views: Vistas principales de la aplicación (páginas).
- src/router: Configuración de rutas para navegación entre páginas.
- src/store: Manejo de estado (opcional, con Pinia o Vuex).
- src/assets: Archivos estáticos como imágenes o íconos.

## Funcionalidades

La aplicación proporciona las siguientes vistas y funcionalidades:

- **Vista de Hoteles:** Listado de todos los hoteles registrados.
- **Formulario de Registro/Edición de Hotel:** Permite agregar o editar un hotel.
- **Gestión de Habitaciones:**
  - Ver habitaciones de un hotel específico.
  - Agregar, editar y eliminar habitaciones con validaciones de tipo y acomodación.
- **Notificaciones:** Muestra mensajes de éxito o error según las acciones realizadas en la API.

## Integración con la API

Las peticiones a la API se configuran en src/services/api.js, usando Axios. Ejemplo de configuración de Axios para manejar la URL base:

```bash
import axios from 'axios';

const api = axios.create({
  baseURL: import.meta.env.VITE_API_BASE_URL,
});

export default api;

```

## Buenas Prácticas y Consideraciones

- **Manejo de Errores:** Asegúrate de manejar errores de las peticiones API en cada acción.
- **Validación en Formularios:** Implementa validaciones en formularios según las reglas de negocio (como el tipo y número de habitaciones).
- **Componentización:** Divide la interfaz en componentes reutilizables para mantener el código modular.
- Accesibilidad y Responsividad: Optimiza el diseño para portátiles de 13 y 15 pulgadas, y asegúrate de que la aplicación sea accesible y responsive.

## Compilación para Producción

Para compilar el proyecto para un entorno de producción:

```bash
npm run build
```

## Licencia

Este proyecto es una prueba técnica.