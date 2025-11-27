# hanging-louis
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hanging Louis - Clothing Store</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            margin: 0; 
            padding: 0; 
            background: #fafafa;
        }
        header { 
            background: #1a1a1a; 
            color: #fff; 
            padding: 20px 0; 
            text-align: center;
            border-bottom: #444 2px solid;
        }
        .container { 
            width: 90%; 
            margin: auto; 
            display: flex; 
            flex-wrap: wrap; 
            justify-content: space-around; 
            padding-top: 20px;
        }
        .product { 
            width: 250px; 
            background: #fff; 
            padding: 20px; 
            margin: 15px; 
            border-radius: 10px; 
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .product h2 { font-size: 22px; margin-bottom: 10px; }
        .product p { margin: 10px 0; font-size: 18px; }
        .product button {
            padding: 10px 15px;
            width: 100%;
            background: #333;
            color: #fff;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }
        .product button:hover {
            background: #000;
        }
        .cart {
            background: #fff;
            padding: 20px;
            margin: 20px auto;
            width: 90%;
            border-radius: 10px;
            font-size: 18px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>

<header>
    <h1>Hanging Louis - Your Clothing Store</h1>
</header>

<div class="container">
    <div class="product">
        <h2>Polo T-Shirt</h2>
        <p>Price: ₹500</p>
        <button data-name="Polo T-Shirt">Add to Cart</button>
    </div>

    <div class="product">
        <h2>Hoodie</h2>
        <p>Price: ₹1200</p>
        <button data-name="Hoodie">Add to Cart</button>
    </div>
</div>

<div class="cart">
    <h2>Shopping Cart</h2>
    <p id="cart-info">No items in cart.</p>
</div>

<script>
    let count = 0;
    const buttons = document.querySelectorAll('button');
    const cartText = document.getElementById('cart-info');

    buttons.forEach(btn => {
        btn.addEventListener('click', () => {
            count++;
            cartText.textContent = `Items in cart: ${count}`;
        });
    });
</script>

</body>
</html>
