<!DOCTYPE html>
<html>
<head>
<title>Flipkart Shopping Website</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #f1f3f6;
}

header {
    background: #2874f0;
    color: white;
    padding: 15px 5%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
}

.logo {
    font-size: 27px;
    font-weight: bold;
}

.search {
    padding: 11px;
    width: 40%;
    border: none;
    border-radius: 4px;
}

header button {
    padding: 10px 20px;
    background: white;
    color: #2874f0;
    border: none;
    cursor: pointer;
    font-weight: bold;
}

nav {
    background: white;
    padding: 15px;
    display: flex;
    justify-content: center;
    gap: 35px;
    flex-wrap: wrap;
}

nav a {
    text-decoration: none;
    color: #222;
    font-weight: bold;
}

.banner {
    background: linear-gradient(120deg, #2874f0, #73a9ff);
    color: white;
    margin: 15px;
    padding: 45px 20px;
    text-align: center;
    border-radius: 5px;
}

.banner h1 {
    font-size: 35px;
}

.banner p {
    margin: 12px;
}

.products {
    background: white;
    margin: 15px;
    padding: 20px;
}

.products h2 {
    margin-bottom: 20px;
}

.product-list {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
}

.product {
    border: 1px solid #ddd;
    padding: 15px;
    text-align: center;
    border-radius: 5px;
    transition: 0.3s;
}

.product:hover {
    box-shadow: 0 3px 12px #bbb;
    transform: translateY(-3px);
}

.product img {
    width: 100%;
    height: 180px;
    object-fit: contain;
    background: white;
}

.product h3 {
    margin: 10px;
}

.price {
    color: green;
    font-weight: bold;
    margin: 10px;
}

.product button {
    background: #2874f0;
    color: white;
    padding: 10px;
    border: none;
    cursor: pointer;
    border-radius: 4px;
}

.product button:hover {
    background: #1558c0;
}

footer {
    background: #172337;
    color: white;
    text-align: center;
    padding: 25px;
    margin-top: 20px;
}

@media(max-width:700px) {
    .search {
        width: 100%;
    }

    .product-list {
        grid-template-columns: repeat(2, 1fr);
    }

    nav {
        gap: 15px;
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">Flipkart</div>

    <input class="search" id="search"
    type="text" placeholder="Search for products...">

    <button>Login</button>

    <button onclick="showCart()">
        🛒 Cart (<span id="count">0</span>)
    </button>
</header>

<nav>
    <a href="#">Home</a>
    <a href="#electronics">Electronics</a>
    <a href="#fashion">Fashion</a>
    <a href="#shoes">Shoes</a>
</nav>

<div class="banner">
    <h1>Big Shopping Days!</h1>
    <p>Up to 50% OFF on Selected Products</p>
    <h2>Shop Now!</h2>
</div>

<!-- ELECTRONICS -->

<section class="products" id="electronics">

<h2>Best Electronics</h2>

<div class="product-list">

<div class="product">
<img src="https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?w=400" alt="Smartphone">
<h3>Samsung s24 Ultra</h3>
<p class="price">₹1,52,300</p>
<button onclick="addCart('Smartphone',12999)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1496181133206-80ce9b88a853?w=400" alt="Laptop">
<h3>Laptop</h3>
<p class="price">₹39,999</p>
<button onclick="addCart('Laptop',39999)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=400" alt="Headphones">
<h3>Headphones</h3>
<p class="price">₹999</p>
<button onclick="addCart('Headphones',999)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=400" alt="Smart Watch">
<h3>Smart Watch</h3>
<p class="price">₹1,499</p>
<button onclick="addCart('Smart Watch',1499)">Add to Cart</button>
</div>

</div>
</section>

<!-- FASHION -->

<section class="products" id="fashion">

<h2>Fashion Collection</h2>

<div class="product-list">

<div class="product">
<img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?w=400" alt="T-Shirt">
<h3>T-Shirt</h3>
<p class="price">₹499</p>
<button onclick="addCart('T-Shirt',499)">Add to Cart</button>
</div>

<div class="product" id="shoes">
<img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=400" alt="Shoes">
<h3>Shoes</h3>
<p class="price">₹999</p>
<button onclick="addCart('Shoes',999)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1548036328-c9fa89d128fa?w=400" alt="Handbag">
<h3>Handbag</h3>
<p class="price">₹153400</p>
<button onclick="addCart('Handbag',1299)">Add to Cart</button>
</div>

<div class="product">
<img src="https://images.unsplash.com/photo-1521369909029-2afed882baee?w=400" alt="Cap">
<h3>Cap</h3>
<p class="price">₹299</p>
<button onclick="addCart('Cap',299)">Add to Cart</button>
</div>

</div>
</section>

<footer>
<h3>Flipkart Shopping Demo</h3>
<p>© 2026 My Shopping Website</p>
</footer>

<script>

let cart = [];

function addCart(name, price) {

    cart.push({name, price});

    document.getElementById("count").innerText = cart.length;

    alert(name + " added to cart!");
}

function showCart() {

    if (cart.length === 0) {
        alert("Your cart is empty!");
        return;
    }

    let total = 0;
    let message = "Your Shopping Cart:\n";

    cart.forEach(function(item) {

        message += item.name + " - ₹" + item.price + "\n";

        total += item.price;

    });

    message += "\nTotal: ₹" + total;

    alert(message);
}

// SEARCH FUNCTION

document.getElementById("search").addEventListener("input", function() {

    let value = this.value.toLowerCase();

    document.querySelectorAll(".product").forEach(function(product) {

        product.style.display =
        product.innerText.toLowerCase().includes(value)
        ? "" : "none";

    });

});

</script>

</body>
</html>

# Website
