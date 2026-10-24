# GestiAula API

## Descripción

GestiAula API es una interfaz de programación de aplicaciones desarrollada como parte del sistema GestiAula, cuyo objetivo es facilitar el acceso a información académica mediante servicios REST.

El proyecto utiliza Java, Spring Boot y MariaDB para proporcionar servicios de consulta de información de alumnos.

## Objetivo

Diseñar una API que permita la comunicación entre los componentes del sistema y facilite la futura integración de módulos de gestión de grupos, asignaturas, asistencias, calificaciones y reportes académicos.

## Tecnologías utilizadas

- Java 21
- Spring Boot 3
- MariaDB
- Maven
- HTTP y JSON
- OpenAPI 3.0 para la documentación de los servicios

## Endpoints disponibles

| Método | Ruta | Descripción |
|---|---|---|
| GET | `/api/estado` | Consulta el estado de la API. |
| GET | `/api/alumnos` | Obtiene la lista de alumnos registrados. |
| GET | `/api/alumnos/{expediente}` | Busca un alumno por su expediente. |

## Ejemplos de solicitudes

Consultar todos los alumnos:

`GET /api/alumnos`

Consultar un alumno específico:

`GET /api/alumnos/1001`

El segundo ejemplo utiliza un expediente ilustrativo; debe sustituirse por uno existente en la base de datos.

## Respuestas HTTP

- `200 OK`: solicitud procesada correctamente.
- `404 Not Found`: no se encontró el alumno solicitado.
- `400 Bad Request`: solicitud con parámetros inválidos.
- `500 Internal Server Error`: error interno del servidor.

Los códigos aplicables dependen de cada endpoint y de su implementación.

## Documentación

La especificación de la API se encuentra en el archivo `openapi.yaml`. El documento de diseño incluye la justificación, los endpoints, sus parámetros, las respuestas HTTP y su relación con los requerimientos del sistema.

## Estado del proyecto

La consulta de alumnos se encuentra implementada y conectada a MariaDB. Las funcionalidades adicionales se incorporarán conforme avance el desarrollo del sistema.

## Ejecución local

Para iniciar el proyecto desde su código fuente, configura la conexión a MariaDB y ejecuta:

```bash
mvn spring-boot:run
```

Si la aplicación utiliza el puerto predeterminado, los servicios estarán disponibles localmente en `http://localhost:8080`.

**Nota:** Esta dirección es local y no representa una publicación pública de la API.
