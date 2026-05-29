# GG Desarrollos — Landing

Sitio estático en HTML + CSS plano. Sin frameworks, sin build, sin dependencias.

## Estructura

```
ggdesarrollos/
├── index.html
├── styles.css
├── assets/
│   ├── favicon.svg
│   └── images/
│       ├── subix.png            ← copiar tu imagen acá
│       ├── matexa.png           ← copiar tu imagen acá
│       └── espaciosverdes.png   ← copiar tu imagen acá
└── README.md
```

## Paso 1 — Copiar las imágenes del portfolio

Las tres imágenes que generaste con ChatGPT deben ir en `assets/images/` con estos nombres exactos:

- `subix.png`
- `matexa.png`
- `espaciosverdes.png`

(Si son `.jpg`, cambiá la extensión en el `index.html` en los `<img src="...">`).

## Paso 2 — Probar localmente

Abrí `index.html` directamente en el navegador. No hace falta servidor.

## Paso 3 — Subir a Vercel

1. Subí la carpeta entera a un repo de GitHub.
2. En Vercel: New Project → Import repo → Deploy.
3. Vercel detecta que es estático y lo deploya. No hace falta configurar nada.
4. Conectá el dominio `ggdesarrollos.com` desde Settings → Domains.

---

## Cómo customizar

### Cambiar el color de acento

En `styles.css`, arriba de todo, está la sección **TOKENS**. Buscá:

```css
--color-accent:       #471D6E;
--color-accent-hover: #5a2589;
```

Cambiás esos dos valores y se actualiza todo el sitio (botones, links, eyebrow, hover, favicon hay que editarlo aparte).

### Cambiar las tipografías

En la misma sección de tokens:

```css
--font-display: 'Fraunces', Georgia, serif;
--font-body:    'Geist', system-ui, -apple-system, sans-serif;
--font-mono:    'JetBrains Mono', ui-monospace, monospace;
```

Si cambiás de fuente, acordate de cambiar también el `<link>` de Google Fonts en `index.html` (línea ~22).

### Cambiar textos

Todos los textos están en `index.html`, fáciles de encontrar:

- Hero: dentro de `<section class="hero">`
- Tarjetas de proyectos: cada `<article class="card">`
- Sección "Sobre": dentro de `<section class="sobre">`
- CTA final: dentro de `<section class="contacto">`

### Cambiar el WhatsApp

Buscá `wa.me/5493571682836` en `index.html`. Aparece 2 veces (hero y CTA final).

---

## Próximos pasos sugeridos

- **Fase 2:** demos por rubro en subdominios (`nutricion.ggdesarrollos.com`, etc.)
- **Fase 3:** página interna por proyecto (`/proyectos/subix`) con caso de estudio (problema, solución, stack, capturas).
- Agregar `robots.txt` y `sitemap.xml` para SEO básico cuando lo necesites.