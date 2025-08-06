
# 🛠️ Sistema de Registro de Asistencias Técnicas – TechnoApp

Este es un sistema completo de gestión de asistencias técnicas desarrollado con **Spring Boot** para el backend, **PostgreSQL** como base de datos y **HTML/CSS/JavaScript** para el frontend.  
El sistema permite registrar técnicos, empresas y asistencias, incluyendo funcionalidades de búsqueda, filtros, paginación y edición.

---

## 📌 Características principales

- ✅ Registro, edición y eliminación de **técnicos**
- ✅ Registro y edición de **empresas**
- ✅ Registro de **asistencias técnicas** con selección de empresa, técnico, fecha y comentarios
- ✅ Filtros por empresa y fecha
- ✅ Paginación de asistencias
- ✅ **Dashboard** con métricas:
  - Asistencias del día
  - Técnicos activos
  - Total de empresas
- 🎨 Interfaz moderna y adaptable (HTML5, Bootstrap 5, Boxicons)

---

## 🧱 Tecnologías utilizadas

### 🧠 Backend
- Java 17  
- Spring Boot 3+  
- Spring Web  
- Spring Data JPA  
- Spring Validation  
- PostgreSQL  
- Lombok  

### 🧑‍🎨 Frontend
- HTML5, CSS3, JavaScript  
- Bootstrap 5  
- Boxicons / Font Awesome  

---

## 📦 Dependencias
Revisar el archivo `pom.xml` para ver todas las dependencias necesarias.

---

## 📁 Estructura del proyecto

gestion/
├── frontend/
│ ├── index.html
│ ├── empresas.html
│ ├── tecnicos.html
│ └── img/
├── src/
│ └── main/
│ ├── java/com.coditech.gestion/
│ │ ├── config/ # Configuraciones globales (CORS)
│ │ ├── controller/ # Controladores REST
│ │ ├── dto/ # Objetos de transferencia (Dashboard)
│ │ ├── entities/ # Entidades JPA
│ │ ├── model/ # Modelos adicionales
│ │ ├── repository/ # Interfaces JpaRepository
│ │ └── service/ # Lógica de negocio
│ ├── resources/
│ │ └── application.properties # Configuración de PostgreSQL
│ └── GestionApplication.java # Clase principal Spring Boot
├── pom.xml # Dependencias del proyecto

yaml
Copiar
Editar

---

## 🧠 Endpoints REST

### 📁 Empresas

| Método | Endpoint               | Descripción              |
|--------|------------------------|--------------------------|
| GET    | `/api/empresas`        | Lista todas las empresas |
| POST   | `/api/empresas`        | Crea una nueva empresa   |
| PUT    | `/api/empresas/{id}`   | Edita una empresa        |
| DELETE | `/api/empresas/{id}`   | Elimina una empresa      |

### 👷 Técnicos (Clientes)

| Método | Endpoint               | Descripción                  |
|--------|------------------------|------------------------------|
| GET    | `/api/clientes`        | Lista todos los técnicos     |
| POST   | `/api/clientes`        | Crea un técnico nuevo        |
| PUT    | `/api/clientes/{id}`   | Edita un técnico existente   |
| DELETE | `/api/clientes/{id}`   | Elimina un técnico           |

### 🛠️ Asistencias Técnicas

| Método | Endpoint                         | Descripción                   |
|--------|----------------------------------|-------------------------------|
| GET    | `/api/asistencias`               | Lista todas las asistencias   |
| GET    | `/api/asistencias/paginado`      | Lista paginada con filtros    |
| POST   | `/api/asistencias`               | Registra una nueva asistencia |

---

## 🚀 Instalación y ejecución

1. **Clonar el repositorio**

```bash
git clone https://github.com/EduBDeveloper/technoapp-asistencias
cd gestion
Configurar la base de datos PostgreSQL

Crear una base de datos llamada gestiondb

Ajustar credenciales en src/main/resources/application.properties:

properties

spring.datasource.url=jdbc:postgresql://localhost:5432/gestiondb (Asegurate de poner correctanmente tus credenciales y haber creado la base de datos postgres)
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
Ejecutar la aplicación Spring Boot

bash
Copiar
Editar
mvn spring-boot:run
Abrir el frontend

Abre index.html o empresas.html en tu navegador.
El frontend se conecta al backend en: http://localhost:8080/api

✍️ Autor
👨‍💻 Desarrollado por: Eduardo Balbuena
🎓 Estudiante de UTIC – Sede San Lorenzo
📫 Contacto: edubalbuena9@gmail.com


