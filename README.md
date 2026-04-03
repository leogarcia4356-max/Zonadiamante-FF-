Zonadiamante FF: La zona oficial para tus diamantes en Venezuela. Recargas rápidas de Free Fire por ID, Pases de Batalla y Tarjetas Semanales/Mensuales. Pago Móvil seguro con entrega inmediata. ¡No te quedes sin tu saldo gamer!"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zonadiamante FF - Carga tus Diamantes</title>
    
    <meta name="description" content="Zonadiamante FF: Recarga diamantes de Free Fire por ID al instante en Venezuela.">
    <meta property="og:title" content="Zonadiamante FF 💎">

    <style>
        /* --- ESTILO ZONADIAMANTE (GAMER DARK BLUE) --- */
        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: #0b0e11; /* Fondo muy oscuro */
            color: white;
            display: flex;
            justify-content: center;
            padding: 15px;
            margin: 0;
        }

        .card {
            background: #1c1f26; /* Fondo secundario oscuro */
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            width: 100%;
            max-width: 400px;
            text-align: center;
            border: 1px solid #333;
        }

        h2 { color: #00d4ff; margin-bottom: 5px; text-transform: uppercase; letter-spacing: 1px; }
        p.subtitle { color: #aaa; font-size: 13px; margin-bottom: 20px; }

        /* --- TÍTULOS DE SECCIÓN (Amarillo Neón) --- */
        .seccion-titulo {
            color: #ffba08;
            font-size: 14px;
            font-weight: bold;
            text-align: left;
            margin: 15px 0 10px 0;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* --- CUADRÍCULA DE PAQUETES --- */
        .grid-paquetes {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 10px;
        }

        .paquete-item {
            border: 2px solid #333;
            border-radius: 12px;
            padding: 15px;
            cursor: pointer;
            transition: 0.3s;
            background: #252932;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .paquete-item img { width: 45px; margin-bottom: 8px; }
        .paquete-item .cantidad { font-weight: bold; font-size: 16px; color: #fff; }
        .paquete-item .precio { font-size: 12px; color: #00d4ff; margin-top: 3px; }

        .paquete-item .tarjeta-img { width: 60px; height: 35px; object-fit: cover; border-radius: 5px; }

        .seleccionada {
            border-color: #00d4ff !important;
            background-color: #1a2a33;
            transform: translateY(-3px);
        }

        /* --- FORMULARIO E INPUTS --- */
        input {
            width: 100%;
            padding: 12px;
            margin: 8px 0;
            border: 1px solid #444;
            background: #0b0e11;
            color: white;
            border-radius: 10px;
            box-sizing: border-box;
            font-size: 16px;
        }

        /* --- MÉTODOS DE PAGO --- */
        .metodo-item {
            display: flex;
            align-items: center;
            padding: 12px;
            border: 1px solid #333;
            border-radius: 10px;
            margin-bottom: 8px;
            text-align: left;
            background: #252932;
            cursor: pointer;
        }

        .metodo-item img { width: 30px; margin-right: 12px; }
        .metodo-item h4 { margin: 0; font-size: 14px; color: #fff; }
        .pago-activo { border-color: #28a745; background-color: #1e2d24; }

        #datosBancarios {
            display: none;
            background: #00d4ff10;
            border: 1px solid #00d4ff;
            border-radius: 12px;
            padding: 15px;
            margin-top: 10px;
            text-align: left;
            font-size: 13px;
        }

        /* --- RESUMEN DE ORDEN --- */
        .resumen {
            background: #15181d;
            padding: 15px;
            border-radius: 12px;
            margin: 20px 0;
            border: 1px dashed #444;
        }
        .fila { display: flex; justify-content: space-between; font-size: 13px; margin: 4px 0; }
        .total { border-top: 1px solid #333; padding-top: 8px; font-weight: bold; color: #00d4ff; font-size: 16px; }

        /* --- BOTÓN PRINCIPAL --- */
        .btn-recargar {
            background: linear-gradient(45deg, #00d4ff, #0056b3);
            color: white;
            border: none;
            padding: 15px;
            width: 100%;
            border-radius: 12px;
            font-size: 17px;
            font-weight: bold;
            cursor: pointer;
        }

        /* --- MODAL DE CONFIRMACIÓN --- */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.85);
            justify-content: center; align-items: center;
            z-index: 1000; padding: 20px;
        }
        .modal-content { background: #1c1f26; padding: 25px; border-radius: 20px; width: 100%; max-width: 340px; border: 1px solid #444; }
    </style>
</head>
<body>

<div class="card">
    <h2>ZONADIAMANTE FF 💎</h2>
    <p class="subtitle">Recargas Rápidas por ID al mejor precio</p>

    <input type="number" id="playerID" placeholder="ID del Jugador (Ej: 12345678)">

    <div class="seccion-titulo">💎 Cargar Diamantes</div>
    <div class="grid-paquetes">
        <div class="paquete-item" onclick="seleccionarPaquete(this, '110 Diamantes', '660.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">110 💎</span>
            <span class="precio">660.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '220 Diamantes', '1.300.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">220 💎</span>
            <span class="precio">1.300.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '341 Diamantes', '1.995.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">341 💎</span>
            <span class="precio">1.995.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '572 Diamantes', '2.999.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">572 💎</span>
            <span class="precio">2.999.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '1.166 Diamantes', '5.550.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">1.166 💎</span>
            <span class="precio">5.550.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '1.738 Diamantes', '8.549.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">1.738 💎</span>
            <span class="precio">8.549.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '2.398 Diamantes', '11.300.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">2.398 💎</span>
            <span class="precio">11.300.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, '6.160 Diamantes', '28.800.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3039/3039433.png">
            <span class="cantidad">6.160 💎</span>
            <span class="precio">28.800.00 Bs</span>
        </div>
    </div>

    <div class="seccion-titulo">💳 Pases y Tarjetas</div>
    <div class="grid-paquetes">
        <div class="paquete-item" onclick="seleccionarPaquete(this, 'Pase B', '2.758.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" class="tarjeta-img">
            <span class="cantidad">Pase B</span>
            <span class="precio">2.758.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, 'Semanal Básica', '461.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/5969/5969046.png" class="tarjeta-img">
            <span class="cantidad">S. Básica</span>
            <span class="precio">461.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, 'Tarjeta Semanal', '1.797.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/2163/2163231.png" class="tarjeta-img">
            <span class="cantidad">Tarjeta S.</span>
            <span class="precio">1.797.00 Bs</span>
        </div>
        <div class="paquete-item" onclick="seleccionarPaquete(this, 'Tarjeta Mensual', '8.303.00')">
            <img src="https://cdn-icons-png.flaticon.com/512/3345/3345330.png" class="tarjeta-img">
            <span class="cantidad">Tarjeta M.</span>
            <span class="precio">8.303.00 Bs</span>
        </div>
    </div>

    <div class="seccion-titulo">💰 Método de Pago</div>
    <div class="metodo-item" onclick="mostrarDatosPago(this, 'Pago Móvil')">
        <img src="https://cdn-icons-png.flaticon.com/512/1019/1019050.png">
        <div class="metodo-info"><h4>Pago Móvil</h4></div>
    </div>

    <div id="datosBancarios">
        <p style="margin: 0 0 5px; color: #00d4ff; font-weight: bold;">💳 Datos de Pago Móvil:</p>
        <strong>Banco:</strong> 0102 Bco Venezuela<br>
        <strong>Cédula:</strong> V-21.122.975<br>
        <strong>Teléfono:</strong> 0416-1893853
    </div>

    <div class="resumen">
        <div class="fila"><span>ID Jugador:</span> <span id="res-id">-</span></div>
        <div class="fila"><span>Producto:</span> <span id="res-paquete">-</span></div>
        <div class="fila total"><span>Total a pagar:</span> <span id="res-total">0.00 Bs</span></div>
    </div>

    <button class="btn-recargar" onclick="abrirModal()">RECARGAR AHORA</button>
</div>

<div id="miModal" class="modal">
    <div class="modal-content">
        <h3 style="color:#00d4ff">Finalizar Pedido</h3>
        <p style="font-size: 12px; color: #aaa;">Ingresa los 4 últimos dígitos de la referencia de tu pago móvil.</p>
        <input type="text" id="refPago" placeholder="Ej: 9876">
        
        <button style="background:#28a745; color:white; border:none; width:100%; padding:15px; border-radius:10px; font-weight:bold; font-size:16px;" onclick="enviar()">
            REPORTAR PAGO WHATSAPP
        </button>
        <p onclick="cerrarModal()" style="font-size:12px; color:#ff4444; margin-top:20px; cursor:pointer;">Cancelar</p>
    </div>
</div>

<script>
    let paqueteG = ""; let precioG = "0.00"; let pagoG = "";

    function seleccionarPaquete(el, nombre, precio) {
        document.querySelectorAll('.paquete-item').forEach(i => i.classList.remove('seleccionada'));
        el.classList.add('seleccionada');
        paqueteG = nombre;
        precioG = precio;
        document.getElementById('res-paquete').innerText = nombre;
        document.getElementById('res-total').innerText = precio + " Bs";
    }

    function mostrarDatosPago(el, nombre) {
        document.querySelectorAll('.metodo-item').forEach(i => i.classList.remove('pago-activo'));
        el.classList.add('pago-activo');
        pagoG = nombre;
        document.getElementById('datosBancarios').style.display = 'block';
    }

    document.getElementById('playerID').addEventListener('input', function() {
        document.getElementById('res-id').innerText = this.value || "-";
    });

    function abrirModal() {
        const id = document.getElementById('playerID').value;
        if(!paqueteG || !id || !pagoG) {
            alert("⚠️ Selecciona el ID, el paquete y haz el pago móvil."); return;
        }
        document.getElementById('miModal').style.display = 'flex';
    }

    function cerrarModal() { document.getElementById('miModal').style.display = 'none'; }

    function enviar() {
        const miNumero = "584161893853"; // TU NÚMERO DE PAGO MÓVIL
        const idJuego = document.getElementById('playerID').value;
        const ref = document.getElementById('refPago').value;

        if(!ref) { alert("Ingresa la referencia."); return; }

        const msg = `*💎 PEDIDO ZONADIAMANTE FF 💎*%0A` +
                    `----------------------------%0A` +
                    `🆔 *ID Jugador:* ${idJuego}%0A` +
                    `📦 *Producto:* ${paqueteG}%0A` +
                    `💰 *Monto:* ${precioG} Bs%0A` +
                    `🔢 *Ref:* ${ref}%0A` +
                    `----------------------------%0A` +
                    `_Adjuntando capture..._`;

        window.open(`https://wa.me/${miNumero}?text=${msg}`, '_blank');
    }
</script>

</body>
</html>

