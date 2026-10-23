# Web de MineKOI

Web estática (HTML + CSS, sin dependencias) que explica el servidor y cómo instalar la instancia.
Se genera con `python tools/gen_sitio.py` desde la carpeta del proyecto; no la edites a mano.

## Publicada (2026-10-24)

- Repositorio: https://github.com/Chamorro2/minekoi (público). Esta carpeta `sitio/` es su copia local (`git remote origin`).
- Web: **https://chamorro2.github.io/minekoi/** (GitHub Pages, rama `main`, carpeta raíz).

Para actualizarla: regenera con `python tools/gen_sitio.py` (no borra `.git`), y desde `sitio/`:

    git add -A
    git commit -m "Actualiza la web"
    git push

## Publicarla en GitHub Pages (cómo se hizo)

1. En GitHub, crea un repositorio nuevo **público**, por ejemplo `minekoi`.
2. Sube **el contenido de esta carpeta `sitio/`** a la raíz del repositorio (`index.html` tiene que quedar arriba del todo).
   Desde la web de GitHub: *Add file → Upload files* y arrastra todo lo que hay dentro de `sitio/`, incluida la carpeta `img/` y `descargas/`.
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)` → **Save**.
4. En uno o dos minutos estará en `https://<tu-usuario>.github.io/minekoi/`.

## Al actualizar el modpack

Si cambia el modpack (por ejemplo, a `minekoi-1.7.0.mrpack`), cambia `MODPACK` en `tools/gen_sitio.py`, vuelve a generar la web y sube los archivos otra vez.

## Ten en cuenta

- La web es **pública** e incluye la dirección del servidor (`72.62.29.18`). El servidor ya es accesible para cualquier cuenta premium (no hay whitelist), así que no cambia la seguridad, pero sí hace que sea más fácil de encontrar.
- No usa logos de los clubes ni fotos de jugadores, e incluye un aviso de que es un proyecto de fans sin afiliación.
