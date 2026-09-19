/* =========================================================
   Página de listado de peleadores: filtros + búsqueda + render.
   Trabaja siempre sobre el arreglo que devuelve cargarPeleadores()
   (hoy viene de un JSON, mañana puede venir de Firestore sin
   tocar nada de acá).
   ========================================================= */

let TODOS = [];
const estado = {
  texto: '',
  filial: null,      // null = todas
  modalidad: null,    // null = todas
  pesoMax: 110,
  edadMax: 45,
};

const $grid = document.getElementById('grid');
const $sinResultados = document.getElementById('sin-resultados');
const $contador = document.getElementById('contador');
const $buscador = document.getElementById('buscador');
const $filtroFilial = document.getElementById('filtro-filial');
const $filtroModalidad = document.getElementById('filtro-modalidad');
const $filtroPeso = document.getElementById('filtro-peso');
const $filtroEdad = document.getElementById('filtro-edad');
const $pesoValor = document.getElementById('peso-valor');
const $edadValor = document.getElementById('edad-valor');
const $limpiar = document.getElementById('limpiar-filtros');

init();

async function init() {
  TODOS = await cargarPeleadores();

  construirChips($filtroFilial, unicos(TODOS.map(p => p.filial)), 'filial');
  construirChips($filtroModalidad, unicos(TODOS.flatMap(p => p.modalidad)), 'modalidad');

  const pesos = TODOS.map(p => p.peso);
  const edades = TODOS.map(p => p.edad);
  const pesoMax = Math.max(...pesos);
  const edadMax = Math.max(...edades);
  $filtroPeso.max = pesoMax;
  $filtroPeso.value = pesoMax;
  $filtroEdad.max = edadMax;
  $filtroEdad.value = edadMax;
  estado.pesoMax = pesoMax;
  estado.edadMax = edadMax;

  $buscador.addEventListener('input', e => {
    estado.texto = e.target.value.trim().toLowerCase();
    render();
  });

  $filtroPeso.addEventListener('input', e => {
    estado.pesoMax = Number(e.target.value);
    $pesoValor.textContent = estado.pesoMax >= pesoMax ? 'Todos' : `hasta ${estado.pesoMax}kg`;
    render();
  });

  $filtroEdad.addEventListener('input', e => {
    estado.edadMax = Number(e.target.value);
    $edadValor.textContent = estado.edadMax >= edadMax ? 'Todas' : `hasta ${estado.edadMax}`;
    render();
  });

  $limpiar.addEventListener('click', () => {
    estado.texto = '';
    estado.filial = null;
    estado.modalidad = null;
    estado.pesoMax = pesoMax;
    estado.edadMax = edadMax;
    $buscador.value = '';
    $filtroPeso.value = pesoMax;
    $filtroEdad.value = edadMax;
    $pesoValor.textContent = 'Todos';
    $edadValor.textContent = 'Todas';
    [...$filtroFilial.children, ...$filtroModalidad.children].forEach(c => c.classList.remove('active'));
    render();
  });

  render();
}

function unicos(arr) {
  return [...new Set(arr)].sort();
}

function construirChips(contenedor, valores, tipo) {
  valores.forEach(valor => {
    const chip = document.createElement('button');
    chip.type = 'button';
    chip.textContent = valor;
    chip.className = 'chip text-xs font-medium px-3 py-1.5 rounded-full';
    chip.addEventListener('click', () => {
      const yaActivo = estado[tipo] === valor;
      [...contenedor.children].forEach(c => c.classList.remove('active'));
      estado[tipo] = yaActivo ? null : valor;
      if (!yaActivo) chip.classList.add('active');
      render();
    });
    contenedor.appendChild(chip);
  });
}

function filtrar() {
  return TODOS.filter(p => {
    if (estado.texto) {
      const nombreCompleto = `${p.nombre} ${p.apellido}`.toLowerCase();
      if (!nombreCompleto.includes(estado.texto)) return false;
    }
    if (estado.filial && p.filial !== estado.filial) return false;
    if (estado.modalidad && !p.modalidad.includes(estado.modalidad)) return false;
    if (p.peso > estado.pesoMax) return false;
    if (p.edad > estado.edadMax) return false;
    return true;
  });
}

function render() {
  const resultados = filtrar();
  $contador.textContent = resultados.length;
  $grid.innerHTML = '';

  if (resultados.length === 0) {
    $sinResultados.classList.remove('hidden');
    return;
  }
  $sinResultados.classList.add('hidden');

  resultados.forEach(p => $grid.appendChild(tarjeta(p)));
}

function tarjeta(p) {
  const div = document.createElement('div');
  div.className = 'card rounded-xl p-5';

  const totalPeleas = p.peleasGanadas + p.peleasPerdidas;
  const efectividad = totalPeleas > 0 ? Math.round((p.peleasGanadas / totalPeleas) * 100) : 0;

  const iniciales = `${p.nombre[0] || ''}${p.apellido[0] || ''}`.toUpperCase();

  div.innerHTML = `
    <div class="flex items-center gap-4 mb-4">
      <div class="h-14 w-14 rounded-full flex items-center justify-center font-display text-lg flex-shrink-0"
           style="background: var(--color-bg-alt-2); color: var(--color-accent); border: 2px solid var(--color-border);">
        ${p.foto ? `<img src="${p.foto}" alt="${p.nombre}" class="h-full w-full object-cover rounded-full">` : iniciales}
      </div>
      <div class="min-w-0">
        <h3 class="font-bold text-base truncate">${p.nombre} ${p.apellido}</h3>
        <p class="text-xs" style="color: var(--color-text-dim);">${p.filial}</p>
      </div>
    </div>

    <div class="flex flex-wrap gap-1.5 mb-4">
      ${p.modalidad.map(m => `<span class="modalidad-tag text-[11px] font-semibold px-2 py-1 rounded">${m}</span>`).join('')}
    </div>

    <div class="grid grid-cols-2 gap-3 text-sm mb-4">
      <div><span style="color: var(--color-text-dim);">Peso:</span> <span class="font-semibold">${p.peso}kg</span></div>
      <div><span style="color: var(--color-text-dim);">Edad:</span> <span class="font-semibold">${p.edad} años</span></div>
    </div>

    <div class="flex items-center justify-between pt-3" style="border-top: 1px solid var(--color-border);">
      <div class="flex gap-4 text-sm">
        <span style="color: var(--color-success);" class="font-bold">${p.peleasGanadas}G</span>
        <span style="color: var(--color-danger);" class="font-bold">${p.peleasPerdidas}P</span>
      </div>
      <span class="text-xs font-semibold text-accent">${efectividad}% efectividad</span>
    </div>
  `;
  return div;
}
