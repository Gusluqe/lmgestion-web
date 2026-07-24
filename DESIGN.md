# DESIGN.md — LMgestión

## Identity (heredada del sitio Canva y del mail de Luciana)
Tonos de marca declarados por la clienta: verde (gama lima y un verde más oscuro como el del logo), negro, blanco, gris clarito y gris oscuro. El sitio Canva ya comprometió fondo negro con tipografía blanca pesada y acento verde: se preserva esa identidad.

## Color (OKLCH, estrategia Committed: el verde carga la marca sobre superficie oscura)
- `--ink`:      oklch(17% 0.012 155)  — casi negro tintado verde (fondo principal)
- `--ink-2`:    oklch(21% 0.014 155)  — panel oscuro
- `--paper`:    oklch(97% 0.005 155)  — blanco cálido (secciones claras)
- `--gris`:     oklch(88% 0.006 155)  — gris clarito
- `--verde`:    oklch(58% 0.16 150)   — verde logo (marca)
- `--lima`:     oklch(85% 0.21 135)   — lima (acentos y highlights sobre oscuro)
- Texto sobre oscuro: oklch(93% 0.006 155); texto secundario oklch(72% 0.01 155)

## Typography
Familia única: **Archivo** (variable, Omnibus-Type, fundidora de Buenos Aires; coherente con marca argentina). Contraste por peso y ancho: display en Archivo Expanded 800/900, cuerpo en Archivo 400/500. Escala modular ≥1.25 con clamp(). Line-height +0.05 sobre fondo oscuro.

## Layout
Asimétrico, alineado a la izquierda, scroll largo con un concepto por pantalla. Servicios como lista numerada 01–04 (patrón heredado del Canva), no grilla de tarjetas idénticas. Fotografía real del negocio (assets/ bajados del sitio Canva) como ancla de cada sección.

## Motion
Reveals de entrada con stagger, ease-out expo, sin bounce. Respeta prefers-reduced-motion.

## Components
- Botón primario: fondo lima, texto casi negro, forma pill.
- Botón WhatsApp flotante (pedido explícito del cliente).
- Enlaces de contacto como lista tipográfica grande, no iconos en grilla.
