/* =========================================================
   Capa de datos.
   Hoy lee de un JSON estático (data/peleadores.json).
   El día que pasen a Firebase/Firestore, esta es la ÚNICA
   función que hay que reemplazar — el resto del código
   (filtros, render, etc.) sigue funcionando igual porque
   siempre trabaja con la lista de objetos que devuelve.
   ========================================================= */

// Resuelve la ruta a /data/peleadores.json sin importar desde qué
// página se cargue este script (index.html en la raíz o
// peleadores/index.html en la subcarpeta). Se calcula apenas se
// carga el script (document.currentScript solo es válido en ese
// momento, no dentro de funciones llamadas después).
const _RUTA_DATOS = (() => {
  const scriptEl = document.currentScript || [...document.scripts].find(s => s.src.includes('js/data.js'));
  const baseJs = new URL(scriptEl.src, window.location.href); // .../js/data.js
  return new URL('../data/peleadores.json', baseJs).href;
})();

async function cargarPeleadores() {
  const res = await fetch(_RUTA_DATOS);
  if (!res.ok) throw new Error('No se pudo cargar peleadores.json');
  return res.json();
}
