# Final Project and Deployment

## Objectives
Build a fully functional web application.
Apply HTML, CSS, and JavaScript concepts learned.
Deploy the project using GitHub Pages, Netlify, or Vercel.

## Instructions
Choose one of the following project ideas:
Blog Website: Implement a multi-page site with navigation.
Ecommerce Website: Implement a multi-page site with navigation.

>[!NOTE]
> - Include at least:
> - A responsive design.
> - JavaScript interactivity.
> - A deployment link.

## Tasks

Create a well-structured HTML5 document.
Use at least 5 different HTML elements.
Ensure semantic correctness.

Good luck and happy coding! 🚀💻



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AutoLux - Premium Car Lighting</title>
    <style>
        /* Global Styles */
        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: var(--dark);
            line-height: 1.6;
        }
        
        /* Header & Navigation */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 1.5rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        .cart-icon {
            position: relative;
        }
        
        .cart-count {
            position: absolute;
            top: -10px;
            right: -10px;
            background-color: var(--secondary);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1494972308805-463bc619d34e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 60vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }
        
        .hero-content {
            max-width: 800px;
            padding: 2rem;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #c0392b;
            cursor: pointer;
        }
        
        /* Products Section */
        .products {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2rem;
            color: var(--primary);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .product-image {
            height: 200px;
            width: 100%;
            object-fit: cover;
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        
        .product-price {
            font-weight: bold;
            color: var(--secondary);
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }
        
        .product-description {
            color: #666;
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            padding: 2rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-column h3 {
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.5rem;
        }
        
        .footer-column a {
            color: var(--light);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column a:hover {
            color: var(--secondary);
        }
        
        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                padding: 1rem;
            }
            
            .nav-links {
                margin-top: 1rem;
            }
            
            .nav-links li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
        
        /* Cart Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 200;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            max-width: 600px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .close-modal {
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .cart-items {
            margin-bottom: 1.5rem;
        }
        
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            border-bottom: 1px solid #eee;
        }
        
        .cart-total {
            font-weight: bold;
            font-size: 1.2rem;
            text-align: right;
            margin-top: 1rem;
        }
        
        .checkout-btn {
            width: 100%;
            margin-top: 1rem;
        }
    </style>
</head>
<body>
    <!-- Header with Navigation -->
    <header>
        <nav>
            <a href="#" class="logo">AutoLux</a>
            <ul class="nav-links">
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li>
                    <a href="#" class="cart-icon" id="cart-button">
                        🛒 <span class="cart-count">0</span>
                    </a>
                </li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Premium Car Lighting Solutions</h1>
            <p>Upgrade your vehicle with our high-performance headlights, fog lights, and LED accessories</p>
            <a href="#products" class="btn">Shop Now</a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <h2 class="section-title">Our Products</h2>
        <div class="product-grid">
            <!-- Product 1 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1590845947676-fa2576f401d2?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="LED Headlights" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">UltraBright LED Headlights</h3>
                    <p class="product-price">$129.99</p>
                    <p class="product-description">High-intensity LED headlights with 6000K white light and 50,000 hour lifespan</p>
                    <button class="btn add-to-cart" data-id="1" data-name="UltraBright LED Headlights" data-price="129.99">Add to Cart</button>
                </div>
            </article>

            <!-- Product 2 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1554744512-d6c603f27a54?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Fog Lights" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">ProBeam Fog Lights</h3>
                    <p class="product-price">$89.99</p>
                    <p class="product-description">Weather-resistant fog lights with wide beam pattern for improved visibility</p>
                    <button class="btn add-to-cart" data-id="2" data-name="ProBeam Fog Lights" data-price="89.99">Add to Cart</button>
                </div>
            </article>

            <!-- Product 3 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1580310614697-2c8a4a716037?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="HID Conversion Kit" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">HID Conversion Kit</h3>
                    <p class="product-price">$149.99</p>
                    <p class="product-description">Complete HID conversion kit with ballasts and 8000K bulbs</p>
                    <button class="btn add-to-cart" data-id="3" data-name="HID Conversion Kit" data-price="149.99">Add to Cart</button>
                </div>
            </article>

            <!-- Product 4 -->
            <article class="product-card">
                <img src="https://images.unsplash.com/photo-1554744512-d6c603f27a54?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="LED Light Bar" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">Off-Road LED Light Bar</h3>
                    <p class="product-price">$199.99</p>
                    <p class="product-description">32-inch curved LED light bar with 120W output for off-road adventures</p>
                    <button class="btn add-to-cart" data-id="4" data-name="Off-Road LED Light Bar" data-price="199.99">Add to Cart</button>
                </div>
            </article>
        </div>
    </section>

    <!-- About Section -->
    <section class="products" id="about">
        <h2 class="section-title">About AutoLux</h2>
        <div style="max-width: 800px; margin: 0 auto; padding: 0 2rem;">
            <p style="margin-bottom: 1.5rem; text-align: center;">
                AutoLux has been providing premium automotive lighting solutions since 2010. 
                Our products are engineered for performance, durability, and style.
            </p>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem; margin-top: 2rem;">
                <div style="text-align: center;">
                    <h3 style="margin-bottom: 1rem;">Quality</h3>
                    <p>All products meet or exceed OEM standards</p>
                </div>
                <div style="text-align: center;">
                    <h3 style="margin-bottom: 1rem;">Innovation</h3>
                    <p>Cutting-edge lighting technology</p>
                </div>
                <div style="text-align: center;">
                    <h3 style="margin-bottom: 1rem;">Support</h3>
                    <p>Lifetime technical support</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="footer-content">
            <div class="footer-column">
                <h3>AutoLux</h3>
                <p>Premium automotive lighting solutions for all vehicle makes and models.</p>
            </div>
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contact</h3>
                <ul>
                    <li>123 Light Street</li>
                    <li>Detroit, MI 48201</li>
                    <li>info@autolux.com</li>
                    <li>(555) 123-4567</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 AutoLux. All rights reserved.</p>
        </div>
    </footer>

    <!-- Cart Modal -->
    <div class="modal" id="cart-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Your Cart</h2>
                <span class="close-modal">&times;</span>
            </div>
            <div class="cart-items" id="cart-items">
                <!-- Cart items will be added here dynamically -->
            </div>
            <div class="cart-total">
                Total: $<span id="cart-total">0.00</span>
            </div>
            <button class="btn checkout-btn">Proceed to Checkout</button>
        </div>
    </div>

    <script>
        // Cart functionality
        let cart = [];
        
        // DOM Elements
        const addToCartButtons = document.querySelectorAll('.add-to-cart');
        const cartButton = document.getElementById('cart-button');
        const cartModal = document.getElementById('cart-modal');
        const closeModal = document.querySelector('.close-modal');
        const cartItemsContainer = document.getElementById('cart-items');
        const cartTotalElement = document.getElementById('cart-total');
        const cartCountElement = document.querySelector('.cart-count');
        
        // Event Listeners
        addToCartButtons.forEach(button => {
            button.addEventListener('click', addToCart);
        });
        
        cartButton.addEventListener('click', openCart);
        closeModal.addEventListener('click', closeCart);
        
        // Functions
        function addToCart(e) {
            const button = e.target;
            const id = button.getAttribute('data-id');
            const name = button.getAttribute('data-name');
            const price = parseFloat(button.getAttribute('data-price'));
            
            // Check if item already in cart
            const existingItem = cart.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    id,
                    name,
                    price,
                    quantity: 1
                });
            }
            
            updateCart();
            
            // Visual feedback
            button.textContent = 'Added!';
            setTimeout(() => {
                button.textContent = 'Add to Cart';
            }, 1000);
        }
        
        function updateCart() {
            // Update cart count
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            cartCountElement.textContent = totalItems;
            
            // Save to localStorage
            localStorage.setItem('cart', JSON.stringify(cart));
        }
        
        function openCart(e) {
            e.preventDefault();
            renderCartItems();
            cartModal.style.display = 'flex';
        }
        
        function closeCart() {
            cartModal.style.display = 'none';
        }
        
        function renderCartItems() {
            cartItemsContainer.innerHTML = '';
            
            if (cart.length === 0) {
                cartItemsContainer.innerHTML = '<p>Your cart is empty</p>';
                cartTotalElement.textContent = '0.00';
                return;
            }
            
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                
                const cartItemElement = document.createElement('div');
                cartItemElement.className = 'cart-item';
                cartItemElement.innerHTML = `
                    <div>
                        <h4>${item.name}</h4>
                        <p>$${item.price} x ${item.quantity}</p>
                    </div>
                    <div>
                        <p>$${itemTotal.toFixed(2)}</p>
                    </div>
                `;
                
                cartItemsContainer.appendChild(cartItemElement);
            });
            
            cartTotalElement.textContent = total.toFixed(2);
        }
        
        // Close modal when clicking outside
        window.addEventListener('click', (e) => {
            if (e.target === cartModal) {
                closeCart();
            }
        });
        
        // Load cart from localStorage
        function loadCart() {
            const savedCart = localStorage.getItem('cart');
            if (savedCart) {
                cart = JSON.parse(savedCart);
                updateCart();
            }
        }
        
        // Initialize
        document.addEventListener('DOMContentLoaded', loadCart);
    </script>
</body>
</html>
