<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tienda de sudaderas personalizadas</title>
  <!-- Aquí puedes añadir el código CSS para dar estilo a la página -->
  <style>
    /* Estilos generales */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      font-size: 16px;
      color: #333;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    h1, h2, h3 {
      font-weight: bold;
    }

    h1 {
      font-size: 3rem;
    }

    h2 {
      font-size: 2rem;
    }

    h3 {
      font-size: 1.5rem;
    }

    img {
      max-width: 100%;
      height: auto;
    }

    button {
      cursor: pointer;
    }

    /* Estilos del encabezado */
    header {
      background-color: #000;
      height: 80px;
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 20px;
    }

    .logo {
      width: 200px;
    }

    .menu {
      display: flex;
      list-style: none;
    }

    .menu li {
      margin: 0 10px;
    }

    .menu a {
      color: #fff;
      font-size: 1.2rem;
      padding: 10px;
    }

    .menu a:hover {
      color: #f00;
    }

    .carrito {
      position: relative;
    }

    .carrito img {
      width: 40px;
    }

    .cantidad {
      position: absolute;
      top: 0;
      right: 0;
      background-color: #f00;
      color: #fff;
      font-size: 0.8rem;
      padding: 2px 5px;
      border-radius: 50%;
    }

    .boton-cuenta {
      border: 2px solid #fff;
      background-color: transparent;
      color: #fff;
      font-size: 1.2rem;
      padding: 10px;
    }

    .boton-cuenta:hover {
      background-color: #f00;
      color: #fff;
    }

    .menu-cuenta {
      position: absolute;
      top: 80px;
      right: 20px;
      background-color: #fff;
      border: 2px solid #000;
      box-shadow: 5px 5px 10px rgba(0,0,0,0.5);
      display: none;
      list-style: none;
    }

    .menu-cuenta li {
      margin: 10px;
    }

    .menu-cuenta a {
      color: #000;
      font-size: 1.2rem;
    }

    .menu-cuenta a:hover {
      color: #f00;
    }

    /* Estilos del banner principal */
    .banner {
      height: 80vh;
      background-image: url("sudadera-banner.jpg");
      background-size: cover;
      background-position: center;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .texto-banner {
      color: #fff;
      text-align: center;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .boton-banner {
      display: inline-block;
      background-color: #f00;
      border: 2px solid #fff;
      color: #fff;
      font-size: 1.5rem;
      padding: 15px 30px;
      margin-top: 20px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .boton-banner:hover {
      background-color: #fff;
      color: #f00;
    }

    /* Estilos de las categorías destacadas */
    .categorias {
      background-color: #eee;
      padding: 40px 20px;
    }

    .contenedor-categorias {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-gap: 20px;
    }

    .categoria {
      border: 2px solid #000;
      padding: 10px;
      position: relative;
    }

    .categoria h3 {
      color: #000;
      font-size: 1.2rem;
      text-align: center;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
      position: absolute;
      bottom: 10px;
      left: 10px;
      right: 10px;
    }

    .boton-categoria {
      display: inline-block;
      background-color: #fff;
      border: 2px solid #000;
      color: #000;
      font-size: 1rem;
      padding: 10px 20px;
      position: absolute;
      top: 10px;
      right: 10px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .boton-categoria:hover {
      background-color: #f00;
      color: #fff;
    }

    /* Estilos de la funcionalidad de personalización */
    .personalizacion {
      background-color: #fff;
      padding: 40px 20px;
    }

    .contenedor-personalizacion {
      display: grid;
      grid-template-columns: 1fr 2fr;
      grid-gap: 20px;
    }

    .herramienta-personalizacion {
      border: 2px solid #000;
      padding: 20px;
    }

    .color-personalizacion,
    .texto-personalizacion,
    .grafico-personalizacion,
    .imagen-personalizacion {
      margin: 10px 0;
    }

    .color-personalizacion label,
    .texto-personalizacion label,
    .grafico-personalizacion label,
    .imagen-personalizacion label {
      display: block;
      color: #000;
      font-size: 1.2rem;
    }

    .color-personalizacion select,
    .grafico-personalizacion select {
      display: block;
      width: 100%;
      border: 2px solid #000;
      padding: 10px;
    }

    .texto-personalizacion input,
    .imagen-personalizacion input {
      display: block;
      width: 100%;
      border: 2px solid #000;
      padding: 10px;
    }

    .vista-previa-personalizacion {
      border: 2px solid #000;
      padding: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .boton-personalizacion {
      text-align: center;
      margin-top: 20px;
    }

    #añadir {
      background-color: #f00;
      border: 2px solid #fff;
      color: #fff;
      font-size: 1.5rem;
      padding: 15px 30px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    #añadir:hover {
      background-color: #fff;
      color: #f00;
    }

    /* Estilos de los productos destacados */
    .productos {
      background-color: #eee;
      padding: 40px 20px;
    }

    .contenedor-productos {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-gap: 20px;
    }

    .producto {
      border: 2px solid #000;
      padding: 10px;
      position: relative;
    }

    .producto h3 {
      color: #000;
      font-size: 1.2rem;
      text-align: center;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
      position: absolute;
      bottom: 10px;
      left: 10px;
      right: 10px;
    }

    .producto p {
      color: #000;
      font-size: 1.2rem;
      text-align: center;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
      position: absolute;      position: absolute;
      top: 10px;
      right: 10px;
    }

    .boton-producto {
      display: inline-block;
      background-color: #fff;
      border: 2px solid #000;
      color: #000;
      font-size: 1rem;
      padding: 10px 20px;
      position: absolute;
      top: 10px;
      left: 10px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .boton-producto:hover {
      background-color: #f00;
      color: #fff;
    }

    /* Estilos de los testimonios o reseñas */
    .testimonios {
      background-color: #fff;
      padding: 40px 20px;
    }

    .contenedor-testimonios {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 20px;
    }

    .testimonio {
      border: 2px solid #000;
      padding: 10px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .testimonio img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      margin-bottom: 10px;
    }

    .testimonio h3 {
      color: #000;
      font-size: 1.2rem;
      margin-bottom: 10px;
    }

    .puntuacion {
      display: flex;
      margin-bottom: 10px;
    }

    .puntuacion img {
      width: 20px;
      height: 20px;
    }

    .testimonio p {
      color: #000;
      font-size: 1rem;
      text-align: justify;
    }

    /* Estilos de la información de envío y devoluciones */
    .informacion {
      background-color: #eee;
      padding: 40px 20px;
    }

    .contenedor-informacion {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-gap: 20px;
    }

    .icono-informacion {
      color: #f00;
      font-size: 3rem;
      text-align: center;
      margin-bottom: 10px;
    }

    .titulo-informacion {
      color: #000;
      font-size: 1.2rem;
      text-align: center;
      margin-bottom: 10px;
    }

    .texto-informacion {
      color: #000;
      font-size: 1rem;
      text-align: justify;
    }

    /* Estilos de la sección de preguntas frecuentes (FAQ) */
    .faq {
      background-color: #fff;
      padding: 40px 20px;
    }

    .contenedor-faq {
      display: flex;
      flex-direction: column;
    }

    .pregunta {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }

    .signo {
      color: #000;
      font-size: 1.5rem;
      margin-right: 10px;
    }

    .pregunta p {
      color: #000;
      font-size: 1.2rem;
    }

    .respuesta {
      color: #000;
      font-size: 1rem;
      text-align: justify;
      margin-left: 30px;
      display: none;
    }

    /* Estilos del footer (pie de página) */
    footer {
      background-color: #000;
      height: 200px;
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      padding: 20px;
    }

    .contenedor-footer {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-gap: 20px;
      width: 100%;
    }

    .columna-footer {
      display: flex;
      flex-direction: column;
      list-style: none;
    }

    .columna-footer li {
      margin: 10px 0;
    }

    .columna-footer a {
      color: #fff;
      font-size: 1rem;
    }

    .columna-footer a:hover {
      color: #f00;
    }

    .icono-footer {
      color: #fff;
      font-size: 2rem;
      margin-right: 10px;
    }

    .icono-footer:hover {
      color: #f00;
    }

    .linea-footer {
      color: #fff;
      font-size: 1rem;
    }

    /* Estilos del formulario de suscripción */
    .suscripcion {
      background-color: #eee;
      padding: 40px 20px;
    }

    .formulario {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .formulario input {
      width: 300px;
      border: 2px solid #000;
      padding: 10px;
      margin-right: 10px;
    }

    .formulario button {
      background-color: #f00;
      border: 2px solid #fff;
      color: #fff;
      font-size: 1.2rem;
      padding: 10px 20px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .formulario button:hover {
      background-color: #fff;
      color: #f00;
    }

    /* Estilos de los botones de redes sociales */
    .redes {
      background-color: #fff;
      padding: 40px 20px;
    }

    .contenedor-redes {
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .boton-red {
      display: inline-block;
      background-color: #f00;
      color: #fff;
      font-size: 2rem;
      padding: 10px 20px;
      margin: 10px;
      box-shadow: 2px 2px 5px rgba(0,0,0,0.5);
    }

    .boton-red:hover {
      background-color: #fff;
      color: #f00;
    }

    /* Estilos de la barra lateral de filtros */
    .barra {
      background-color: #eee;
      border: 2px solid #000;
      padding: 20px;
      position: fixed;
      top: 80px;
      left: 0;
      bottom: 200px;
      width: 300px;
      overflow-y: auto;
      display: none;
    }

    .titulo-barra {
      color: #000;
      font-size: 1.5rem;
      text-align: center;
      margin-bottom: 10px;
    }

    .filtro {
      display: flex;
      align-items: center;
      margin-bottom: 10px;
    }

    .filtro input {
      margin-right: 10px;
    }

    .filtro label {
      color: #000;
      font-size: 1.2rem;
    }

    .boton-barra {
      position: fixed;
      top: 80px;
      left: 0;
      background-color: #000;
      color: #fff;
      font-size: 2rem;
      padding: 10px;
      border: none;
    }

    .boton-barra:hover {
      background-color: #f00;
      color: #fff;
    }
  </style>
</head>
<body>
  <!-- Encabezado -->
  <header>
    <div class="logo">
      <img src="logo.png" alt="Logo de la tienda">
    </div>
    <nav class="menu">
      <ul>
        <li><a href="#"><i class="fas fa-tshirt"></i> Sudaderas</a></li>
        <li><a href="#"><i class="fas fa-paint-brush"></i> Personalización</a></li>
        <li><a href="#"><i class="fas fa-star"></i> Novedades</a></li>
      </ul>
    </nav>
    <div class="carrito">
      <img src="carrito.png" alt="Carrito de compras">
      <span class="cantidad">0</span>
    </div>
    <div class="cuenta">
      <button class="boton-cuenta"><i class="fas fa-user"></i> Cuenta</button>
      <div class="menu-cuenta">
        <ul>
          <li><a href="#"><i class="fas fa-sign-in-alt"></i> Iniciar sesión</a></li>
          <li><a href="#"><i class="fas fa-user-plus"></i> Registrarse</a></li>
          <li><a href="#"><i class="fas fa-shopping-bag"></i> Mis pedidos</a></li>
          <li><a href="#"><i class="fas fa-user-circle"></i> Mi perfil</a></li>
        </ul>
      </div>
    </div>
  </header>
  <!-- Banner principal -->
