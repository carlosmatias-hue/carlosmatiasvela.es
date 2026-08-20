# Web personal — Carlos Matías Vela

Página personal de una sola pantalla (CV + enlace a LinkedIn) lista para publicar en GitHub Pages con el dominio `carlosmatiasvela.es`.

## Contenido

- `index.html` — toda la página (HTML + CSS incluido, sin dependencias externas).
- `assets/carlos-photo.png` — foto de perfil.
- `assets/logos/` — logotipos de las entidades certificadoras (Scrum Alliance, SAFe, ICAgile, PMI, Kanban University, CertiProf, LeSS.works, unFIX, thePower) que aparecen en la franja "Certificado por" de la sección Formación.

## Cómo publicarla en GitHub Pages

1. En GitHub, crea un repositorio nuevo (público) — por ejemplo `carlosmatiasvela.es` o `web-personal`.
2. Sube estos dos archivos (`index.html` y la carpeta `assets/`) a la raíz del repositorio. Puedes arrastrarlos directamente en la web de GitHub ("Add file" → "Upload files") o con git:
   ```
   git init
   git add index.html assets
   git commit -m "Primera versión de la web personal"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
   git push -u origin main
   ```
3. En el repositorio, ve a **Settings → Pages**.
4. En "Build and deployment", elige "Deploy from a branch", rama `main`, carpeta `/root`, y guarda.
5. En la misma pantalla de Pages, en **Custom domain**, escribe `carlosmatiasvela.es` y guarda (esto crea un archivo `CNAME` en el repo).
6. En el panel de dinahosting, dentro de `carlosmatiasvela.es` → **Zonas DNS**, crea 4 registros tipo **A** apuntando a:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
7. Espera a que se propague el DNS (minutos a un par de horas) y vuelve a Settings → Pages para activar **Enforce HTTPS**.

## Personalizar después

- Cambia textos, experiencia o habilidades directamente en `index.html` (todo está comentado por secciones: Sobre mí, Experiencia, Formación, Habilidades, Testimonios, Contacto).
- Para actualizar la foto, sustituye `assets/carlos-photo.png` por otra imagen con el mismo nombre (idealmente cuadrada, mínimo 300x300px).
- Para añadir o quitar una certificación, edita la lista dentro de `<ul class="cert-list">`; si es de una entidad nueva, añade su logo en `assets/logos/` y una línea más en el `<div class="logo-strip">`.
