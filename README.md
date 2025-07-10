<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Gift Haven - Premium Gifts & Souvenirs</title>
    <style>
        :root {
            --primary: #e63946;
            --secondary: #f1faee;
            --accent: #a8dadc;
            --dark: #1d3557;
            --light: #f8f9fa;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
            border-bottom: 1px solid #eee;
        }
        
        .logo h1 {
            color: var(--primary);
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .logo span {
            color: var(--dark);
            font-size: 1rem;
            display: block;
        }
        
        .search-bar {
            flex-grow: 1;
            margin: 0 30px;
            position: relative;
        }
        
        .search-bar input {
            width: 100%;
            padding: 10px 15px;
            border: 1px solid #ddd;
            border-radius: 30px;
            font-size: 16px;
        }
        
        .user-actions {
            display: flex;
            gap: 20px;
        }
        
        .user-actions a {
            color: var(--dark);
            text-decoration: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            font-size: 14px;
        }
        
        .user-actions i {
            font-size: 1.2rem;
            margin-bottom: 3px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            justify-content: center;
            padding: 15px 0;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--primary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(230,57,70,0.9), rgba(168,218,220,0.9));
            color: white;
            padding: 80px 0;
            text-align: center;
            margin-bottom: 40px;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .cta-button {
            display: inline-block;
            background-color: white;
            color: var(--primary);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Featured Products */
        .section-title {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .section-title h2 {
            font-size: 2rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 200px;
            overflow: hidden;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.05);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .product-price {
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .add-to-cart {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
            width: 100%;
        }
        
        .add-to-cart:hover {
            background-color: #c1121f;
        }
        
        /* Categories */
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
            margin-bottom: 60px;
        }
        
        .category-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: all 0.3s;
        }
        
        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .category-card img {
            width: 100%;
            height: 120px;
            object-fit: cover;
        }
        
        .category-title {
            padding: 15px;
            font-weight: 600;
            color: var(--dark);
        }
        
        /* Newsletter */
        .newsletter {
            background-color: var(--secondary);
            padding: 60px 0;
            text-align: center;
            margin-bottom: 60px;
        }
        
        .newsletter-content {
            max-width: 600px;
            margin: 0 auto;
        }
        
        .newsletter h3 {
            font-size: 1.8rem;
            color: var(--dark);
            margin-bottom: 20px;
        }
        
        .newsletter p {
            margin-bottom: 30px;
        }
        
        .newsletter-form {
            display: flex;
            justify-content: center;
        }
        
        .newsletter-form input {
            padding: 12px 20px;
            border: 1px solid #ddd;
            border-radius: 4px 0 0 4px;
            font-size: 16px;
            width: 70%;
            max-width: 400px;
        }
        
        .newsletter-form button {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 0 4px 4px 0;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .newsletter-form button:hover {
            background-color: #c1121f;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-column h4 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background-color: var(--primary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #eee;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: var(--accent);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-top {
                flex-direction: column;
                gap: 15px;
            }
            
            .search-bar {
                margin: 15px 0;
                width: 100%;
            }
            
            nav ul {
                flex-wrap: wrap;
            }
            
            nav ul li {
                margin: 5px 10px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
            
            .newsletter-form input {
                width: 100%;
                border-radius: 4px;
                margin-bottom: 10px;
            }
            
            .newsletter-form button {
                border-radius: 4px;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo">
                    <h1>The Gift Haven</h1>
                    <span>Thoughtful Gifts for Every Occasion</span>
                </div>
                
                <div class="search-bar">
                    <input type="text" placeholder="Search for gifts...">
                </div>
                
                <div class="user-actions">
                    <a href="#">
                        <i class="fas fa-user"></i>
                        <span>Account</span>
                    </a>
                    <a href="#">
                        <i class="fas fa-heart"></i>
                        <span>Wishlist</span>
                    </a>
                    <a href="#">
                        <i class="fas fa-shopping-cart"></i>
                        <span>Cart (0)</span>
                    </a>
                </div>
            </div>
            
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Shop</a></li>
                    <li><a href="#">Gift Cards</a></li>
                    <li><a href="#">Occasions</a></li>
                    <li><a href="#">Collections</a></li>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>Thoughtful Gifts for Special Moments</h2>
            <p>Find the perfect present for birthdays, anniversaries, holidays and more from our curated collection.</p>
            <a href="#" class="cta-button">Shop Now</a>
        </div>
    </section>
    
    <!-- Featured Products -->
    <section class="container">
        <div class="section-title">
            <h2>Featured Products</h2>
        </div>
        
        <div class="products-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f1669d82-80a3-4b92-b9ba-b090c40b554a.png" alt="Personalized engraved silver necklace with heart pendant on velvet display">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Personalized Heart Necklace</h3>
                    <div class="product-price">$39.99</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/538e532a-4343-47db-84f2-1b802a6700a6.png" alt="Premium scented soy candles in glass jars with minimalist labels and wooden lids">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Luxury Scented Candles</h3>
                    <div class="product-price">$24.99</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ebc5d23c-69fe-4767-ba82-1ec573f6ae02.png" alt="Custom photo calendar with spiral binding showing mountain landscape photos">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Custom Photo Calendar</h3>
                    <div class="product-price">$19.99</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
            
            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-image">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b18ef7ae-c1a2-499f-a5b2-834f4ee00c60.png" alt="Artisan ceramic coffee mug with hand-painted floral design on wooden table">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Hand-Painted Mug</h3>
                    <div class="product-price">$16.99</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Categories -->
    <section class="container">
        <div class="section-title">
            <h2>Shop by Category</h2>
        </div>
        
        <div class="categories">
            <div class="category-card">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a49fa5a1-00a1-4126-8b2d-3d6bd0de2da8.png" alt="Collection of jewelry items including necklaces, rings and bracelets on display">
                <div class="category-title">Jewelry</div>
            </div>
            
            <div class="category-card">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7ac45346-8e8a-4fb8-8340-1cac8e60378d.png" alt="Assortment of home decor items including vases, picture frames and decorative bowls">
                <div class="category-title">Home Decor</div>
            </div>
            
            <div class="category-card">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/4f45d953-7cfc-435d-a965-c47ee2c252b3.png" alt="Colorful stationery set with notebooks, pens and leather-bound journals">
                <div class="category-title">Stationery</div>
            </div>
            
            <div class="category-card">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/bdb87e9b-3066-4a2a-96cb-4126c7561a5b.png" alt="Gift basket filled with gourmet chocolates, cookies and specialty foods">
                <div class="category-title">Gift Baskets</div>
            </div>
            
            <div class="category-card">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7fefa11c-dc48-4faa-98a0-49d01f92d0ea.png" alt="Handmade plush teddy bears with ribbons around their necks sitting on shelf">
                <div class="category-title">Stuffed Animals</div>
            </div>
        </div>
    </section>
    
    <!-- Newsletter -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-content">
                <h3>Join Our Newsletter</h3>
                <p>Receive exclusive offers, new product announcements and gift ideas straight to your inbox.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Enter your email address">
                    <button type="submit">Subscribe</button>
                </form>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h4>Shop</h4>
                    <ul>
                        <li><a href="#">All Products</a></li>
                        <li><a href="#">New Arrivals</a></li>
                        <li><a href="#">Best Sellers</a></li>
                        <li><a href="#">Gift Cards</a></li>
                        <li><a href="#">Special Offers</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h4>Customer Service</h4>
                    <ul>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">FAQ</a></li>
                        <li><a href="#">Shipping & Returns</a></li>
                        <li><a href="#">Size Guide</a></li>
                        <li><a href="#">Track Order</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h4>About Us</h4>
                    <ul>
                        <li><a href="#">Our Story</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Sustainability</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Press</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h4>Connect</h4>
                    <ul>
                        <li><a href="#"><i class="fab fa-facebook-f"></i> Facebook</a></li>
                        <li><a href="#"><i class="fab fa-instagram"></i> Instagram</a></li>
                        <li><a href="#"><i class="fab fa-pinterest-p"></i> Pinterest</a></li>
                        <li><a href="#"><i class="fab fa-twitter"></i> Twitter</a></li>
                        <li><a href="#"><i class="fab fa-youtube"></i> YouTube</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>© 2023 The Gift Haven. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Simple cart functionality
        document.addEventListener('DOMContentLoaded', function() {
            const addToCartButtons = document.querySelectorAll('.add-to-cart');
            const cartCount = document.querySelector('.fa-shopping-cart').nextElementSibling;
            let count = 0;
            
            addToCartButtons.forEach(button => {
                button.addEventListener('click', function() {
                    count++;
                    cartCount.textContent = `Cart (${count})`;
                    
                    // Animation
                    button.textContent = 'Added!';
                    button.style.backgroundColor = '#4caf50';
                    
                    setTimeout(() => {
                        button.textContent = 'Add to Cart';
                        button.style.backgroundColor = '';
                    }, 1500);
                });
            });
            
            // Newsletter form submission
            const newsletterForm = document.querySelector('.newsletter-form');
            newsletterForm.addEventListener('submit', function(e) {
                e.preventDefault();
                const email = this.querySelector('input').value;
                if (email) {
                    alert('Thank you for subscribing to our newsletter!');
                    this.querySelector('input').value = '';
                }
            });
        });
    </script>
</body>
</html>
