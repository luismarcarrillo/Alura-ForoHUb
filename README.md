# ForoHub

ForoHub es un proyecto backend en Java usando Spring Boot, que implementa un foro con funcionalidad completa. Los usuarios pueden crear, listar y eliminar tópicos, utilizando seguridad basada en JWT.

## Tecnologías Utilizadas
- **Java 17+**
- **Maven 4+**
- **Spring Boot 3+**
- **MySQL 8+**
- **IntelliJ IDEA** (opcional)

## Dependencias
- Lombok
- Spring Web
- Spring Boot DevTools
- Spring Data JPA
- Flyway Migration
- MySQL Driver
- Validation
- Spring Security

## Configuración

### Variables de Entorno
```properties
spring.application.name=foro_hub
spring.datasource.url=jdbc:mysql://localhost/foro_hub
spring.datasource.username=root
spring.datasource.password=${DB_PASS}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
server.error.include-stacktrace=never
api.security.secret=${JWT_SECRET}
```

### Base de Datos
Usa MySQL; asegúrate de configurarlo correctamente y ajustar `DB_PASS`.

## Endpoints de API
- **Listar Tópicos:** `GET /topicos`
- **Crear Tópico:** `POST /topicos` (requiere autenticación)
- **Autenticación:** `POST /auth` (devuelve JWT)
- **Eliminar Tópico:** `DELETE /topicos/{id}` (requiere autenticación)
