# Projects

Repositorio central para guardar el código, la documentación y los archivos del proyecto, y consultar los avances desde distintos dispositivos.

## Ver y descargar los avances

1. Abre https://github.com/Branbr7/Projects e inicia sesión con una cuenta que tenga acceso.
2. Selecciona la rama `main` para ver la versión publicada.
3. Para descargar todo, selecciona **Code → Download ZIP**.
4. Para descargar un archivo, ábrelo y usa la opción de descarga de GitHub.

La descarga ZIP es una copia: no se actualiza automáticamente.

## Trabajar desde otra computadora

Con Git instalado, descarga el repositorio una sola vez:

```sh
git clone https://github.com/Branbr7/Projects.git
cd Projects
```

Antes de empezar a trabajar, guarda tus cambios pendientes y obtén los últimos avances:

```sh
git pull --ff-only origin main
```

Para publicar cambios, revisa los archivos y añade únicamente los que quieras compartir:

```sh
git status
git add <archivos>
git commit -m "Describe el avance"
git push origin main
```

Evita editar los mismos archivos simultáneamente en dos computadoras. No publiques contraseñas, claves de API ni datos privados.

## Archivos generados en las conversaciones

Los archivos creados en un entorno o adjuntos a una conversación no se suben automáticamente a GitHub. Para que estén disponibles desde todos los dispositivos, deben guardarse en este repositorio y publicarse con un commit y un push. El historial de commits permite consultar los avances publicados.

GitHub conserva los archivos publicados; no sincroniza automáticamente el historial de conversaciones ni los procesos de un entorno de desarrollo.
