# API Onboarding Report – PotterAPI

## 1. Resumen de la API

**Nombre:** PotterAPI

**Base URL:** https://potterapi-fedeperin.vercel.app

**Arquitectura:** REST

**Formato de respuesta:** JSON

**Autenticación:** No requiere autenticación (API pública)

**Rate limit:** No especificado públicamente

PotterAPI es una API REST desarrollada con Express.js que proporciona información e imágenes del universo de Harry Potter, incluyendo libros, personajes, casas y hechizos.

La API soporta múltiples idiomas mediante un prefijo en la ruta: `/en`, `/es`, `/fr`, `/it`, `/pt`, `/uk`

---

## 2. Recursos principales

### /[lang]/books
Devuelve información sobre los libros.

Campos principales: `number`, `title`, `originalTitle`, `releaseDate`, `description`, `pages`, `cover`

### /[lang]/characters
Devuelve información sobre personajes.

Campos principales: `fullName`, `nickname`, `hogwartsHouse`, `interpretedBy`, `children`, `image`, `birthdate`, `index`

### /[lang]/houses
Devuelve información sobre las casas de Hogwarts.

### /[lang]/spells
Devuelve hechizos y su descripción.

---

## 3. Parámetros de consulta

| Parámetro | Descripción |
|-----------|-------------|
| `index` | Devuelve un elemento específico |
| `max` | Limita la cantidad de resultados |
| `page` | Permite paginación |
| `search` | Búsqueda por texto |

Ejemplos:
```bash
/en/characters?search=Weasley
/en/characters?max=5&page=2
```

---

## 4. Códigos de estado observados

### 200 OK
Se devuelve cuando la solicitud es exitosa.

### 404 Not Found
Se obtuvo en los siguientes casos:

- Endpoint inexistente: `/en/personajessss`
- Parámetro inválido: `/en/characters?max=-5`

Respuesta de ejemplo:
```json
{
  "error": "Parameter 'max' should be greater than 0"
}
```

Aunque conceptualmente este caso podría corresponder a un 400 Bad Request, la implementación de la API devuelve 404.

### 400 Bad Request
No fue posible reproducir un 400 explícito. La API tiende a ignorar ciertos parámetros inválidos en lugar de generar error.

### 401 Unauthorized
No aplica. La API no implementa autenticación.

### 403 Forbidden
No aplica. No existen recursos protegidos ni control de acceso.

---

## 5. Conclusión

PotterAPI es una API pública de solo lectura que permite demostrar principios REST, uso de parámetros de consulta, paginación, búsqueda y manejo básico de errores. Es adecuada para fines académicos y exploración de APIs REST.
