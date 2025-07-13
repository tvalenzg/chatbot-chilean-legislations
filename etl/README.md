# ETL Chilean legislations - Chatbot Project

## Descripción

En este proyecto se busca desarrollar Pipeline de ETL para datos frecuentemente utilizados en la organización DSS.

## Estructura del Repositorio

El repositorio sigue una estructura organizada para facilitar la mantenibilidad y escalabilidad del proyecto:

```
├── src/          # Código fuente del proyecto
├── notebooks/    # Archivos experimentales en formato Jupyter Notebook (.ipynb)
├── data/        # Archivos locales utilizados para pruebas y procesamiento
├── env.example  # Plantilla para variables de entorno
├── pyproject.toml  # Configuración de dependencias y herramientas
├── ruff.toml    # Configuración Linter
├── README.md    # Documentación del proyecto
```

### Convenciones de Nombres

- Las carpetas y archivos que no sean paquetes (por ejemplo, dentro de `notebooks/`) deben usar guiones normales (`-`) para separar palabras en nombres compuestos y llevar una numeración doble al inicio. Ejemplo:
  - `01-example-name.ipynb`
  - `02-another-example.ipynb`
- Los archivos que pertenecen a paquetes de Python deben usar guiones bajos (`_`) en nombres compuestos. Ejemplo:
  - `mi_paquete/utils.py`
  - `procesamiento_datos/modelo.py`

## Ramas del Repositorio

El desarrollo del proyecto se gestiona a través de la rama principal 'main':

- **main**: Contiene el código estable y listo para producción.

Por otra parte, cada tarea y/o tarjeta nueva, debe ser resuelta en una rama nueva. Al finalizar la funcionalidad se deberá hacer PR a algún miembro del equipo. 
El proceso de mergeo debe contemplar el "squash and merge" junto a la eliminación de la rama.

## Gestión de Dependencias

Para la gestión de dependencias, el proyecto utiliza **uv**, una herramienta eficiente para la instalación y administración de paquetes en Python. Se recomienda seguir los siguientes comandos:

- Para sincronizar las dependencias con `pyproject.toml`:
  ```sh
  uv sync
  ```
- Para añadir una nueva dependencia:
  ```sh
  uv add nombre_de_dependencia
  ```

## Estilo de Código

Para garantizar un código limpio y mantenible, el proyecto utiliza **ruff**, una herramienta de análisis y formateo de código Python. Se recomienda seguir los siguientes pasos:

1. Verificar errores de clean code:
   ```sh
   uv run ruff check nombre_de_archivo
   ```
2. Formatear el código automáticamente al estilo de **ruff**:
   ```sh
   uv run ruff format nombre_de_archivo
   ```
3. Realizar un commit después de la limpieza de código.

## Variables de Entorno

El archivo `env.example` actúa como una plantilla para definir las variables de entorno necesarias para el correcto funcionamiento del sistema. Se debe crear un archivo `.env` basado en esta plantilla y completar las variables requeridas.