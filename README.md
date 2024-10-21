<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pendientes Artesanales</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            margin: 0;
        }
        nav {
            background-color: #444;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            display: inline-block;
        }
        .container {
            width: 80%;
            margin: auto;
        }
        .product {
            display: inline-block;
            background-color: white;
            border: 1px solid #ddd;
            margin: 10px;
            padding: 15px;
            width: 30%;
            text-align: center;
        }
        .product img {
            width: 100%;
            height: auto;
        }
        .product h2 {
            margin: 10px 0;
            font-size: 20px;
        }
        .product p {
            margin: 5px 0;
        }
        .product button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
        }
        .cart {
            text-align: right;
            margin-top: 20px;
        }
        .cart p {
            font-size: 18px;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }
        form {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
        }
        form input, form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        form button {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <h1>Pendientes Artesanales de Mi Hija</h1>
    </header>

    <nav>
        <a href="#productos">Productos</a>
        <a href="#contacto">Contacto</a>
    </nav>

    <div class="container">
        <section id="productos">
            <h2>Nuestros Pendientes</h2>

            <div class="cart">
                <p>Carrito: <span id="cart-count">0</span> pendientes</p>
            </div>

            <div class="product">
                <img src="https://via.placeholder.com/300x300" alt="Pendiente 1">
                <h2>Pendiente 1</h2>
                <p>Precio: $10</p>
                <button onclick="addToCart()">Añadir al carrito</button>
            </div>

            <div class="product">
                <img src="https://via.placeholder.com/300x300" alt="Pendiente 2">
                <h2>Pendiente 2</h2>
                <p>Precio: $12</p>
                <button onclick="addToCart()">Añadir al carrito</button>
            </div>

            <div class="product">
                <img src="https://via.placeholder.com/300x300" alt="Pendiente 3">
                <h2>Pendiente 3</h2>
                <p>Precio: $15</p>
                <button onclick="addToCart()">Añadir al carrito</button>
            </div>
        </section>

        <section id="contacto">
            <h2>Contacto</h2>
            <form>
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" placeholder="Tu nombre" required>

                <label for="email">Correo electrónico:</label>
                <input type="email" id="email" name="email" placeholder="Tu correo" required>

                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" rows="5" placeholder="Escribe tu mensaje aquí..." required></textarea>

                <button type="submit">Enviar mensaje</button>
            </form>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 Pendientes Artesanales. Todos los derechos reservados.</p>
    </footer>

    <script>
        let cartCount = 0;
        
        function addToCart() {
            cartCount++;
            document.getElementById("cart-count").textContent = cartCount;
            alert("Pendiente añadido al carrito!");
        }
    </script>
</body>
</html>
