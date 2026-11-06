# KRATOS – Barber Shop

Plataforma web para consultar barberías, servicios y gestionar reservas de citas.

## Tecnologías
- HTML, CSS y JavaScript
- Supabase (PostgreSQL y autenticación)
- GitHub

## Estructura
- `index.html`: prototipo web original de KRATOS.
- `supabase/config.toml`: configuración básica del proyecto Supabase CLI.
- `supabase/migrations/20261106000100_create_kratos.sql`: estructura inicial de la base de datos.

## Importante: estado del proyecto
El `index.html` incluido es el prototipo original. Todavía utiliza `localStorage` para guardar usuarios, barberías y reservas; **esta copia aún no está conectada a Supabase**. La migración crea las tablas y políticas de seguridad, pero el siguiente paso de desarrollo será adaptar el JavaScript para usar Supabase Auth y estas tablas.

## Tablas creadas por la migración
- `profiles`: perfil asociado a una cuenta de Supabase Auth.
- `shops`: barberías.
- `barbers`: barberos de cada barbería.
- `services`: servicios ofrecidos.
- `bookings`: reservas.

## Cómo subirlo a GitHub
1. Descarga y extrae el ZIP.
2. Abre el repositorio `KRATOS` en GitHub.
3. Selecciona **Add file → Upload files**.
4. Arrastra el contenido de la carpeta extraída (no la carpeta ZIP).
5. Escribe el mensaje `Agregar estructura inicial de KRATOS`.
6. Pulsa **Commit changes**.

## Seguridad
Nunca subas contraseñas de base de datos, claves `service_role` o claves secretas al repositorio. La conexión del navegador debe usar únicamente la clave publicable de Supabase y políticas RLS.
