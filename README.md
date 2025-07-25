# Climaxx
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Climaxx | Aire y Mecánica</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f8f8f8; }
    header { background: #ffd700; color: #000; padding: 20px; text-align: center; }
    nav { background: #333; padding: 10px; text-align: center; }
    nav a { color: white; margin: 0 15px; text-decoration: none; }
    section { padding: 30px; }
    h2 { color: #333; }
    .form-group { margin-bottom: 15px; }
    label { display: block; margin-bottom: 5px; }
    input, textarea, select {
      width: 100%; padding: 8px; box-sizing: border-box;
    }
    button {
      background: #ffd700; border: none; padding: 10px 20px;
      font-size: 16px; cursor: pointer;
    }
    footer { background: #333; color: white; text-align: center; padding: 20px; }
  </style>
</head>
<body>

  <header>
    <img src="logo.png" alt="Logo Climaxx" style="height: 60px;" />
    <h1>Climaxx</h1>
    <p>Aire acondicionado, calefacción y más - San Rafael, Mendoza</p>
  </header>

  <nav>
    <a href="#inicio">Inicio</a>
    <a href="#nosotros">Nosotros</a>
    <a href="#servicios">Servicios</a>
    <a href="#turno">Turnos</a>
    <a href="#contacto">Contacto</a>
  </nav>

  <section id="inicio">
    <h2>Bienvenidos a Climaxx</h2>
    <p>Especialistas en climatización y mantenimiento automotor. ¡Más que un taller, somos confianza sobre ruedas!</p>
  </section>

  <section id="nosotros">
    <h2>Sobre Nosotros</h2>
    <p>Climaxx nace en San Rafael con una visión clara: brindar soluciones integrales para tu vehículo. Nos dedicamos a la climatización automotriz, pero además sumamos servicios de mecánica, lavadero, lubricentro y repuestos. Nuestro objetivo es ofrecer comodidad, confianza y eficiencia.</p>
  </section>

  <section id="servicios">
    <h2>Nuestros Servicios</h2>
    <ul>
      <li><strong>Climatización:</strong> Instalación, reparación y carga de aire acondicionado.</li>
      <li><strong>Calefacción:</strong> Diagnóstico y arreglo de sistemas de calefacción automotriz.</li>
      <li><strong>Mecánica general:</strong> Frenos, suspensión, motor, electricidad.</li>
      <li><strong>Lubricentro:</strong> Cambio de aceite, filtro y revisión general.</li>
      <li><strong>Lavadero:</strong> Limpieza completa, interior y exterior.</li>
      <li><strong>Repuestos:</strong> Venta de accesorios y repuestos seleccionados.</li>
    </ul>
  </section>

  <section id="turno">
    <h2>Agenda tu Turno</h2>
    <form id="turnoForm">
      <div class="form-group">
        <label for="nombre">Nombre y Apellido</label>
        <input type="text" id="nombre" required />
      </div>
      <div class="form-group">
        <label for="telefono">Teléfono</label>
        <input type="text" id="telefono" required />
      </div>
      <div class="form-group">
        <label for="vehiculo">Marca y Modelo del Vehículo</label>
        <input type="text" id="vehiculo" required />
      </div>
      <div class="form-group">
        <label for="patente">Patente</label>
        <input type="text" id="patente" required />
      </div>
      <div class="form-group">
        <label for="servicio">Servicio</label>
        <select id="servicio" required>
          <option value="Climatización">Climatización</option>
          <option value="Calefacción">Calefacción</option>
          <option value="Mecánica general">Mecánica general</option>
          <option value="Lubricentro">Lubricentro</option>
          <option value="Lavadero">Lavadero</option>
          <option value="Repuestos">Repuestos</option>
        </select>
      </div>
      <button type="submit">Enviar por WhatsApp</button>
    </form>
  </section>

  <section id="contacto">
    <h2>Contacto</h2>
    <p>📍 Av. Mitre 1570, San Rafael, Mendoza</p>
    <p>📲 <a href="https://wa.me/5492604309828" target="_blank">WhatsApp: 2604309828</a></p>
    <p>📸 <a href="https://instagram.com/climaxxsr" target="_blank">@climaxxsr en Instagram</a></p>
  </section>

  <footer>
    <p>&copy; 2025 Climaxx. Todos los derechos reservados.</p>
  </footer>

  <script>
    document.getElementById("turnoForm").addEventListener("submit", function(e) {
      e.preventDefault();
      const nombre = document.getElementById("nombre").value;
      const telefono = document.getElementById("telefono").value;
      const vehiculo = document.getElementById("vehiculo").value;
      const patente = document.getElementById("patente").value;
      const servicio = document.getElementById("servicio").value;

      const mensaje = `Hola, soy ${nombre}. Quiero sacar un turno para el servicio de *${servicio}*.\n\n📱 Teléfono: ${telefono}\n🚗 Vehículo: ${vehiculo}\n📄 Patente: ${patente}`;

      const url = `https://wa.me/5492604309828?text=${encodeURIComponent(mensaje)}`;
      window.open(url, "_blank");
    });
  </script>

</body>
</html>
