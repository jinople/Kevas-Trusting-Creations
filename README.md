<!DOCTYPE html>
<html>
<head>
<title>My Simple Website</title>
<style>
body {
font-family: Arial, sans-serif;
text-align: center;
}
.image-container {
margin: 20px;
}
img {
width: 200px;
height: 150px;
border: 1px solid #ccc;
}
.image-text {
font-size: 18px;
margin-top: 10px;
}
.price {
font-size: 24px;
font-weight: bold;
color: #00698f;
}
</style>
</head>
<body>
<h1>Welcome to My Simple Website</h1>
<div class="image-container">
<img src="image1.jpg" alt="Image 1">
<p class="image-text">This is image 1</p>
<p class="price">$19.99</p>
</div>
<div class="image-container">
<img src="image2.jpg" alt="Image 2">
<p class="image-text">This is image 2</p>
<p class="price">$29.99</p>
</div>
<div class="image-container">
<img src="image3.jpg" alt="Image 3">
<p class="image-text">This is image 3</p>
<p class="price">$39.99</p>
</div>

<!-- Add a simple checkout form -->
<form id="checkout-form">
<label>Card Number:</label>
<input type="text" id="card-number" />
<label>Expiration Date:</label>
<input type="text" id="expiration-date" />
<label>CVC:</label>
<input type="text" id="cvc" />
<button type="submit">Pay $19.99</button>
</form>

<!-- Add Stripe's JavaScript library and checkout code -->
<script src="https://js.stripe.com/v3/"></script>
<script>
const stripe = Stripe('Secret key');
const checkoutForm = document.getElementById('checkout-form');

checkoutForm.addEventListener('submit', event => {
event.preventDefault();
stripe.createToken({
card: {
number: document.getElementById('card-number').value,
exp_month: document.getElementById('expiration-date').value.split('/')[0],
exp_year: document.getElementById('expiration-date').value.split('/')[1],
cvc: document.getElementById('cvc').value
}
}).then(result => {
// Send the token to your server to charge the customer
fetch('/charge', {
method: 'POST',
headers: {
'Content-Type': 'application/json'
},
body: JSON.stringify({ token: result.token.id })
}).then(response => {
response.json().then(data => {
console.log(data);
});
});
});
</script>
</body>
</html>
