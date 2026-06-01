# PostContenido 1 - Unidad 11

## Refactorización y Arquitectura en Capas con Spring Boot

### Autor

Camilo Sánchez


## Arquitectura Implementada

La aplicación está organizada siguiendo una arquitectura en capas.

---

```text
Cliente HTTP
      |
      v
+------------------+
| ProductoController|
+------------------+
          |
          v
+------------------+
| ProductoService  |
| (Interface)      |
+------------------+
          |
          v
+-------------------------+
| ProductoServiceImpl     |
+-------------------------+
          |
          v
+------------------+
| ProductoRepository|
+------------------+
          |
          v
+------------------+
|    Producto      |
|     Entity       |
+------------------+

          ^
          |
+----------------------+
| ProductoFactory      |
+----------------------+

          ^
          |
+----------------------+
| DTOs                 |
| ProductoRequestDTO   |
| ProductoResponseDTO  |
+----------------------+

          ^
          |
+----------------------+
| GlobalExceptionHandler|
+----------------------+
```

---

## Estructura del Proyecto

```text
src
└── main
    ├── java
    │   └── com.universidad.productos
    │
    ├── controller
    ├── service
    ├── repository
    ├── dto
    ├── entity
    ├── factory
    └── exception
    │
    └── resources
        └── application.properties
```
---
## Conclusiones

Se aplicaron correctamente principios SOLID y patrones de diseño como DAO, DTO y Factory para mejorar la organización del proyecto. Además, se implementó un manejo global de excepciones mediante `@RestControllerAdvice`, permitiendo respuestas consistentes y profesionales para errores de validación, recursos inexistentes y errores internos del servidor.
