# Gestión de Producción de Muebles 🛠️

Este proyecto ha sido diseñado como una solución integral para la gestión eficiente de la producción en fábricas de muebles. Incluye un conjunto de funcionalidades que permiten administrar de manera dinámica los recursos humanos, los pedidos de clientes y la selección de materiales necesarios para la fabricación. Una de las características principales es la asignación automática de empleados a los pedidos, lo que garantiza una optimización en la distribución de la carga laboral y la reducción de tiempos de espera.

El sistema está compuesto por dos partes principales:
- **Backend**: Desarrollado en Java con Spring Boot, este módulo maneja toda la lógica de negocio, como la asignación inteligente de empleados, la gestión de pedidos y notificaciones automáticas. También ofrece una API REST segura y robusta para interactuar con el frontend.
- **Frontend**: Construido con Svelte, proporciona una interfaz moderna e intuitiva que permite a los administradores y clientes interactuar con el sistema de manera sencilla. Incluye funcionalidades como la visualización del estado de pedidos, la gestión de empleados y la personalización de materiales para cada proyecto.

El principal objetivo del proyecto es optimizar los procesos productivos en fábricas de muebles, teniendo en cuenta factores clave como la disponibilidad diaria de empleados, las especificaciones individuales de cada pedido, y el manejo eficiente de tiempos y recursos. Esto lo convierte en una herramienta poderosa para mejorar la productividad y la toma de decisiones en tiempo real.

---

## 🚀 Funcionalidades Principales

### **Frontend (Svelte)**
- **Inicio de sesión:**
  - Permite a los administradores y clientes autenticarse.
  - Gestión de roles para restringir accesos.
  
- **Gestión de empleados:**
  - Actualización de asistencia diaria.
  - Visualización de notificaciones importantes según las horas trabajadas.
  
- **Gestión de pedidos:**
  - Asignación automática de empleados a los pedidos.
  - Visualización del estado y tiempo estimado de los pedidos.
  
- **Gestión de muebles y materiales:**
  - CRUD completo (crear, leer, actualizar y eliminar) de muebles y materiales.
  - Selección personalizada de materiales para cada pedido.

### **Backend (Spring Boot)**
- **Gestión de empleados:**
  - Registro de asistencia diaria.
  - Generación de notificaciones automáticas cuando los empleados superan ciertos umbrales de horas trabajadas.

- **Asignación de empleados a pedidos:**
  - Lógica avanzada para asignar empleados de manera eficiente.
  - Manejo de pedidos demorados y reprogramación automática.
  
- **Optimización de tiempo de producción:**
  - Ajuste dinámico de tiempos estimados según la carga laboral disponible.

- **API REST:**
  - Endpoints seguros para interactuar con el frontend.
  - Documentación de API generada automáticamente.

---

## 🛠️ Tecnologías Utilizadas

### **Frontend**
- [Svelte](https://svelte.dev/) - Framework de desarrollo para interfaces de usuario rápidas y dinámicas.
- `svelte-routing` - Librería para manejar rutas en la aplicación.

### **Backend**
- [Spring Boot](https://spring.io/projects/spring-boot) - Framework para construir aplicaciones robustas en Java.
- `Spring Data JPA` - Para interactuar con la base de datos.
- `H2 Database` - Base de datos embebida para pruebas locales.
- `MySQL` - Base de datos relacional para producción. ```

---

## 📂 Estructura del Proyecto

### **Frontend**
```plaintext
  src/
  ├── App.svelte            # Componente principal
  ├── pages/                # Páginas individuales de la aplicación
  │   ├── Index.svelte         # Página de inicio
  │   ├── LoginCliente.svelte  # Login para clientes
  │   ├── InicioAdmin.svelte   # Dashboard del administrador
  │   ├── PedidosCliente.svelte# Gestión de pedidos para clientes
  │   └── AsignacionEmpleados.svelte # Gestión de empleados
  ├── axiosConfig.js        # Configuración de Axios para las solicitudes HTTP
  └── main.js               # Archivo principal para inicializar la app


```
### **Backend**

```
src/
├── main/java/com/example/BackendCoreMuebles/
│   ├── Modelos/          # Clases que representan las entidades del sistema
│   ├── Repositorio/      # Interfaces JPA para interactuar con la base de datos
│   ├── Controladores/    # Endpoints de la API REST
│   └── Servicio/         # Lógica de negocio y asignación automática

```


---

## 🌐 Endpoints Principales de la API REST

### **Empleados**
- **GET** `/api/empleados` - Obtener todos los empleados.
- **POST** `/api/empleados` - Crear un nuevo empleado.
- **PUT** `/api/empleados/{id}` - Actualizar un empleado existente.
- **DELETE** `/api/empleados/{id}` - Eliminar un empleado.

### **Pedidos**
- **GET** `/api/pedidos` - Obtener todos los pedidos.
- **POST** `/api/pedidos` - Crear un nuevo pedido.
- **PUT** `/api/pedidos/{id}` - Actualizar un pedido existente.
- **DELETE** `/api/pedidos/{id}` - Eliminar un pedido.

### **Asignaciones**
- **GET** `/api/asignaciones` - Obtener todas las asignaciones.
- **POST** `/api/asignaciones` - Asignar empleados a un pedido.
- **PUT** `/api/asignaciones/liberar/{id}` - Liberar empleados de un pedido.


## 🔧 Configuración del Proyecto

### **Frontend**
1. **Clonar el repositorio del frontend.**
   ```
   git clone https://github.com/AleFe2425/Proyecto-Core-Muebles.git
   
   cd frontend

2. **Instalar las dependencias:**
   ```
   npm install
   
3. **Ejecutar el servidor de desarrollo:**
   ```
   npm run dev

### **Backend**
1. **Clonar el repositorio del backend.**
   ```
   git clone https://github.com/AleFe2425/Proyecto-Core-Muebles.git
   cd backend

2. **Configurar la base de datos MySQL en el archivo application.properties:**
   ```
   spring.datasource.url=jdbc:mysql://localhost:3306/mueblesdb
   spring.datasource.username=tu_usuario
   spring.datasource.password=tu_contraseña
   
3. **Compilar y ejecutar el backend:**
   ```
   ./mvnw spring-boot:run

## 🧾 Evidencias del Proyecto

**Videos**
1. Video Youtube Defensa del Reto Core: https://youtu.be/OShEKWfVLss
2. Video Defensa Core: https://youtu.be/yHwznkB7uQE

**Link**
1. Link Proyecto Deployado (Svelte app): https://frontend-muebles.vercel.app/admin



   
   
