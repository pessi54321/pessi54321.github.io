<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ingeniería Civil</title>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f0f0f0;
      overflow: hidden;
    }

    .pagina {
      display: none;
      height: 100vh;
      width: 100vw;
      padding: 20px;
      overflow-y: auto;
      background-color: white;
      position: absolute;
      top: 0;
      left: 0;
    }

    .pagina.activa {
      display: block;
      animation: cambioHoja 0.5s ease-in-out;
    }

    @keyframes cambioHoja {
      from {
        opacity: 0;
        transform: translateX(100%);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    h1, h2 {
      color: #2c3e50;
      text-align: center;
    }

    .imagenes {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      justify-items: center;
      margin-top: 20px;
    }

    .imagenes img {
      width: 200px;
      height: 150px;
      object-fit: cover;
      background-color: #ccc;
    }

    .boton, .volver {
      text-align: center;
      margin: 20px;
    }

    .boton a, .volver a {
      display: inline-block;
      padding: 10px 20px;
      background-color: #007BFF;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }

    .seccion {
      margin-bottom: 30px;
    }

    ul {
      padding-left: 20px;
    }
  </style>
</head>
<body>

  <!-- Página 1: Galería -->
  <div id="pagina1" class="pagina activa">
    <h1>Imágenes de Ingeniería Civil</h1>
    <div class="imagenes">
      <img src="D:\Nueva carpeta\a.jpg"">
      <img src="D:\Nueva carpeta\b.jpg">
      <img src="D:\Nueva carpeta\a.jpg">
      <img src="D:\Nueva carpeta\b.jpg">
      <img src="D:\Nueva carpeta\a.jpg">
      <img src="D:\Nueva carpeta\b.jpg">
      <img src="D:\Nueva carpeta\a.jpg">
      <img src="D:\Nueva carpeta\b.jpg">
      <img src="D:\Nueva carpeta\a.jpg">
    </div>
    <div class="boton">
      <a href="#" onclick="cambiarPagina('pagina2')">Ir a Información de Ingeniería Civil</a>
    </div>
  </div>

  <!-- Página 2: Información -->
  <div id="pagina2" class="pagina">
    <h1>Información de Ingeniería Civil</h1>

    <div class="seccion">
      <h2>Universidad Autónoma del Estado de Morelos (UAEM)</h2>
      <p><strong>Ubicación:</strong> Cuernavaca, Morelos, México.</p>
      <p><strong>Duración de la carrera:</strong> Aproximadamente 9 semestres (4.5 años).</p>
      <p><strong>Becas:</strong></p>
      <ul>
        <li>Beca de manutención</li>
        <li>Beca de excelencia académica</li>
        <li>Beca de movilidad estudiantil</li>
        <li>Beca Jóvenes Escribiendo el Futuro</li>
      </ul>
      <p><strong>Ventajas:</strong></p>
      <ul>
        <li>Enfoque práctico con laboratorios bien equipados.</li>
        <li>Buena vinculación con empresas locales y del gobierno.</li>
        <li>Programas de servicio social y prácticas profesionales.</li>
      </ul>
      <p><strong>Desventajas:</strong></p>
      <ul>
        <li>Infraestructura limitada en comparación con universidades más grandes.</li>
        <li>Menor número de intercambios internacionales.</li>
      </ul>
    </div>

    <div class="seccion">
      <h2>Instituto Politécnico Nacional (IPN)</h2>
      <p><strong>Ubicación:</strong> Ciudad de México, en unidades como la ESIA.</p>
      <p><strong>Duración de la carrera:</strong> Aproximadamente 9 semestres (4.5 años).</p>
      <p><strong>Becas:</strong></p>
      <ul>
        <li>Beca institucional (manutención)</li>
        <li>Beca de excelencia</li>
        <li>Beca de movilidad nacional e internacional</li>
        <li>Beca de titulación</li>
        <li>Beca Jóvenes Escribiendo el Futuro</li>
      </ul>
      <p><strong>Ventajas:</strong></p>
      <ul>
        <li>Alta calidad académica reconocida a nivel nacional e internacional.</li>
        <li>Acceso a centros de investigación y tecnología de punta.</li>
        <li>Amplias oportunidades laborales gracias al prestigio del IPN.</li>
      </ul>
      <p><strong>Desventajas:</strong></p>
      <ul>
        <li>Alta competencia para ingresar.</li>
        <li>Grupos numerosos en clases introductorias.</li>
      </ul>
    </div>

    <div class="volver">
      <a href="#" onclick="cambiarPagina('pagina1')">Volver a las imágenes</a>
    </div>
  </div>

  <script>
    function cambiarPagina(id) {
      document.querySelectorAll('.pagina').forEach(p => p.classList.remove('activa'));
      document.getElementById(id).classList.add('activa');
    }
  </script>

</body>
</html>
