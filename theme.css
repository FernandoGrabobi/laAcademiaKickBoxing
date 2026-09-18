# La Academia KickBoxing — Sitio web

## Estructura

```
index.html              → Página principal
peleadores/index.html   → Listado de peleadores con filtros y búsqueda
data/peleadores.json    → Datos de los peleadores (editar acá para agregar/quitar)
css/theme.css           → Colores de marca (variables CSS)
css/fonts.css           → Tipografías (Anton + Inter, con fallback si no hay internet)
css/tailwind.css        → CSS de Tailwind ya compilado (no se edita a mano)
js/data.js              → Carga los datos (hoy desde el JSON)
js/peleadores.js        → Lógica de filtros, búsqueda y renderizado de tarjetas
img/logo.png            → Logo de la academia
```

## Cómo agregar/editar un peleador

Abrí `data/peleadores.json` y agregá un objeto nuevo al arreglo, siguiendo el mismo formato que los existentes:

```json
{
  "id": 25,
  "nombre": "Juan",
  "apellido": "Perez",
  "foto": "",
  "filial": "Villa Mercedes",
  "modalidad": ["K1", "Low Kick"],
  "peso": 72,
  "edad": 22,
  "peleasGanadas": 5,
  "peleasPerdidas": 2
}
```

- `id` tiene que ser único.
- `modalidad` es un arreglo, puede tener una o varias modalidades ("K1", "Low Kick", "Full Contact").
- `foto` es opcional: si la dejás vacía se muestran las iniciales del peleador.

No hace falta tocar nada de código ni recompilar nada para esto — con guardar el JSON alcanza.

## Cómo editar los colores/logo

- Los colores de marca están centralizados en `css/theme.css` (variables `--color-primary`, `--color-accent`, etc.). Cambiar ahí impacta en todo el sitio.
- El logo es `img/logo.png` — para reemplazarlo, pisá ese archivo con el logo definitivo (mismo nombre).

## Si agregás clases nuevas de Tailwind

El CSS de Tailwind (`css/tailwind.css`) está compilado, no se genera en el momento como con el CDN. Si en algún momento agregás HTML con clases de Tailwind que no estén ya usadas en el sitio, hay que regenerar ese archivo:

```bash
npm install
npx tailwindcss -i ./css/tailwind-input.css -o ./css/tailwind.css --minify
```

(Si no existe `css/tailwind-input.css`, crealo con este contenido:)
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Próximos pasos posibles

- Migrar `data/peleadores.json` a Firebase/Firestore para poder cargar peleadores desde un panel en vez de editar el JSON a mano. El único archivo que habría que tocar es `js/data.js` (la función `cargarPeleadores`) — el resto del sitio no cambia.
- Agregar fotos reales de los peleadores.
- Agregar una página de detalle por peleador (historial de peleas, etc.) si hace falta más adelante.
