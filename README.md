<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nasim</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            text-align: center;
        }

        header {
            background-color: #333;
            color: white;
            padding: 20px 0;
        }

        header h1 {
            margin: 0;
        }

        .product-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            padding: 30px;
        }

        .product {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .product:hover {
            transform: translateY(-10px);
        }

        .product img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .product h3 {
            margin-top: 15px;
            color: #333;
        }

        .product p {
            color: #777;
            font-size: 14px;
        }

        .product input, .product select {
            margin-top: 10px;
            padding: 10px;
            width: 100%;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .product button {
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .product button:hover {
            background-color: #218838;
        }

        .cart {
            margin-top: 40px;
            padding: 20px;
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        .cart h2 {
            margin-bottom: 20px;
            color: #333;
        }

        .cart ul {
            list-style: none;
            padding: 0;
            text-align: left;
            margin-bottom: 20px;
        }

        .cart ul li {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin: 10px 0;
            padding: 10px;
            background-color: #f9f9f9;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .cart ul li img {
            width: 50px;
            height: auto;
            border-radius: 5px;
            margin-right: 15px;
        }

        .cart ul li .product-details {
            flex-grow: 1;
            text-align: left;
        }

        .cart ul li .product-details h4 {
            margin: 0;
            font-size: 16px;
            color: #333;
        }

        .cart ul li .product-details p {
            margin: 5px 0;
            font-size: 14px;
            color: #777;
        }

        .checkout-button {
            padding: 15px 30px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .checkout-button:hover {
            background-color: #0056b3;
        }

    </style>
</head>
<body>

    <header>
        <h1>Tienda Online</h1>
        <p>¡Los mejores productos al mejor precio!</p>
    </header>

    <div class="product-container">
        <!-- Producto 1 -->
        <div class="product">
            <img id="product1Image" src="https://via.placeholder.com/300" alt="Producto 1">
            <h3>Producto 1</h3>
            <p>Descripción del Producto 1: Este es un producto de alta calidad.</p>
            <label for="quantity1">Cantidad:</label>
            <input type="number" id="quantity1" min="1" value="1">
            <label for="weight1">Peso:</label>
            <select id="weight1" onchange="updateImage('product1')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 1', document.getElementById('quantity1').value, document.getElementById('weight1').value)">Añadir al carrito</button>
        </div>

        <!-- Producto 2 -->
        <div class="product">
            <img id="product2Image" src="https://via.placeholder.com/300" alt="Producto 2">
            <h3>Producto 2</h3>
            <p>Descripción del Producto 2: Este es otro producto increíble.</p>
            <label for="quantity2">Cantidad:</label>
            <input type="number" id="quantity2" min="1" value="1">
            <label for="weight2">Peso:</label>
            <select id="weight2" onchange="updateImage('product2')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 2', document.getElementById('quantity2').value, document.getElementById('weight2').value)">Añadir al carrito</button>
        </div>

        <!-- Producto 3 -->
        <div class="product">
            <img id="product3Image" src="https://via.placeholder.com/300" alt="Producto 3">
            <h3>Producto 3</h3>
            <p>Descripción del Producto 3: Un producto versátil y práctico.</p>
            <label for="quantity3">Cantidad:</label>
            <input type="number" id="quantity3" min="1" value="1">
            <label for="weight3">Peso:</label>
            <select id="weight3" onchange="updateImage('product3')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 3', document.getElementById('quantity3').value, document.getElementById('weight3').value)">Añadir al carrito</button>
        </div>

        <!-- Producto 4 -->
        <div class="product">
            <img id="product4Image" src="https://via.placeholder.com/300" alt="Producto 4">
            <h3>Producto 4</h3>
            <p>Descripción del Producto 4: Producto altamente recomendado.</p>
            <label for="quantity4">Cantidad:</label>
            <input type="number" id="quantity4" min="1" value="1">
            <label for="weight4">Peso:</label>
            <select id="weight4" onchange="updateImage('product4')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 4', document.getElementById('quantity4').value, document.getElementById('weight4').value)">Añadir al carrito</button>
        </div>

        <!-- Producto 5 -->
        <div class="product">
            <img id="product5Image" src="https://via.placeholder.com/300" alt="Producto 5">
            <h3>Producto 5</h3>
            <p>Descripción del Producto 5: Producto popular en nuestra tienda.</p>
            <label for="quantity5">Cantidad:</label>
            <input type="number" id="quantity5" min="1" value="1">
            <label for="weight5">Peso:</label>
            <select id="weight5" onchange="updateImage('product5')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 5', document.getElementById('quantity5').value, document.getElementById('weight5').value)">Añadir al carrito</button>
        </div>

        <!-- Producto 6 -->
        <div class="product">
            <img id="product6Image" src="https://via.placeholder.com/300" alt="Producto 6">
            <h3>Producto 6</h3>
            <p>Descripción del Producto 6: Un producto único y especial.</p>
            <label for="quantity6">Cantidad:</label>
            <input type="number" id="quantity6" min="1" value="1">
            <label for="weight6">Peso:</label>
            <select id="weight6" onchange="updateImage('product6')">
                <option value="500">500 g</option>
                <option value="6000">6 kg</option>
                <option value="8000">8 kg</option>
            </select>
            <button onclick="addToCart('Producto 6', document.getElementById('quantity6').value, document.getElementById('weight6').value)">Añadir al carrito</button>
        </div>
    </div>

    <div class="cart">
        <h2>Carrito</h2>
        <ul id="cartList"></ul>
        <button id="checkoutButton" class="checkout-button" style="display:none;" onclick="sendToWhatsApp()">Realizar Pedido</button>
    </div>

    <script>
        let cart = [];

        // Update image based on selected weight
        function updateImage(productId) {
            const weight = document.getElementById(productId + 'Weight').value;
            const image = document.getElementById(productId + 'Image');

            // Switch image based on weight
            if (weight === '500') {
                image.src = 'https://via.placeholder.com/300?text=500g';
            } else if (weight === '6000') {
                image.src = 'https://via.placeholder.com/300?text=6kg';
            } else if (weight === '8000') {
                image.src = 'https://via.placeholder.com/300?text=8kg';
            }
        }

        function addToCart(product, quantity, weight) {
            // Restrict order to at least 10 for 500g only
            if (weight === '500' && quantity < 10) {
                alert('La cantidad mínima para 500g es 10.');
                return;
            }

            // Allow adding to cart
            cart.push({ product, quantity, weight });
            updateCart();
        }

        function updateCart() {
            let cartList = document.getElementById('cartList');
            cartList.innerHTML = '';
            cart.forEach(item => {
                let listItem = document.createElement('li');
                listItem.innerHTML = `
                    <img src="https://via.placeholder.com/50" alt="${item.product}">
                    <div class="product-details">
                        <h4>${item.product}</h4>
                        <p>Cantidad: ${item.quantity}</p>
                        <p>Peso: ${item.weight} g</p>
                    </div>
                `;
                cartList.appendChild(listItem);
            });

            document.getElementById('checkoutButton').style.display = cart.length > 0 ? 'inline' : 'none';
        }

        function sendToWhatsApp() {
            let message = "Nuevo Pedido:\n";
            cart.forEach(item => {
                message += `${item.product} - Cantidad: ${item.quantity} - Peso: ${item.weight} g\n`;
            });

            let phoneNumber = "624677424";
            let encodedMessage = encodeURIComponent(message);
            let url = `https://wa.me/${phoneNumber}?text=${encodedMessage}`;
            window.open(url, '_blank');
        }
    </script>

</body>
</html>
