
# Tutorias API

## Descripción

Proyecto de API REST para gestión de tutorías desarrollado con FastAPI siguiendo una arquitectura en capas (Domain-Driven Design).

## Estructura del Proyecto

```
drawio/                        # Diagramas realizados en drawio
│   ├── Cajas de Arquitectura.drawio
│   └── Sistema de tutorias - Cajas principales.drawio
tutorias/
├── app/
│   ├── __init__.py
│   ├── api/                    # Rutas y endpoints
│   │   ├── __init__.py
│   │   └── main.py
│   ├── application/            # Casos de uso y servicios
│   │   ├── __init__.py
│   │   └── services.py
│   ├── domain/                 # Lógica de negocio
│   │   ├── __init__.py
│   │   ├── models.py
│   │   └── errors.py
│   └── infraestructure/        # Acceso a datos
│       ├── __init__.py
│       └── repositories.py
├── tests/
│   ├── __pycache__/
│   └── test_reservas.py
├── .pytest_cache/
├── requirements.txt
README.md
Arquitectura - Evidencias guía 1.pdf # Capturas de pantalla con evidencias
```

## Requisitos

Instala las dependencias:

```bash
pip install -r requirements.txt
```

## Ejecución

### Iniciar servidor con Uvicorn

```bash
uvicorn app.api.main:app --reload
```

- `--reload`: Reinicia automáticamente en cambios de código
- Accede en `http://localhost:8000`

### Ejecutar tests con Pytest

```bash
pytest tests/
```

- `pytest -q`: Correr pruebas


## Visualizar Diagramas

Para ver los diagramas de arquitectura:

1. Accede a [draw.io](https://draw.io)
2. Selecciona **File > Open** y carga los archivos `.drawio` ubicados en la carpeta `drawio/`
3. Alternativamente, puedes usar la extensión de draw.io en tu editor si lo tienes instalado

Los diagramas principales son:
- **Cajas de Arquitectura.drawio**: Representa la estructura general del proyecto
- **Sistema de tutorias - Cajas principales.drawio**: Muestra los componentes principales del sistema
