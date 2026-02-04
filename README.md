<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cosmic Digitalz - Digital Marketing Agency</title>
    <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --cosmic-navy: #0A0E27;
            --cosmic-purple: #6366F1;
            --cosmic-cyan: #06B6D4;
            --cosmic-pink: #EC4899;
            --cosmic-gold: #F59E0B;
            --text-white: #F8FAFC;
            --text-gray: #94A3B8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'DM Sans', sans-serif;
            background: var(--cosmic-navy);
            color: var(--text-white);
            overflow-x: hidden;
        }

        /* Animated Background */
        .cosmic-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #0A0E27 0%, #1a1f3a 100%);
        }

        .cosmic-bg::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 800px;
            height: 800px;
            background: radial-gradient(circle, rgba(99, 102, 241, 0.15) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 20s ease-in-out infinite;
        }

        .cosmic-bg::after {
            content: '';
            position: absolute;
            bottom: -30%;
            left: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(6, 182, 212, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 15s ease-in-out infinite reverse;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            33% { transform: translate(30px, -50px) rotate(120deg); }
            66% { transform: translate(-20px, 20px) rotate(240deg); }
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            backdrop-filter: blur(10px);
            background: rgba(10, 14, 39, 0.8);
            border-bottom: 1px solid rgba(99, 102, 241, 0.1);
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from { transform: translateY(-100%); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        .logo {
            font-family: 'Syne', sans-serif;
            font-size: 1.8rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-gray);
            text-decoration: none;
            font-weight: 500;
            position: relative;
            transition: color 0.3s;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--cosmic-purple), var(--cosmic-cyan));
            transition: width 0.3s;
        }

        .nav-links a:hover {
            color: var(--text-white);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .cta-button {
            padding: 0.8rem 2rem;
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-pink));
            border: none;
            border-radius: 50px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.4);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 8rem 5% 4rem;
            position: relative;
        }

        .hero-content h1 {
            font-family: 'Syne', sans-serif;
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-cyan), var(--cosmic-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-content p {
            font-size: 1.3rem;
            color: var(--text-gray);
            max-width: 600px;
            margin: 0 auto 2.5rem;
            line-height: 1.7;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

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

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            animation: fadeInUp 1s ease-out 0.7s both;
        }

        .btn-primary {
            padding: 1rem 2.5rem;
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-pink));
            border: none;
            border-radius: 50px;
            color: white;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.5);
        }

        .btn-secondary {
            padding: 1rem 2.5rem;
            background: transparent;
            border: 2px solid var(--cosmic-purple);
            border-radius: 50px;
            color: white;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-secondary:hover {
            background: rgba(99, 102, 241, 0.1);
            transform: translateY(-3px);
        }

        /* Services Section */
        .services {
            padding: 6rem 5%;
            position: relative;
        }

        .section-title {
            font-family: 'Syne', sans-serif;
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            text-align: center;
            margin-bottom: 1rem;
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-gray);
            font-size: 1.2rem;
            margin-bottom: 4rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 20px;
            padding: 2.5rem;
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.4s;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: var(--cosmic-purple);
            box-shadow: 0 20px 60px rgba(99, 102, 241, 0.2);
        }

        .service-card:hover::before {
            opacity: 1;
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            display: inline-block;
        }

        .service-card h3 {
            font-family: 'Syne', sans-serif;
            font-size: 1.6rem;
            margin-bottom: 1rem;
            position: relative;
        }

        .service-card p {
            color: var(--text-gray);
            line-height: 1.7;
            position: relative;
        }

        /* Stats Section */
        .stats {
            padding: 5rem 5%;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.1), rgba(6, 182, 212, 0.05));
            margin: 4rem 0;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .stat-item h3 {
            font-family: 'Syne', sans-serif;
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.5rem;
        }

        .stat-item p {
            color: var(--text-gray);
            font-size: 1.1rem;
        }

        /* Process Section */
        .process {
            padding: 6rem 5%;
        }

        .process-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1400px;
            margin: 0 auto;
        }

        .step {
            text-align: center;
            padding: 2rem;
            position: relative;
        }

        .step-number {
            font-family: 'Syne', sans-serif;
            font-size: 4rem;
            font-weight: 800;
            background: linear-gradient(135deg, var(--cosmic-purple), var(--cosmic-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
        }

        .step h3 {
            font-family: 'Syne', sans-serif;
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .step p {
            color: var(--text-gray);
            line-height: 1.6;
        }

        /* Contact Section */
        .contact {
            padding: 6rem 5%;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.05), rgba(236, 72, 153, 0.05));
        }

        .contact-container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-form {
            display: grid;
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .form-group {
            display: grid;
            gap: 1.5rem;
            grid-template-columns: 1fr 1fr;
        }

        input, textarea {
            width: 100%;
            padding: 1.2rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(99, 102, 241, 0.2);
            border-radius: 10px;
            color: white;
            font-family: 'DM Sans', sans-serif;
            font-size: 1rem;
            transition: all 0.3s;
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: var(--cosmic-purple);
            background: rgba(255, 255, 255, 0.08);
        }

        textarea {
            resize: vertical;
            min-height: 150px;
            grid-column: 1 / -1;
        }

        /* Footer */
        footer {
            padding: 3rem 5%;
            border-top: 1px solid rgba(99, 102, 241, 0.1);
            text-align: center;
            color: var(--text-gray);
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .social-links {
            display: flex;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--text-gray);
            font-size: 1.5rem;
            transition: all 0.3s;
        }

        .social-links a:hover {
            color: var(--cosmic-purple);
            transform: translateY(-3px);
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .form-group {
                grid-template-columns: 1fr;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn-primary, .btn-secondary {
                width: 100%;
                max-width: 300px;
            }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <div class="cosmic-bg"></div>

    <nav>
        <div class="logo">Cosmic Digitalz</div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#process">Process</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button class="cta-button">Get Started</button>
    </nav>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>
                Elevate Your Brand in the <span class="gradient-text">Digital Universe</span>
            </h1>
            <p>
                We transform ambitious brands into digital powerhouses through data-driven strategies, 
                creative excellence, and cutting-edge marketing solutions.
            </p>
            <div class="hero-buttons">
                <a href="#contact" class="btn-primary">Start Your Journey</a>
                <a href="#services" class="btn-secondary">Explore Services</a>
            </div>
        </div>
    </section>

    <section class="stats">
        <div class="stats-grid">
            <div class="stat-item">
                <h3>250+</h3>
                <p>Projects Delivered</p>
            </div>
            <div class="stat-item">
                <h3>98%</h3>
                <p>Client Satisfaction</p>
            </div>
            <div class="stat-item">
                <h3>150M+</h3>
                <p>Impressions Generated</p>
            </div>
            <div class="stat-item">
                <h3>5X</h3>
                <p>Average ROI Growth</p>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <h2 class="section-title">Our <span class="gradient-text">Services</span></h2>
        <p class="section-subtitle">
            Comprehensive digital solutions tailored to skyrocket your online presence
        </p>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🎯</div>
                <h3>Strategic Marketing</h3>
                <p>
                    Data-driven strategies that align with your business goals and drive measurable results 
                    across all digital channels.
                </p>
            </div>
            <div class="service-card">
                <div class="service-icon">📱</div>
                <h3>Social Media Management</h3>
                <p>
                    Build engaged communities and amplify your brand voice with compelling content and 
                    strategic social campaigns.
                </p>
            </div>
            <div class="service-card">
                <div class="service-icon">🚀</div>
                <h3>SEO & Content</h3>
                <p>
                    Dominate search rankings with optimized content that attracts, engages, and converts 
                    your target audience.
                </p>
            </div>
            <div class="service-card">
                <div class="service-icon">💡</div>
                <h3>Brand Development</h3>
                <p>
                    Craft unforgettable brand identities that resonate with your audience and stand out 
                    in competitive markets.
                </p>
            </div>
            <div class="service-card">
                <div class="service-icon">📊</div>
                <h3>Analytics & Insights</h3>
                <p>
                    Transform data into actionable insights with comprehensive analytics and performance 
                    tracking dashboards.
                </p>
            </div>
            <div class="service-card">
                <div class="service-icon">🎨</div>
                <h3>Creative Services</h3>
                <p>
                    Stunning visuals and compelling narratives that capture attention and drive 
                    engagement across platforms.
                </p>
            </div>
        </div>
    </section>

    <section class="process" id="process">
        <h2 class="section-title">Our <span class="gradient-text">Process</span></h2>
        <p class="section-subtitle">
            A proven methodology that delivers exceptional results every time
        </p>
        <div class="process-steps">
            <div class="step">
                <div class="step-number">01</div>
                <h3>Discovery</h3>
                <p>We dive deep into your brand, goals, and audience to create a solid foundation.</p>
            </div>
            <div class="step">
                <div class="step-number">02</div>
                <h3>Strategy</h3>
                <p>Develop comprehensive strategies tailored to your unique business objectives.</p>
            </div>
            <div class="step">
                <div class="step-number">03</div>
                <h3>Execution</h3>
                <p>Launch campaigns with precision, creativity, and unwavering attention to detail.</p>
            </div>
            <div class="step">
                <div class="step-number">04</div>
                <h3>Optimization</h3>
                <p>Continuously refine and improve based on data insights and performance metrics.</p>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="contact-container">
            <h2 class="section-title">Let's Create Something <span class="gradient-text">Extraordinary</span></h2>
            <p class="section-subtitle">
                Ready to transform your digital presence? Get in touch and let's start your journey.
            </p>
            <form class="contact-form">
                <div class="form-group">
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Your Email" required>
                </div>
                <div class="form-group">
                    <input type="text" placeholder="Company Name">
                    <input type="tel" placeholder="Phone Number">
                </div>
                <textarea placeholder="Tell us about your project..." required></textarea>
                <button type="submit" class="btn-primary" style="justify-self: center;">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <div class="social-links">
                <a href="#" aria-label="LinkedIn">💼</a>
                <a href="#" aria-label="Twitter">🐦</a>
                <a href="#" aria-label="Instagram">📷</a>
                <a href="#" aria-label="Facebook">👍</a>
            </div>
            <p>&copy; 2026 Cosmic Digitalz. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scroll for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Form submission handler
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We\'ll get back to you soon.');
            this.reset();
        });

        // Add scroll-based animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.service-card, .step, .stat-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease-out, transform 0.6s ease-out';
            observer.observe(el);
        });
    </script>
</body>
</html>