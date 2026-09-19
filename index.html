<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Peleadores · La Academia KickBoxing</title>
<link rel="icon" href="../img/logo.png" type="image/png">
<link rel="stylesheet" href="../css/tailwind.css">
<link rel="stylesheet" href="../css/theme.css">
<link rel="stylesheet" href="../css/fonts.css">
<style>
  body { font-family: var(--font-body); background: var(--color-bg); color: var(--color-text); }
  .font-display { font-family: var(--font-display); letter-spacing: 0.02em; font-weight: 900; }
  .bg-brand { background-color: var(--color-primary); }
  .text-brand { color: var(--color-primary); }
  .bg-accent { background-color: var(--color-accent); }
  .text-accent { color: var(--color-accent); }
  .border-brand { border-color: var(--color-primary); }

  .chip {
    cursor: pointer; user-select: none;
    border: 1px solid var(--color-border);
    background: var(--color-bg-alt);
    color: var(--color-text-muted);
    transition: all .15s ease;
  }
  .chip.active {
    background: var(--color-primary);
    border-color: var(--color-primary);
    color: white;
    font-weight: 600;
  }
  .chip:hover:not(.active) { border-color: var(--color-primary); color: var(--color-text); }

  input[type="text"], select {
    background: var(--color-bg-alt-2);
    border: 1px solid var(--color-border);
    color: var(--color-text);
  }
  input[type="text"]:focus, select:focus {
    outline: none; border-color: var(--color-accent);
  }
  input[type="range"] { accent-color: var(--color-primary); }

  .card {
    background: var(--color-bg-alt);
    border: 1px solid var(--color-border);
    transition: transform .15s ease, border-color .15s ease;
  }
  .card:hover { transform: translateY(-3px); border-color: var(--color-primary); }

  .modalidad-tag {
    background: var(--color-bg-alt-2);
    color: var(--color-accent-light, var(--color-accent));
    border: 1px solid var(--color-border);
  }
</style>
</head>
<body class="min-h-screen">

  <!-- NAV -->
  <header class="sticky top-0 z-50 border-b" style="background: rgba(10,10,10,0.92); border-color: var(--color-border); backdrop-filter: blur(6px);">
    <div class="max-w-6xl mx-auto px-5 py-3 flex items-center justify-between">
      <a href="../index.html" class="flex items-center gap-3">
        <img src="../img/logo.png" alt="La Academia KickBoxing" class="h-11 w-11 object-contain rounded-md">
        <span class="font-display text-lg tracking-wide hidden sm:block">LA ACADEMIA <span class="text-brand">KICK BOXING</span></span>
      </a>
      <nav class="flex items-center gap-6 text-sm font-semibold">
        <a href="../index.html" class="hover:text-brand transition-colors">Inicio</a>
        <a href="index.html" class="text-brand">Peleadores</a>
      </nav>
    </div>
  </header>

  <!-- TITULO -->
  <section class="max-w-6xl mx-auto px-5 pt-10 pb-6">
    <h1 class="font-display text-4xl mb-2">PELEADORES</h1>
    <p style="color: var(--color-text-muted);">Buscá por nombre, filial, modalidad, peso o edad.</p>
  </section>

  <!-- FILTROS -->
  <section class="max-w-6xl mx-auto px-5 pb-6">
    <div class="rounded-xl p-5 space-y-5" style="background: var(--color-bg-alt); border: 1px solid var(--color-border);">

      <!-- buscador -->
      <div>
        <input id="buscador" type="text" placeholder="Buscar por nombre o apellido..."
          class="w-full rounded-md px-4 py-2.5 text-sm">
      </div>

      <div class="grid sm:grid-cols-2 gap-5">
        <!-- filial -->
        <div>
          <label class="block text-xs font-bold uppercase tracking-wide mb-2" style="color: var(--color-text-dim);">Filial</label>
          <div id="filtro-filial" class="flex flex-wrap gap-2"></div>
        </div>

        <!-- modalidad -->
        <div>
          <label class="block text-xs font-bold uppercase tracking-wide mb-2" style="color: var(--color-text-dim);">Modalidad</label>
          <div id="filtro-modalidad" class="flex flex-wrap gap-2"></div>
        </div>
      </div>

      <div class="grid sm:grid-cols-2 gap-5">
        <!-- peso -->
        <div>
          <label class="block text-xs font-bold uppercase tracking-wide mb-2" style="color: var(--color-text-dim);">
            Peso: <span id="peso-valor">Todos</span>
          </label>
          <div class="flex items-center gap-3">
            <span class="text-xs" style="color: var(--color-text-dim);">40kg</span>
            <input id="filtro-peso" type="range" min="40" max="110" value="110" class="w-full">
            <span class="text-xs" style="color: var(--color-text-dim);">110kg</span>
          </div>
        </div>

        <!-- edad -->
        <div>
          <label class="block text-xs font-bold uppercase tracking-wide mb-2" style="color: var(--color-text-dim);">
            Edad: <span id="edad-valor">Todas</span>
          </label>
          <div class="flex items-center gap-3">
            <span class="text-xs" style="color: var(--color-text-dim);">14</span>
            <input id="filtro-edad" type="range" min="14" max="45" value="45" class="w-full">
            <span class="text-xs" style="color: var(--color-text-dim);">45</span>
          </div>
        </div>
      </div>

      <div class="flex items-center justify-between pt-1">
        <p class="text-xs" style="color: var(--color-text-dim);"><span id="contador">0</span> peleadores encontrados</p>
        <button id="limpiar-filtros" class="text-xs font-semibold text-accent hover:underline">Limpiar filtros</button>
      </div>
    </div>
  </section>

  <!-- GRID -->
  <section class="max-w-6xl mx-auto px-5 pb-20">
    <div id="grid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5"></div>
    <p id="sin-resultados" class="hidden text-center py-16" style="color: var(--color-text-muted);">
      No se encontraron peleadores con esos filtros.
    </p>
  </section>

  <script src="../js/data.js"></script>
  <script src="../js/peleadores.js"></script>
</body>
</html>
