# Familias CSF

- `index.html`: sitio de las familias (asistencia y ranking, ingreso con el nombre del hijo/a).
- `entrenador.html`: panel del entrenador. Registra asistencia y puntos, carga alumnos y guarda solo en `datos.json`.
- `datos.json`: los datos. Los escribe el panel del entrenador.
- `entrenadores.json`: usuarios de los entrenadores (con el token cifrado).
- `icono.png`: ícono para la pantalla de inicio.

## Panel del entrenador

- Primera vez (sin entrenadores creados): el panel muestra "Primera configuración". Se pega el token de GitHub (fine-grained, solo este repositorio, Contents: Read and write) y se crea el administrador con usuario y contraseña.
- Después, en la pestaña **Equipo**, el administrador crea un usuario y contraseña por cada entrenador y le asigna sus grupos o clases.
- Cada entrenador solo ve y registra a los alumnos de sus grupos. Los alumnos se asignan a un grupo al cargarlos.
- `entrenadores.json` guarda el token cifrado con la contraseña de cada entrenador (PBKDF2 + AES-GCM). Usar contraseñas largas.

El ingreso de las familias es un filtro cómodo, no seguridad: el repositorio es público.
