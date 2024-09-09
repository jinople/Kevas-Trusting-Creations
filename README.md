<!DOCTYPE html>
<html>
<head>
<title>Keva's Trusting Creations</title>
<style>
body {
font-family: Arial, sans-serif;
background-color: #f5f5f5;
}
header {
background-color: #00698f;
color: #fff;
padding: 20px;
text-align: center;
}
nav {
background-color: #333;
color: #fff;
padding: 20px;
text-align: center;
}
nav a {
color: #fff;
text-decoration: none;
margin: 20px;
}
nav a:hover {
color: #ccc;
}
main {
display: flex;
flex-wrap: wrap;
justify-content: center;
}
.shirt-container {
margin: 20px;
width: 250px;
height: 350px;
background-color: #fff;
border: 1px solid #ddd;
border-radius: 10px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.shirt-image {
width: 100%;
height: 150px;
object-fit: cover;
border-radius: 10px 10px 0 0;
}
.shirt-info {
padding: 20px;
}
.shirt-name {
font-weight: bold;
font-size: 18px;
}
.shirt-price {
font-size: 16px;
color: #00698f;
}
.paypal-button {
background-color: #00698f;
color: #fff;
border: none;
border-radius: 10px;
padding: 10px 20px;
cursor: pointer;
}
.paypal-button:hover {
background-color: #00457c;
}
</style>
</head>
<body>
<header>
<h1>Keva's Trusting Creations</h1>
</header>
<nav>
<a href="index.html">Home</a>
<a href="shirts-2.html">Shirts 2</a>
</nav>
<main>
<!-- Shirt 1 -->
<div class="shirt-container">
<img src="shirt1.jpg" alt="Shirt 1" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Trusting Tee</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 1', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 2 -->
<div class="shirt-container">
<img src="shirt2.jpg" alt="Shirt 2" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Believe Me</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 2', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 3 -->
<div class="shirt-container">
<img src="shirt3.jpg" alt="Shirt 3" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Hopeful Heart</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 3', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 4 -->
<div class="shirt-container">
<img src="shirt4.jpg" alt="Shirt 4" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Faithful Friend</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 4', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 5 -->
<div class="shirt-container">
<img src="shirt5.jpg" alt="Shirt 5" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Loyal Love</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 5', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 6 -->
<div class="shirt-container">
<img src="shirt6.jpg" alt="Shirt 6" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Kindness Keeper</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 6', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 7 -->
<div class="shirt-container">
<img src="shirt7.jpg" alt="Shirt 7" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Gentle Soul</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 7', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 8 -->
<div class="shirt-container">
<img src="shirt8.jpg" alt="Shirt 8" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Peaceful Pulse</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 8', '19.99')">Buy Now</button>
</div>
</div>
</main>
<script src="https://www.paypal.com/sdk/js?client-id=YOUR_PAYPAL_CLIENT_ID"></script>
<script>
function paypalCheckout(shirtName, price) {
paypal.Buttons({
createOrder: function(data, actions) {
return actions.order.create({
purchase_units: [{
amount: {
currency_code: 'USD',
value: price
}
}]
});
},
onApprove: function(data, actions) {
return actions.order.capture().then(function(details) {
console.log(Payment successful for ${shirtName}!);
});
}
}).render('#paypal-button-container');
}
</script>
</body>
</html>
html
<!-- Shirt 9 -->
<div class="shirt-container">
<img src="shirt9.jpg" alt="Shirt 9" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Tranquil Tee</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 9', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 10 -->
<div class="shirt-container">
<img src="shirt10.jpg" alt="Shirt 10" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Serenity Shirt</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 10', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 11 -->
<div class="shirt-container">
<img src="shirt11.jpg" alt="Shirt 11" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Harmony Hoodie</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 11', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 12 -->
<div class="shirt-container">
<img src="shirt12.jpg" alt="Shirt 12" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Peaceful Pullover</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 12', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 13 -->
<div class="shirt-container">
<img src="shirt13.jpg" alt="Shirt 13" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Calm Crewneck</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 13', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 14 -->
<div class="shirt-container">
<img src="shirt14.jpg" alt="Shirt 14" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Soothing Sweater</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 14', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 15 -->
<div class="shirt-container">
<img src="shirt15.jpg" alt="Shirt 15" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Tranquil Tee</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 15', '19.99')">Buy Now</button>
</div>
</div>
<!-- Shirt 16 -->
<div class="shirt-container">
<img src="shirt16.jpg" alt="Shirt 16" class="shirt-image">
<div class="shirt-info">
<h2 class="shirt-name">Serenity Shirt</h2>
<p class="shirt-price">$19.99</p>
<button class="paypal-button" onclick="paypalCheckout('Shirt 16', '19.99')">Buy Now</button>
</div>
</div>
