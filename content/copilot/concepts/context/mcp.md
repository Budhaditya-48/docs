 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PowderPro - Premium Powder Solutions</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #2c3e50;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #e74c3c;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23f8f9fa" width="1200" height="600"/><circle fill="%23e3f2fd" opacity="0.6" cx="200" cy="150" r="80"/><circle fill="%23bbdefb" opacity="0.4" cx="800" cy="200" r="120"/><circle fill="%2390caf9" opacity="0.3" cx="1000" cy="400" r="60"/><path fill="%23fff" opacity="0.8" d="M300 450 Q400 500 500 450 Q600 400 700 450 Q800 500 900 450 L1000 480 L1100 470 Z"/></svg>');
            background-size: cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .cta-button {
            display: inline-block;
            background: #e74c3c;
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(231,76,60,0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(231,76,60,0.6);
        }

        /* Sections */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        section {
            padding: 100px 0;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: #2c3e50;
        }

        /* Products */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .product-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 1rem;
        }

        .product-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #2c3e50;
        }

        /* Features */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .feature {
            text-align: center;
            padding: 2rem;
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #e74c3c, #f39c12);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Contact */
        .contact {
            background: #f8f9fa;
        }

        .contact-form {
            max-width: 600px;
            margin: 3rem auto 0;
            display: grid;
            gap: 1rem;
        }

        .contact-form input,
        .contact-form textarea {
            padding: 15px;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #e74c3c;
        }

        /* Footer */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            section {
                padding: 60px 0;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.8s ease-out;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">PowderPro</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content fade-in">
            <h1>Premium Powder Solutions</h1>
            <p>Discover our finest selection of high-quality powders for industrial, cosmetic, and specialty applications. Excellence in every particle.</p>
            <a href="#products" class="cta-button">Explore Products</a>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="container">
        <h2 class="fade-in">Our Premium Products</h2>
        <div class="products-grid">
            <div class="product-card fade-in">
                <div style="background: linear-gradient(45deg, #e3f2fd, #bbdefb); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; margin-bottom: 1rem; font-size: 4rem;">⚗️</div>
                <h3>Chemical Powders</h3>
                <p>High-purity industrial chemicals in powder form for manufacturing and processing.</p>
            </div>
            <div class="product-card fade-in">
                <div style="background: linear-gradient(45deg, #f3e5f5, #e1bee7); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; margin-bottom: 1rem; font-size: 4rem;">💄</div>
                <h3>Cosmetic Powders</h3>
                <p>Premium cosmetic-grade powders for beauty and personal care products.</p>
            </div>
            <div class="product-card fade-in">
                <div style="background: linear-gradient(45deg, #e8f5e8, #c8e6c9); height: 200px; border-radius: 10px; display: flex; align-items: center; justify-content: center; margin-bottom: 1rem; font-size: 4rem;">🏭</div>
                <h3>Industrial Powders</h3>
                <p>Specialty powders for manufacturing, coating, and industrial applications.</p>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="about" style="background: #f8f9fa;">
        <div class="container">
            <h2 class="fade-in">Why Choose PowderPro?</h2>
            <div class="features-grid">
                <div class="feature fade-in">
                    <div class="feature-icon">✅</div>
                    <h3>Premium Quality</h3>
                    <p>ISO-certified quality control ensures every batch meets the highest standards.</p>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">🚚</div>
                    <h3>Fast Shipping</h3>
                    <p>Worldwide delivery with tracking. Most orders ship within 24 hours.</p>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">🧪</div>
                    <h3>Custom Solutions</h3>
                    <p>Tailored powder blends and custom packaging for your specific needs.</p>
                </div>
                <div class="feature fade-in">
                    <div class="feature-icon">💰</div>
                    <h3>Competitive Pricing</h3>
                    <p>Bulk discounts and flexible pricing for businesses of all sizes.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="fade-in">Get In Touch</h2>
            <form class="contact-form fade-in" onsubmit="submitForm(event)">
                <input type="text" placeholder="Your Name" required>
                <input type="email" placeholder="Your Email" required>
                <input type="text" placeholder="Subject" required>
                <textarea rows="5" placeholder="Your Message" required></textarea>
                <button type="submit" class="cta-button" style="width: 100%; margin-top: 1rem;">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 PowderPro. All rights reserved. | Premium Powder Solutions Worldwide</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission
        function submitForm(event) {
            event.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            event.target.reset();
        }

        // Fade in animation on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
                }
            });
        });

        document.querySelectorAll('.fade-in').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.8s ease-out, transform 0.8s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>

* [AUTOTITLE](/copilot/how-tos/copilot-cli/customize-copilot/add-mcp-servers)
* [AUTOTITLE](/copilot/how-tos/context/model-context-protocol/extending-copilot-chat-with-mcp)
* [AUTOTITLE](/copilot/how-tos/context/model-context-protocol/using-the-github-mcp-server)
* [AUTOTITLE](/copilot/tutorials/enhancing-copilot-agent-mode-with-mcp)
* [AUTOTITLE](/copilot/reference/customization-cheat-sheet)
