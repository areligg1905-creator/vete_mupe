# Nombre del proyecto

Descripción breve del proyecto (qué hace, framework si aplica, versión de PHP requerida).

## Estructura sugerida
- app/                 -> Código PHP
- public/              -> Punto de entrada (index.php, assets)
- vendor/              -> Dependencias (no subir)
- db/dump.sql          -> Volcado SQL exportado desde phpMyAdmin (opcional)
- .env                 -> Configuración local sensible (NO subir)
- README.md

## Archivos incluidos
- `.gitignore` — reglas para ignorar archivos sensibles/temporales.
- `README.md` — este archivo.

## Pasos rápidos para subir el proyecto a GitHub

1) Inicializar repositorio local y primer commit
```bash
git init
git add .
git commit -m "Initial commit: proyecto + estructura"
```

2) Crear repositorio en GitHub (opciones)
- Por la web: crear nuevo repo en https://github.com y seguir las instrucciones.
- Con la CLI de GitHub:
```bash
gh repo create NOMBRE-REPO --public --source=. --remote=origin --push
```

3) Conectar remoto y subir (si lo haces manual)
```bash
git remote add origin https://github.com/TU_USUARIO/NOMBRE-REPO.git
git branch -M main
git push -u origin main
```

## Importar la base de datos (.sql) en otro entorno

- Con phpMyAdmin:
  - Entra en phpMyAdmin → selecciona la base de datos → pestaña "Importar" → sube `db/dump.sql` o `db/dump.sql.gz`.

- Con MySQL desde la terminal:
```bash
mysql -u usuario -p nombre_basedatos < db/dump.sql
```

## Buenas prácticas y seguridad
- Nunca subas credenciales reales ni el archivo `.env`.
- Incluye un `.env.example` con las claves/variables sin valores reales para documentar la configuración.
- Si la BD contiene datos personales, anonimiza o revisa la normativa aplicable antes de subir.

## Ejemplo de .env.example
```ini
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_basedatos
DB_USERNAME=usuario
DB_PASSWORD=secreto
APP_ENV=local
APP_DEBUG=true
```

## Qué hice por ti y el siguiente paso
He generado un `.gitignore` con reglas comunes para proyectos PHP y un `README.md` inicial con instrucciones para subir tu proyecto y cómo importar el dump de la base de datos. Ahora puedes:
- Copiar estos archivos en la raíz de tu proyecto local.
- Ajustar el README (nombre, descripción, comandos específicos).
- Crear el repositorio en GitHub y hacer push.

Si quieres, puedo:
- Generar también un `./db/dump.sql` placeholder o un `/.env.example` listo para copiar.
- Prepararte los comandos adaptados a tu sistema (Windows/macOS/Linux) o guiarte paso a paso mientras lo subes. ¿Cuál prefieres ahora?