# Sonrisa Imperial — Landing page

Landing page para la clínica dental **Sonrisa Imperial**. Su **único objetivo es que el visitante agende una cita**. Tiene que verse minimalista pero profesional. No agregar secciones que distraigan de agendar.

## Archivos
- `index.html`: el sitio completo en un solo archivo (HTML + CSS + JS inline). No usa frameworks ni paso de build.

## Diseño (respetar siempre)
- Fondo blanco cálido: `#FAF8F5` (`--bg`)
- Verde salvia profundo (marca): `#2F4A3E` (`--brand`), hover `#3E6151` (`--brand-light`)
- Dorado suave (acento): `#C9A876` (`--gold`)
- Texto: `#1C1B19` (`--ink`), texto secundario `#55534E` (`--ink-soft`), líneas `#E8E4DD` (`--line`)
- Tipografías: **Fraunces** (serif, títulos) + **Inter** (sans, cuerpo), vía Google Fonts
- Ancho máximo del contenido: 640px. Mucho aire y pocos elementos.
- Ilustración de portada: SVG propio (silueta de diente en línea con acentos dorados). No usar fotos de stock con derechos poco claros.

## Estructura actual
1. Header con logo SVG + nombre
2. Hero con ilustración, titular "Tu sonrisa merece una cita hoy, no algún día." y un botón a `#agendar`
3. Tres razones: Confirmación inmediata · Horarios flexibles · Un solo lugar
4. Formulario de agendamiento (nombre, teléfono, correo, fecha, motivo)
5. Footer con dirección y teléfono (datos de ejemplo: Av. Providencia 1234, Santiago · +56 2 2345 6789)

## Pendientes conocidos
- **El formulario no envía datos a ningún lado.** Solo muestra una confirmación en pantalla. Falta conectarlo a algo real (correo, WhatsApp o una base de datos).
- La dirección, el teléfono y el texto "+12 años" son de ejemplo: hay que confirmarlos con la clínica.
- Dominio propio: por definir (p. ej. sonrisaimperial.cl).
- Panel de edición futuro: por ahora las ediciones se hacen pidiéndole los cambios a Claude, que commitea y pushea a `main` (auto-deploy). Más adelante se podría evaluar un panel `/admin` con una base de datos liviana (p. ej. Vercel KV) si se necesita.

## Repositorio
- GitHub: https://github.com/mintmurrayinteriordesign-create/sonrisa-imperial (rama `main`)
- Git y GitHub CLI (`gh`) están instalados localmente y autenticados como `mintmurrayinteriordesign-create`.

## Despliegue (Vercel)
- Producción: https://sonrisa-imperial-a-team-7bdf.vercel.app
- Equipo de Vercel: `a-team-7bdf` (teamId `team_hcJPJVl19sU1x6qeBkGhJdFL`), proyecto: `sonrisa-imperial`
- **Auto-deploy activo:** el repo de GitHub está conectado al proyecto (Settings → Git). Cada `git push` a `main` dispara un deploy automático a producción.
- Login a la cuenta de Vercel del equipo: usar "Continue with Email" con el correo de la clínica — la opción "Continue with GitHub" lleva a una cuenta distinta (personal, ligada a `mintmurrayinteriordesign-create`), no al equipo `a-team-7bdf`.
- El token del conector MCP de Vercel no tiene permiso de lectura sobre ese equipo (da 403 al listar o leer despliegues/proyectos). Para confirmar el estado de un deploy, revisar el dashboard de Vercel directamente.
