<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Malla Interactiva - Geografía UACh</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f0f0f0;
      padding: 2rem;
    }
    h1 {
      text-align: center;
      color: #0d3b66;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 1rem;
    }
    .ramo {
      background: white;
      border: 2px solid #1c7ed6;
      padding: 1rem;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    .ramo:hover {
      background: #e3f2fd;
    }
    .modal {
      display: none;
      position: fixed;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      background: white;
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      z-index: 10;
    }
    .overlay {
      display: none;
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.4);
      z-index: 5;
    }
  </style>
</head>
<body>

<h1>Malla Interactiva - Geografía UACh</h1>

<div class="grid">
  <div class="ramo" onclick="mostrarModal('CAEV055')">CAEV055 - Introducción a la Geografía</div>
  <div class="ramo" onclick="mostrarModal('CITI057')">CITI057 - Geografía Física General</div>
  <div class="ramo" onclick="mostrarModal('MATM040')">MATM040 - Álgebra</div>
  <div class="ramo" onclick="mostrarModal('CIDI047')">CIDI047 - Lengua Materna</div>
  <div class="ramo" onclick="mostrarModal('CIDI054')">CIDI054 - Inglés I</div>
</div>

<!-- Ventana modal -->
<div class="overlay" id="overlay" onclick="cerrarModal()"></div>
<div class="modal" id="modal">
  <h2 id="tituloRamo"></h2>
  <p id="descripcionRamo"></p>
  <button onclick="cerrarModal()">Cerrar</button>
</
