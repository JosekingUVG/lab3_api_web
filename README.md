# Laboratorio 3 – Exploración de API REST

## Descripción

Este repositorio contiene el desarrollo del Laboratorio #3 del curso Sistemas y Tecnologías Web.

La API seleccionada fue **PotterAPI**, una API REST pública que proporciona información sobre el universo de Harry Potter.

---

## Estructura del repositorio
```
laboratorio-3-api/
│
├── API_ONBOARDING_REPORT.md
├── httpie-commands.md
├── README.md
│
└── postman/
    ├── potterApiEnvironment.json
    ├── Happy-Path.postman_collection.json
    └── Issues.postman_collection.json
```

---

## Contenido

### API_ONBOARDING_REPORT.md
Incluye resumen de la API, recursos principales, parámetros disponibles, análisis de códigos de estado y conclusiones técnicas.

### httpie-commands.md
Incluye configuración de variables de entorno y más de 10 comandos HTTPie cubriendo listado, búsqueda, paginación y manejo de errores.

### Carpeta postman/
Contiene el environment configurado, la colección Happy Path y la colección Issues.

---

## Notas

PotterAPI no requiere autenticación. Por lo tanto, no fue posible demostrar errores 401 o 403 debido a la ausencia de endpoints protegidos.

