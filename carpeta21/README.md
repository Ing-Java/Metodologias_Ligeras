# Metodologías Ligeras - Refactorización USantaTecla-movies

Este repositorio contiene la evolución del código del ejercicio clásico **USantaTecla-movies** para la asignatura de Metodologías Ligeras (UPM), demostrando el proceso de refactorización paso a paso.

## Estructura del proyecto

- `carpeta21/`  
  Proyecto Java con las versiones sucesivas del ejercicio, cada una en su carpeta:
  - `v21`: Versión base/original.
  - `v22`: Refactorización del bucle en `Customer` usando `for-each`.
  - `v23`: Eliminada la dependencia de `Customer` con `Movie` delegando el acceso al título a `Rental`.
  - `v24`: Permite la inyección de la lista de alquileres en `Customer` para reducir el acoplamiento con `ArrayList`.

## Cómo se estructuran los refactorings

Cada carpeta `vXX` es una copia evolutiva de la anterior, aplicando un refactoring concreto, con sus propios tests.

### Detalle de refactorings

- **v22:**  
  Se sustituye el bucle `while` por un bucle `for-each` en `Customer.java` para mejorar la legibilidad.
- **v23:**  
  Se elimina el acceso directo de `Customer` a los métodos de `Movie`. Ahora `Customer` obtiene el título de la película a través de `Rental`.
- **v24:**  
  Se permite inyectar la lista de rentals a `Customer` por constructor, disminuyendo el acoplamiento a la implementación concreta (`ArrayList`).

## Cómo ejecutar los tests

Puedes ejecutar los tests de cada versión desde tu IDE o con Maven/Gradle, asegurando que cada refactoring mantiene la funcionalidad.

---

**Autor:** Javier  
**Asignatura:** Metodologías Ligeras - UPM
