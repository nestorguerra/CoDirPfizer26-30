# Informe IA 2026–2030 · Pfizer España

Escenario editorial interactivo (HTML autocontenido) sobre el impacto de la IA agéntica en Pfizer España, 2026–2030. Pieza de NCompany para el comité de dirección.

## Qué hay aquí

- `index.html` — la página completa. Un único archivo, sin dependencias externas: todo el CSS y el JavaScript van dentro. Funciona abriéndolo en cualquier navegador.
- `.nojekyll` — desactiva el procesado Jekyll de GitHub Pages (sirve el HTML tal cual).
- `robots.txt` — pide a los buscadores que no indexen la página (ver nota de visibilidad).
- `.gitignore` — ignora archivos de sistema (macOS / Windows / editores).

## Publicar en GitHub Pages

### Opción A — por la web (sin git, lo más rápido)

1. En GitHub, crea un repositorio nuevo (botón **New**). Ponle el nombre que quieras (ver nota de visibilidad sobre el nombre).
2. En el repo vacío, pulsa **uploading an existing file** y arrastra **el contenido de esta carpeta** (no la carpeta en sí): `index.html`, `.nojekyll`, `robots.txt`, `.gitignore`, `README.md`.
3. **Commit changes**.
4. Ve a **Settings → Pages**.
5. En **Source**, elige **Deploy from a branch**. En **Branch**, elige `main` y carpeta `/ (root)`. **Save**.
6. Espera 1–2 minutos. GitHub te dará la URL: `https://<tu-usuario>.github.io/<nombre-repo>/`.

### Opción B — por línea de comandos (git)

```bash
cd informe-ia-2026-2030
git init
git add .
git commit -m "Informe IA 2026-2030 Pfizer España"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/<nombre-repo>.git
git push -u origin main
```

Luego activa Pages en **Settings → Pages** igual que en los pasos 4–6 de la Opción A.

## Dominio propio (opcional)

Para servirlo desde un subdominio tuyo (p. ej. `ia.nestorguerra.com`):

1. Crea un archivo `CNAME` en la raíz con una sola línea: tu dominio (`ia.nestorguerra.com`).
2. En tu DNS, añade un registro CNAME que apunte a `<tu-usuario>.github.io`.
3. En **Settings → Pages → Custom domain**, escribe el dominio y guarda.

## Nota de visibilidad y confidencialidad

GitHub Pages publica la web en una **URL pública**. Si el repositorio es **público**, cualquiera con el enlace —y, sin el `robots.txt`, también los buscadores— puede acceder al contenido. Este documento menciona cartera y pipeline de Pfizer a título ilustrativo. Antes de publicar, decide:

- **Repo público + `robots.txt`** (incluido): accesible por enlace, pero no indexado por Google. Suficiente si solo vas a compartir la URL con el comité.
- **Repo privado + GitHub Pages**: requiere plan de pago (GitHub Pro / Team / Enterprise). La página sigue siendo accesible por URL salvo en Enterprise con *private pages*.
- **Nombre del repo**: la URL pública incluye el nombre del repo. Evita nombres que revelen el cliente si te preocupa la discreción.

Para un blindaje extra, puedes añadir esta línea dentro de `<head>` en `index.html`:

```html
<meta name="robots" content="noindex,nofollow">
```

---

© 2026 Néstor Guerra · NCompany. Todos los derechos reservados.
