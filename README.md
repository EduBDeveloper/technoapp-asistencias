
![1](https://github.com/user-attachments/assets/9800ae21-6dc1-46af-8a27-bed18c82158f)


# 🛠️ Sistema de Registro de Asistencias Técnicas – TechnoApp

Este es un sistema completo de gestión de asistencias técnicas desarrollado con Spring Boot para el backend, PostgreSQL como base de datos y HTML/CSS/JavaScript para el frontend. El sistema permite registrar técnicos, empresas y asistencias, incluyendo funcionalidades de búsqueda, filtros, paginación y edición.

---

## 📌 Características principales

- Registro, edición y eliminación de técnicos.
- Registro y edición de empresas.
- Registro de asistencias técnicas con selección de empresa, técnico, fecha y comentarios.
- Filtros por empresa y fecha.
- Paginación de asistencias.
- Dashboard con métricas como:
  - Asistencias del día.
  - Técnicos activos.
  - Total de empresas.
- Interfaz moderna y adaptable (HTML5, Bootstrap 5, Boxicons).

---

## 🧱 Tecnologías utilizadas

### 🔙 Backend:
- **Spring Boot** – Framework principal para la API REST.
- **Spring Web** – Para la gestión de controladores y endpoints REST.
- **Spring Data JPA** – Para persistencia de datos.
- **Hibernate** – ORM por defecto de JPA.
- **PostgreSQL** – Motor de base de datos relacional.

### 🧑‍🎨 Frontend:
- **HTML5, CSS3, JavaScript**
- **Bootstrap 5**
- **Boxicons / Font Awesome**

---

## 📁 Estructura del proyecto

technoapp/
├── backend/
│ ├── controller/
│ ├── service/
│ ├── repository/
│ ├── entities/
│ └── application.properties
├── frontend/
│ ├── index.html
│ ├── empresas.html
│ └── tecnicos.html
├── db/
│ └── esquema_postgresql.sql


---

## 🚀 Instalación y ejecución

### 1. Clonar el repositorio

git clone https://github.com/tu-usuario/technoapp.git
cd technoapp
2. Configurar la base de datos PostgreSQL
Crear una base de datos llamada technoapp_db.

2. Ajustar credenciales en application.properties:

spring.datasource.url=jdbc:postgresql://localhost:5432/technoapp_db
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update

3. Ejecutar la aplicación Spring Boot
   mvn spring-boot:run

4. Abrir el frontend
Abre index.html o empresas.html en tu navegador. El frontend se conecta al backend en http://localhost:8080/api.


📌 Endpoints principales
Recurso	Método	Ruta	Descripción
Empresa	GET	/api/empresas	Listar empresas
Empresa	POST	/api/empresas	Crear empresa
Empresa	PUT	/api/empresas/{id}	Actualizar empresa
Técnico	GET	/api/clientes	Listar técnicos
Técnico	POST	/api/clientes	Crear técnico
Técnico	PUT	/api/clientes/{id}	Actualizar técnico
Asistencia	POST	/api/asistencias	Registrar asistencia
Asistencia	GET	/api/asistencias	Listar asistencias
Asistencia	GET	/api/asistencias/paginado	Asistencias con filtros y paginación


✍️ Autor
👨‍💻 Desarrollado por: Eduardo Balbuena

🎓 Estudiante de UTIC – Sede San Lorenzo

📫 Contacto: edubalbuena9@gmail.com



