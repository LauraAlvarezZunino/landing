# Frontend: Biblioteca Cortázar

## Descripción del Proyecto

**La Gran Ocasión** es una plataforma web desarrollada para la Biblioteca Julio Cortazar de la Escuela Nacional 'Ernesto Sábato',con el objetivo de fomentar la lectura, la crítica literaria y la participación comunitaria entre alumnos y docentes. Este repositorio contiene la aplicación cliente construida bajo una arquitectura **Mobile First (RNF1)** para garantizar la accesibilidad y usabilidad.

* **Desarrollado por:** Alumnos del Instituto de Formación Docente y Tecnica N°166
* **Materia:** Práctica Docente (Prof. Lucas Salvatori).

##  Características Principales (RF)

* **Autenticación Institucional:** Inicio de sesión seguro (RF1).
* **Catálogo Interactivo:** Búsqueda y filtrado avanzado de libros (RF4, RF5).
* **Comunidad y Opiniones:** Valoración de libros y participación en foros (RF10, RF11).
* **Gamificación:** Sistema de insignias y reconocimiento a lectores destacados (RF15, RF13).
* **Panel Docente:** Acceso a funciones de moderación y creación de foros de debate (RF3, RF8, RF16).

##  Stack Tecnológico

| Componente | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Framework** | **React.js** | Librería principal para construir la interfaz. |
| **Tooling** | **Vite** | Empaquetador y servidor de desarrollo rápido. |
| **UI/Estilos** | **Material-UI (MUI)** | Componentes de diseño para una interfaz intuitiva (RNF2). |
| **Llamadas API**|  Fetch | Gestión de la comunicación con el Backend. |

##  Instalación y Ejecución Local

Sigue estos pasos para levantar el entorno de desarrollo:

### 1. Prerrequisitos
Asegúrate de tener instalado [Node.js](https://nodejs.org/).

### 2. Clonar el repositorio
```bash
git clone  [https://github.com/TurcoDev/sababook-front.git] 
cd sababook-front
```
### 3. Instalacion de dependencias
npm install
### 4. Configurar Variables de Entorno
*Crea un archivo .env en la raíz del proyecto para definir la conexión con la API:
# URL base de la API del Backend (Express)
VITE_API_URL="http://localhost:3000/api/v1" 

### 5. Iniciar la Aplicación

*npm run dev
*La aplicación estará disponible en http://localhost:5173.
## Estructura del Proyecto (RNF9)
El proyecto sigue una estructura modular para garantizar la Mantenibilidad (RNF9):
*src/components: Componentes reutilizables de UI (ej. TarjetaLibro, Header).
*src/pages: Vistas principales de la aplicación (ej. /Home, /BookDetails).
*src/services: Módulos para las llamadas a la API (separa la lógica de datos de la UI).
*src/themes: Configuración de estilos y temas de MUI.





























## Descripción del Proyecto

#  Backend API: Biblioteca Cortázar

**La Gran Ocasión** es una plataforma web desarrollada para la Biblioteca Julio Cortazar de la Escuela Nacional 'Ernesto Sábato',con el objetivo de fomentar la lectura, la crítica literaria y la participación comunitaria entre alumnos y docentes. Este repositorio contiene la aplicación cliente construida bajo una arquitectura **Mobile First (RNF1)** para garantizar la accesibilidad y usabilidad.

* **Desarrollado por:** Alumnos del Instituto de Formación Docente y Tecnica N°166
* **Materia:** Práctica Docente (Prof. Lucas Salvatori).

Este repositorio contiene el servicio de **API RESTful** para la Biblioteca E. Cortázar. Es responsable de manejar la lógica de negocio, la persistencia de datos (Supabase/PostgreSQL), la seguridad (RF17) y el control de acceso basado en roles (RF3).

* **Arquitectura:** Modelo Vista Controlador (MVC) (RNF9).
* **Objetivo de Rendimiento:** Asegurar un tiempo de respuesta rápido (RNF3).

##  Stack Tecnológico

| Componente | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Framework** | **Express.js** (Node.js) | Creación rápida de la API REST. |
| **Base de Datos**| **Supabase (PostgreSQL)** | Persistencia de datos, alta confiabilidad (RNF7). |
| **Seguridad** | **JWT** | Mecanismo para la autenticación y control de sesión. |

##  Instalación y Ejecución Local

### 1. Prerrequisitos
* [Node.js](https://nodejs.org/)
* Una cuenta y proyecto activo en [Supabase](https://supabase.com/).

### 2. Clonar el repositorio
```bash
git clone [https://github.com/TurcoDev/sababook-back.git]
cd sababook-back
### 3. Instalar Dependencias

npm install
### 4. Configurar Variables de Entorno
Crea un archivo .env en la raíz con la siguiente información:
Fragmento de código
# Configuración de la API
PORT=3000
JWT_SECRET="una_clave_secreta_fuerte_aqui"

# Conexión a Supabase/PostgreSQL
SUPABASE_URL="https://supabase.com/docs/reference/cli/introduction"
SUPABASE_KEY="[Clave de servicio (service_role) de Supabase]"

# Opcional: Clave inicial para crear el primer usuario Admin
ADMIN_INITIAL_KEY="ADMIN1234"

### 5. Iniciar el Servidor


npm run dev

El servidor estará disponible en http://localhost:3000.

