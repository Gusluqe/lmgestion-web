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
- **Cupones de descuento**: agregar, desactivar o borrar. Viene cargado `MIPRIMERGESTION` con 10% de descuento; se muestra como banner en el hero y se valida en el formulario.

Los cambios guardados aplican al instante **en ese navegador**. Para que los vean todos los visitantes del sitio publicado: botón **"Descargar config.js"** y reemplazar el archivo `config.js` en el hosting.

## Formulario de consultas

La sección "Contame de tu negocio" pide nombre, WhatsApp, email, descripción y cupón (opcional). Se envía por email (FormSubmit) a la casilla configurada; si falla, ofrece mandar los mismos datos por WhatsApp.

**Importante (una sola vez):** el primer envío dispara un mail de activación de FormSubmit a la casilla de Luciana; hay que abrirlo y tocar "Activate" para que empiecen a llegar las consultas.

## Publicar

Es un sitio estático: se puede subir tal cual a Netlify, Vercel, GitHub Pages o cualquier hosting. Subir la carpeta completa (index.html, admin.html, config.js y assets/).
