# IS2-HOSTELERIA

Sistema de gestión de reservas y servicios para un hotel (proyecto de Ingeniería de Software).

Descripción
-----------
Proyecto web desarrollado con Django que permite gestionar reservas, servicios disponibles y el proceso de pago de reservas. El proyecto incluye una aplicación principal `myapp` donde se encuentran los modelos, vistas y plantillas.

Estado
------
Proyecto en desarrollo. Incluye una configuración básica con base de datos SQLite (`db.sqlite3`) y las migraciones iniciales en `myapp/migrations/`.

Stack tecnológico
-----------------
- Python 3.8+
- Django (versión usada en desarrollo local)
- SQLite (por defecto, archivo `db.sqlite3`)

Estructura principal
--------------------
Raíz del proyecto contiene:

- `manage.py` - script de administración de Django.
- `Hotel/` - configuración del proyecto Django (settings, urls, wsgi/asgi).
- `myapp/` - aplicación principal con modelos, vistas, templates y static.
- `db.sqlite3` - base de datos por defecto (SQLite).

Prerrequisitos
--------------
- Python 3.8 o superior instalado.
- (Recomendado) virtualenv/venv para aislar dependencias.

Instalación y ejecución local
-----------------------------
1. Crear y activar un entorno virtual (Windows PowerShell):

	```powershell
	python -m venv .venv
	.\.venv\Scripts\Activate.ps1
	```

2. Instalar dependencias:

	- Si tienes un `requirements.txt`:

	  ```powershell
	  pip install -r requirements.txt
	  ```

	- Si no existe, instala Django (ajusta la versión si es necesario):

	  ```powershell
	  pip install "django>=3.2,<5"
	  ```

3. Aplicar migraciones y crear usuario administrador:

	```powershell
	python manage.py migrate
	python manage.py createsuperuser
	```

4. Ejecutar el servidor de desarrollo:

	```powershell
	python manage.py runserver
	```

	Después de esto, abre http://127.0.0.1:8000/ en tu navegador.

Pruebas
-------
Ejecuta las pruebas automáticas (si existen) con:

```powershell
python manage.py test
```

Archivos estáticos (producción)
------------------------------
Para preparar archivos estáticos en despliegue (si aplica):

```powershell
python manage.py collectstatic
```

Buenas prácticas y recomendaciones
---------------------------------
- Añadir un `requirements.txt` con `pip freeze > requirements.txt` una vez fijas las dependencias.
- Añadir un `.gitignore` (por ejemplo excluir `.venv/`, `__pycache__/`, `db.sqlite3`, archivos IDE). Ejemplos: `/.venv`, `db.sqlite3`, `*.pyc`, `__pycache__/`, `.vscode/`.
- No subir credenciales ni claves al repositorio.

Comandos git (PowerShell) — subir proyecto a GitHub
-------------------------------------------------
Recomendación: crea primero el repositorio vacío en GitHub (sin README). Luego, desde la raíz del proyecto, puedes usar estos comandos.

1) Comandos básicos para un repo nuevo (sin remote):

```powershell
git init
git add .
git commit -m "chore: inicial - proyecto IS2-HOSTELERIA"
git branch -M main
# reemplaza <USER> y <REPO> por tu usuario y nombre del repo en GitHub
git remote add origin https://github.com/<USER>/<REPO>.git
git push -u origin main
```

2) Si ya existe un `origin` remoto configurado y sólo quieres subir cambios:

```powershell
git status
git add .
git commit -m "chore: actualizar proyecto y README"
git push origin main
```

3) Verificar remotos y ramas:

```powershell
git remote -v
git branch --show-current
```

Notas finales
-------------
Si quieres, puedo:

- Añadir un `.gitignore` recomendado y un `requirements.txt` base.
- Crear un pequeño script de ejecución o un archivo `README` en inglés si lo necesitas.

Contacto
--------
Proyecto creado como trabajo de la asignatura de Ingeniería de Software — incluye las migraciones en `myapp/migrations/`.

Gracias por usar el repositorio — dime si deseas que añada `.gitignore` y `requirements.txt` ahora.

