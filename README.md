# Estudios HYS · Diario de desarrollo

Blog de desarrollo de Estudios HYS, estudio indie de juegos móviles. Se publica gratis con GitHub Pages y Jekyll, tema [minima](https://github.com/jekyll/minima) (incluido en Pages, sin un workflow de Actions).

Cuando Pages esté activado, el sitio queda en [https://estudios-hys.github.io/blog/](https://estudios-hys.github.io/blog/).

Contacto público: [soporte@estudioshys.com](mailto:soporte@estudioshys.com). No publiques teléfono ni dirección postal.

## Añadir una entrada

Todas las entradas pasan por un pull request que aprueba solo [@Rsan2017](https://github.com/Rsan2017).

1. Crea `_posts/AAAA-MM-DD-titulo.md`. La fecha del nombre y la de `date` tienen que ser la misma. Ejemplo: `_posts/2026-10-24-arrancamos.md`.
2. Empieza el fichero así:

   ```markdown
   ---
   layout: post
   title: "Título de la entrada"
   date: AAAA-MM-DD
   ---

   Texto en español, con tono cercano.
   ```

3. Abre un pull request contra `main`. No se publica nada empujando directo a `main`.
4. Lo revisa, aprueba y fusiona solo @Rsan2017. `.github/CODEOWNERS` le asigna todos los ficheros (`* @Rsan2017`).

Para que GitHub impida fusionar sin esa aprobación: Settings > Rules > Rulesets (o la protección de ramas) sobre `main`, exigiendo pull request y revisión de code owners.

## Activar GitHub Pages

En el repositorio: **Settings > Pages > Deploy from a branch**. Rama `main`, carpeta `/` (root). Guarda.

Pages construye el sitio con Jekyll al fusionar en `main`. No hace falta añadir un workflow de Actions: el tema `minima` ya forma parte de GitHub Pages.

## Vista previa en local

Hace falta Ruby. Instala el tema que usa Pages y los dos plugins del `_config.yml`:

```bash
gem install jekyll minima:2.5.1 jekyll-feed jekyll-seo-tag
jekyll serve
```

Ábrelo en `http://127.0.0.1:4000/blog/`.
