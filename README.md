# Microservicio de Clientes - FastAPI

Microservicio para gestionar clientes y sus compras en un sistema de perfumería. Implementado con FastAPI y SQLAlchemy.

## Tecnologías

- Python 3.9+
- FastAPI
- SQLite (base de datos)
- SQLAlchemy (ORM)
- Alembic (migraciones)
- Pydantic (validación)

## Requisitos

- Python 3.9 o superior
- pip (gestor de paquetes de Python)

## Instalación y ejecución

1. **Crear y activar entorno virtual**

   ```bash
   # Crear entorno virtual
   python -m venv venv

   # Activar entorno virtual
   # En macOS/Linux:
   source venv/bin/activate
   # En Windows:
   # venv\Scripts\activate
   ```

2. **Instalar dependencias**

   ```bash
   pip install -r requirements.txt
   ```

3. **Ejecutar migraciones**

   ```bash
   alembic upgrade head
   ```

4. **Iniciar servidor**

   ```bash
   uvicorn app.main:app --reload --host 0.0.0.0 --port 8001
   ```

5. **Acceder a la API**
   - API: http://localhost:8001/
   - Documentación Swagger: http://localhost:8001/docs
   - Verificación de salud: http://localhost:8001/health

## Endpoints principales

- `GET /api/clientes` - Listar todos los clientes
- `POST /api/clientes` - Crear cliente
- `GET /api/clientes/{id}` - Obtener cliente por ID
- `PUT /api/clientes/{id}` - Actualizar cliente
- `DELETE /api/clientes/{id}` - Eliminar cliente
- `GET /api/clientes/activos` - Listar clientes activos
- `GET /api/compras` - Listar todas las compras
- `POST /api/compras` - Crear compra
- `POST /api/compras/{id}/completar` - Marcar compra como completada