<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Starbucks - 123 Main St, Your City</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="rgba(255,255,255,0.1)"/><circle cx="75" cy="75" r="1" fill="rgba(255,255,255,0.05)"/><circle cx="50" cy="10" r="0.5" fill="rgba(255,255,255,0.08)"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            opacity: 0.3;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 20px;
        }

        .logo {
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #00754a, #00a651);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
        }

        .cta-button {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(45deg, #00754a, #00a651);
            color: white;
            padding: 18px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 500;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(0,117,74,0.4);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0,117,74,0.6);
        }

        /* Location Section */
        .location-section {
            padding: 100px 20px;
            background: #f8f9fa;
            position: relative;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 600;
            margin-bottom: 3rem;
            color: #1e3c72;
        }

        .location-card {
            background: white;
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            text-align: center;
            transition: all 0.3s ease;
            margin-bottom: 30px;
        }

        .location-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 80px rgba(0,0,0,0.15);
        }

        .location-icon {
            font-size: 4rem;
            color: #00754a;
            margin-bottom: 20px;
        }

        .location-address {
            font-size: 1.3rem;
            font-weight: 500;
            color: #333;
            margin-bottom: 20px;
        }

        /* Gallery Section */
        .gallery {
            padding: 100px 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .gallery-item {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            height: 300px;
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        /* Features Section */
        .features {
            padding: 100px 20px;
            background: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .feature-card {
            text-align: center;
            padding: 40px 20px;
            border-radius: 20px;
            background: #f8f9fa;
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            background: linear-gradient(135deg, #00754a, #00a651);
            color: white;
            transform: translateY(-10px);
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        /* Hours Section */
        .hours {
            padding: 100px 20px;
            background: #f8f9fa;
        }

        .hours-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .hours-card {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
        }

        /* Footer */
        .footer {
            background: #1e3c72;
            color: white;
            text-align: center;
            padding: 50px 20px 20px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .social-links {
            margin-top: 30px;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin: 0 15px;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            color: #00a651;
            transform: translateY(-3px);
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .logo {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }

        .map-container {
            height: 400px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.2);
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="logo">☕</div>
            <h1>Starbucks Coffee</h1>
            <p>Your favorite coffee destination with premium brews and cozy atmosphere</p>
            <a href="https://maps.app.goo.gl/DuDFpnHHFjh2CtLX8" target="_blank" class="cta-button">
                <i class="fas fa-map-marker-alt"></i>
                Get Directions
            </a>
        </div>
    </section>

    <!-- Location Section -->
    <section class="location-section">
        <div class="container">
            <h2 class="section-title">Visit Us</h2>
            <div class="location-card">
                <div class="location-icon">
                    <i class="fas fa-map-marker-alt"></i>
                </div>
                <div class="location-address">
                    123 Main St<br>
                    Your City, State 12345
                </div>
                <a href="https://maps.app.goo.gl/DuDFpnHHFjh2CtLX8" target="_blank" class="cta-button">
                    <i class="fas fa-directions"></i>
                    Open in Google Maps
                </a>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3022.566745284537!2d-73.987319684593!3d40.75889597932681!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDQ1JzMzLjIiTiA3M8KwNTknMTYuNSJX!5e0!3m2!1sen!2sus!4v1690000000000!5m2!1sen!2sus"
                        width="100%" 
                        height="100%" 
                        style="border:0;" 
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade">
                    </iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section class="gallery">
        <div class="container">
            <h2 class="section-title">Our Space</h2>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <i class="fas fa-coffee" style="font-size: 4rem;"></i>
                    <div>Cozy Interior</div>
                </div>
                <div class="gallery-item">
                    <i class="fas fa-chair" style="font-size: 4rem;"></i>
                    <div>Comfortable Seating</div>
                </div>
                <div class="gallery-item">
                    <i class="fas fa-wifi" style="font-size: 4rem;"></i>
                    <div>Free WiFi</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <h2 class="section-title">What We Offer</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-coffee"></i>
                    </div>
                    <h3>Premium Coffee</h3>
                    <p>Artisanal coffee beans roasted to perfection</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-wifi"></i>
                    </div>
                    <h3>Free WiFi</h3>
                    <p>Stay connected while you enjoy your coffee</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-plug"></i>
                    </div>
                    <h3>Charging Stations</h3>
                    <p>Keep your devices powered up</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-utensils"></i>
                    </div>
                    <h3>Food & Pastries</h3>
                    <p>Freshly baked goods and snacks</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Hours Section -->
    <section class="hours">
        <div class="container">
            <h2 class="section-title">Hours of Operation</h2>
            <div class="hours-grid">
                <div class="hours-card">
                    <h3>Monday - Friday</h3>
                    <p>6:00 AM - 8:00 PM</p>
                </div>
                <div class="hours-card">
                    <h3>Saturday</h3>
                    <p>7:00 AM - 8:00 PM</p>
                </div>
                <div class="hours-card">
                    <h3>Sunday</h3>
                    <p>7:00 AM - 7:00 PM</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <div class="logo" style="font-size: 2.5rem; margin-bottom: 20px;">☕</div>
            <p>Experience the perfect blend of coffee and comfort</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-google"></i></a>
            </div>
            <p style="margin-top: 30px; opacity: 0.8; font-size: 0.9rem;">
                &copy; 2024 Starbucks. All rights reserved. | 
                <a href="https://maps.app.goo.gl/DuDFpnHHFjh2CtLX8" target="_blank" style="color: #00a651;">View on Google Maps</a>
            </p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add scroll effect to hero
        window.addEventListener('scroll', () => {
            const hero = document.querySelector('.hero');
            const scrolled = window.pageYOffset;
            hero.style.transform = `translateY(${scrolled * 0.5}px)`;
        });
    </script>
</body>
</html>
