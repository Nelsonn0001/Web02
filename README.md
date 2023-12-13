<html>
<head>
    <style>
        /* Estilo CSS con un color morado claro */
        body {
            font-family: Arial, sans-serif;
            background-color: #f0e6ff;
            margin: 0;
        }

        h1 {
           color: white;
            font-size: 36px;
            text-align: center;
        }

        header {
            background-color: #a64dff;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px;
        }

        .logo {
            width: 100px;
            height: 100px;
        }

        .cart {
            width: 50px;
            height: 50px;
        }

        .banner {
            width: 100%;
            height: 300px;
            object-fit: cover;
        }

        .main {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            margin: 20px;
        }

        .sweater {
            width: 300px;
            height: 400px;
            border: 1px solid #a64dff;
            margin: 10px;
            position: relative;
        }

        .sweater img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        .sweater button {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 50px;
            border: none;
            background-color: #a64dff;
            color: white;
            font-size: 18px;
            cursor: pointer;
        }

        .customization {
            width: 600px;
            height: 400px;
            border: 1px solid #a64dff;
            margin: 10px;
            padding: 10px;
        }

        .customization h2 {
            color: #a64dff;
            text-align: center;
        }

        .customization label {
            display: block;
            margin: 10px;
        }

        .customization input, .customization select {
            display: block;
            margin: 10px;
        }

        .featured {
            width: 100%;
            height: 200px;
            background-color: #a64dff;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px;
        }

        .featured h3 {
            color: white;
            font-size: 24px;
        }

        .subscription {
            width: 100%;
            height: 100px;
            background-color: #f0e6ff;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px;
        }

        .subscription input {
            width: 300px;
            height: 40px;
            border: 1px solid #a64dff;
            padding: 10px;
        }

        .subscription button {
            width: 100px;
            height: 40px;
            border: none;
            background-color: #a64dff;
            color: white;
            font-size: 18px;
            cursor: pointer;
        }

        footer {
            background-color: #a64dff;
            color: white;
            font-size: 14px;
            text-align: center;
            padding: 10px;
        }

        footer a {
            color: white;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <header>
        <!-- Encabezado con el logo de la marca y el carrito de compras -->
        <img src="logo.png" alt="Logo de la marca" class="logo">
        <h1>Sudaderas Personalizadas</h1>
        <img src="cart.png" alt="Carrito de compras" class="cart">
    </header>
    <img src="banner.jpg" alt="Banner principal" class="banner">
    <div class="main">
        <!-- La sudadera y las herramientas de personalización -->
        <div class="sweater">
            <img src="sweater.jpg" alt="Sudadera">
            <button type="button" onclick="alert('Aquí iría el código para personalizar la sudadera')">Personalizar</button>
        </div>
        <div class="customization">
            <h2>Herramientas de personalización</h2>
            <form id="customization-form" onsubmit="alert('Aquí iría el código para enviar el formulario de personalización')">
                <label for="color">Color:</label>
                <select id="color" name="color">
                    <option value="blanco">Blanco</option>
                    <option value="negro">Negro</option>
                    <option value="rojo">Rojo</option>
                    <option value="azul">Azul</option>
                    <option value="verde">Verde</option>
                </select>
                <label for="size">Talla:</label>
                <select id="size" name="size">
                    <option value="s">S</option>
                    <option value="m">M</option>
                    <option value="l">L</option>
                    <option value="xl">XL</option>
                </select>
                <label for="text">Agregar texto a la imagen:</label>
                <input type="text" id="text" name="text" placeholder="Escribe aquí tu texto">
                <label for="image">Subir imágenes:</label>
                <input type="file" id="image" name="image" accept="image/*">
                <input type="submit" value="Guardar personalización">
            </form>
        </div>
    </div>
    <div class="featured">
        <!-- Producto destacado -->
        <h3>¡No te pierdas nuestra oferta especial! Sudadera con capucha y bolsillo por solo $19.99</h3>
    </div>
    <div class="subscription">
        <!-- Formulario de suscripción -->
        <form id="subscription-form" onsubmit="alert('Aquí iría el código para suscribirse al boletín')">
            <input type="email" id="email" name="email" placeholder="Ingresa tu correo electrónico" required>
            <button type="submit">Suscribirse</button>
        </form>
    </div>
    <footer>
        <!-- Pie de página con las políticas de la marca -->
        <p>© 2023 Sudaderas Personalizadas. Todos los derechos reservados.</p>
        <p><a href="politicas.html">Políticas de privacidad</a> | <a href="terminos.html">Términos y condiciones</a></p>
    </footer>
</body>
</html>
