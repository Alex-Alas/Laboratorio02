# Laboratorio 02 - Arquitectura de Software

Este repositorio contiene los archivos del Laboratorio 02, incluyendo modelos en OCL (Object Constraint Language) y una implementación de referencia en Python con pruebas unitarias.

## Requisitos

*   **USE OCL (UML-based Specification Environment):** Para ejecutar y validar los modelos `.use` y scripts `.cmd`.
    *   [Descargar USE OCL](https://sourceforge.net/projects/useocl/)
*   **Python 3.x:** Para ejecutar la implementación lógica y las pruebas.

## Estructura del Proyecto

*   `ocl/`: Contiene los archivos de modelo (`.use`) y scripts de comandos (`.cmd`).
    *   `University.use` / `University.cmd`: Ejercicio introductorio.
    *   `Reservas.use` / `Reservas.cmd`: Pruebas iniciales del sistema de tutorías.
    *   `Tutorias.use`: Modelo completo con todas las restricciones, precondiciones y postcondiciones.
    *   `cars.use` / `cars.cmd`: Ejemplo de clase.
*   `python/`: Implementación en Python.
    *   `tutorias/`: Código fuente del dominio, servicios y repositorios.
    *   `tests/`: Pruebas unitarias (`test_reservas.py`).
*   `Tabla_de_Trazabilidad.md`: Documento que vincula los elementos OCL con el código Python.

## Ejecución

### 1. Modelos OCL (USE)

Para verificar los modelos:

1.  Abrir **USE OCL**.
2.  Cargar un modelo `.use` (File -> Open Specification... -> Seleccionar `ocl/Tutorias.use` u otro).
3.  Cargar un script de prueba `.cmd` (State -> Determine State -> Open Script... -> Seleccionar `ocl/Reservas.cmd` u otro).
    *   *Nota: Asegúrate de que el script sea compatible con el modelo cargado (e.g., `University.cmd` con `University.use`).*
4.  Observar el "Class Invariant Window" para ver si se cumplen las restricciones.

### 2. Pruebas en Python

Para ejecutar las pruebas unitarias y verificar la lógica de negocio:

1.  Navegar a la carpeta `python`:
    ```bash
    cd python
    ```
2.  Ejecutar las pruebas con `unittest`:
    ```bash
    python -m unittest tests/test_reservas.py
    ```

Si todo es correcto, verás una salida indicando `OK` y el número de pruebas ejecutadas.

## Trazabilidad

Puedes consultar el detalle de cómo cada restricción OCL se mapea a código Python en el archivo [Tabla_de_Trazabilidad.md](./Tabla_de_Trazabilidad.md).
