# Sitio web LMgestión

Página web de LMgestión (Luciana Morales, Lic. en Administración), armada a partir del mail "INFORMACION PAGINA LMgestion" del 30/04/2026 y de su sitio Canva (lmgestion.my.canva.site).

## Archivos

- `index.html` — la página principal (todo el contenido: hero, perfil, servicios, beneficios, formulario, contacto).
- `admin.html` — panel de administración. **Clave: `lmgestion2026`**.
- `config.js` — datos editables del sitio (email de contacto y cupones de descuento).
- `assets/` — logo e imágenes (bajadas del sitio Canva y optimizadas a WebP).

## Cómo verla localmente

Abrir una terminal en esta carpeta y ejecutar `python -m http.server 8642`, después entrar a http://127.0.0.1:8642/

## Panel de administración (admin.html)

Permite editar sin tocar código:
- **Email de contacto** (adonde llegan las consultas del formulario). El WhatsApp queda fijo a pedido.

Los cambios guardados aplican al instante **en ese navegador**. Para que los vean todos los visitantes del sitio publicado: botón **"Descargar config.js"** y reemplazar el archivo `config.js` en el hosting.

## Formulario de consultas

La sección "Contame de tu negocio" pide nombre, WhatsApp, email y descripción. Se envía por email (FormSubmit) a la casilla configurada; si falla, ofrece mandar los mismos datos por WhatsApp.

**Importante (una sola vez):** el primer envío dispara un mail de activación de FormSubmit a la casilla de Luciana; hay que abrirlo y tocar "Activate" para que empiecen a llegar las consultas.

## Publicación

- **Sitio en vivo:** https://lmgestion.netlify.app
- **Panel admin en vivo:** https://lmgestion.netlify.app/admin.html
- **Repositorio:** https://github.com/Gusluqe/lmgestion-web
- **Administración de Netlify:** https://app.netlify.com/projects/lmgestion

Para publicar cambios (por ejemplo, un `config.js` nuevo descargado del admin): copiar el archivo a esta carpeta y ejecutar

```
npx netlify-cli deploy --prod --dir .
```

y para guardar el historial en GitHub:

```
git add -A && git commit -m "Actualización" && git push
```
