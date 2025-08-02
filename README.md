<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prakash Ke Pankh - A Journey Towards Minimising Myopia</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #4a5568;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo::before {
            content: "👁️";
            font-size: 2rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #4a5568;
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: #667eea;
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        main {
            margin-top: 80px;
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 600"><defs><linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" style="stop-color:%23667eea;stop-opacity:1" /><stop offset="100%" style="stop-color:%23764ba2;stop-opacity:1" /></linearGradient></defs><rect width="100%" height="100%" fill="url(%23bg)"/></svg>');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 8rem 0 6rem;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(102, 126, 234, 0.8), rgba(118, 75, 162, 0.8));
            animation: gradientShift 8s ease-in-out infinite;
        }

        @keyframes gradientShift {
            0%, 100% { opacity: 0.8; }
            50% { opacity: 0.6; }
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            font-weight: 300;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            animation: fadeInUp 1s ease-out 0.4s both;
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

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #ff6b6b, #ee5a24);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 107, 107, 0.4);
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(255, 107, 107, 0.6);
        }

        .section {
            padding: 5rem 0;
            background: white;
            margin: 2rem 0;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2, #ff6b6b);
        }

        .section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2d3748;
            position: relative;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .about-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            padding: 2.5rem;
            border-radius: 15px;
            color: white;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .about-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 1px, transparent 1px);
            background-size: 20px 20px;
            animation: float 20s linear infinite;
        }

        @keyframes float {
            0% { transform: rotate(0deg) translate(-50%, -50%); }
            100% { transform: rotate(360deg) translate(-50%, -50%); }
        }

        .about-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(240, 147, 251, 0.4);
        }

        .about-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            position: relative;
            z-index: 2;
        }

        .about-card p {
            position: relative;
            z-index: 2;
        }

        .founders {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .founder-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 2px solid transparent;
            background-clip: padding-box;
            position: relative;
        }

        .founder-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 15px;
            padding: 2px;
            background: linear-gradient(45deg, #667eea, #764ba2, #ff6b6b);
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: exclude;
            mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .founder-card:hover::before {
            opacity: 1;
        }

        .founder-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
        }

        .founder-avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            margin: 0 auto 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
            font-weight: bold;
        }

        .founder-card h3 {
            color: #2d3748;
            margin-bottom: 0.5rem;
            font-size: 1.5rem;
        }

        .founder-card .class-info {
            color: #667eea;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .school-info {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 3rem;
            border-radius: 15px;
            text-align: center;
            margin: 3rem 0;
            position: relative;
            overflow: hidden;
        }

        .school-info::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="rgba(255,255,255,0.1)"/></svg>');
            animation: float 30s linear infinite;
        }

        .school-info h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            position: relative;
            z-index: 2;
        }

        .school-info p {
            font-size: 1.1rem;
            position: relative;
            z-index: 2;
        }

        .myopia-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .info-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border-left: 4px solid #667eea;
            position: relative;
            overflow: hidden;
        }

        .info-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.05), rgba(118, 75, 162, 0.05));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .info-card:hover::before {
            opacity: 1;
        }

        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
        }

        .info-card h4 {
            color: #2d3748;
            margin-bottom: 1rem;
            font-size: 1.3rem;
            position: relative;
            z-index: 2;
        }

        .info-card ul {
            list-style: none;
            position: relative;
            z-index: 2;
        }

        .info-card li {
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .info-card li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
        }

        .vision-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            margin: 3rem 0;
            position: relative;
            overflow: hidden;
        }

        .vision-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 60"><circle cx="30" cy="30" r="1" fill="rgba(255,255,255,0.1)"/></svg>');
            animation: twinkle 3s ease-in-out infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.8; }
        }

        .vision-card h3 {
            font-size: 2.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 2;
        }

        .vision-card p {
            font-size: 1.1rem;
            line-height: 1.8;
            position: relative;
            z-index: 2;
        }

        footer {
            background: #2d3748;
            color: white;
            text-align: center;
            padding: 3rem 0;
            margin-top: 4rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            margin-bottom: 1rem;
            color: #667eea;
        }

        .footer-section p, .footer-section a {
            margin-bottom: 0.5rem;
            color: #cbd5e0;
            text-decoration: none;
        }

        .footer-section a:hover {
            color: #667eea;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }

        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background: #667eea;
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: #764ba2;
            transform: translateY(-2px);
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .section {
                margin: 1rem 0;
                padding: 3rem 0;
            }
            
            .section h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <a href="#" class="logo">Prakash Ke Pankh</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#myopia">Myopia Info</a></li>
                <li><a href="#team">Team</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="hero-content container">
                <h1>Prakash Ke Pankh</h1>
                <div class="hero-subtitle">प्रकाश के पंख - Wings of Light</div>
                <p>A Journey Towards Minimising Myopia - Spreading awareness about eye health and myopia prevention, one person at a time</p>
                <a href="#about" class="cta-button">Learn More About Our Mission</a>
            </div>
        </section>

        <section id="about" class="section">
            <div class="container">
                <h2>About Our Initiative</h2>
                <p style="text-align: center; font-size: 1.2rem; margin-bottom: 3rem; color: #4a5568;">
                    Prakash Ke Pankh is a student-led awareness initiative focused on educating people about myopia - its causes, consequences, and prevention methods. We believe that knowledge is the first step towards better eye health.
                </p>
                
                <div class="about-grid">
                    <div class="about-card">
                        <h3>🎯 Our Mission</h3>
                        <p>To create widespread awareness about myopia and its prevention, starting from our immediate community and expanding to reach as many people as possible through education and advocacy.</p>
                    </div>
                    <div class="about-card">
                        <h3>👁️ Our Focus</h3>
                        <p>Educating people about the causes, consequences, and prevention of myopia through interactive sessions, informative materials, and community outreach programs.</p>
                    </div>
                    <div class="about-card">
                        <h3>🌟 Our Approach</h3>
                        <p>We started with friends, family members, and relatives, and aim to extend our reach to larger platforms as we grow and develop our initiative.</p>
                    </div>
                </div>

                <div class="vision-card">
                    <h3>Our Vision</h3>
                    <p>We envision a future where myopia is not just treated but prevented through early awareness and proper eye care habits. By empowering individuals with knowledge about eye health, we hope to contribute to reducing the global burden of myopia, especially among young people who spend increasing amounts of time on digital devices.</p>
                </div>
            </div>
        </section>

        <section id="team" class="section">
            <div class="container">
                <h2>Meet Our Team</h2>
                <div class="founders">
                    <div class="founder-card">
                        <div class="founder-avatar">C</div>
                        <h3>Chayan Kashyap</h3>
                        <div class="class-info">Class 8 Student</div>
                        <p>Co-founder and passionate advocate for eye health awareness. Chayan brings enthusiasm and dedication to spreading knowledge about myopia prevention in our community.</p>
                    </div>
                    <div class="founder-card">
                        <div class="founder-avatar">A</div>
                        <h3>Arnab Jyoti Parashar</h3>
                        <div class="class-info">Class 8 Student</div>
                        <p>Co-founder with a strong commitment to health education. Arnab contributes innovative ideas and helps organize our awareness campaigns effectively.</p>
                    </div>
                </div>

                <div class="school-info">
                    <h3>🏫 Saint Francis De Sales School</h3>
                    <p>Satgaon, Narangi, Guwahati, Assam<br>
                    Proud to be representing our school in this important health awareness initiative</p>
                </div>
            </div>
        </section>

        <section id="myopia" class="section">
            <div class="container">
                <h2>Understanding Myopia</h2>
                <p style="text-align: center; font-size: 1.1rem; margin-bottom: 3rem; color: #4a5568;">
                    Myopia, commonly known as nearsightedness, is a growing concern worldwide. Here's what everyone should know:
                </p>

                <div class="myopia-info">
                    <div class="info-card">
                        <h4>🔍 What is Myopia?</h4>
                        <ul>
                            <li>A refractive error where distant objects appear blurry</li>
                            <li>Near objects can be seen clearly</li>
                            <li>Occurs when the eyeball is too long or cornea is too curved</li>
                            <li>Light focuses in front of the retina instead of on it</li>
                        </ul>
                    </div>
                    
                    <div class="info-card">
                        <h4>⚠️ Common Causes</h4>
                        <ul>
                            <li>Excessive near work (reading, writing, digital devices)</li>
                            <li>Lack of outdoor activities and natural light</li>
                            <li>Genetic factors and family history</li>
                            <li>Poor lighting conditions while studying</li>
                            <li>Prolonged screen time without breaks</li>
                        </ul>
                    </div>
                    
                    <div class="info-card">
                        <h4>🚨 Warning Signs</h4>
                        <ul>
                            <li>Difficulty seeing distant objects clearly</li>
                            <li>Squinting to see better</li>
                            <li>Headaches and eye strain</li>
                            <li>Sitting closer to TV or board</li>
                            <li>Rubbing eyes frequently</li>
                        </ul>
                    </div>
                    
                    <div class="info-card">
                        <h4>💪 Prevention Tips</h4>
                        <ul>
                            <li>Follow the 20-20-20 rule: Every 20 minutes, look at something 20 feet away for 20 seconds</li>
                            <li>Spend at least 2 hours outdoors daily</li>
                            <li>Maintain proper reading distance (arm's length)</li>
                            <li>Ensure good lighting while studying</li>
                            <li>Regular eye check-ups</li>
                        </ul>
                    </div>
                    
                    <div class="info-card">
                        <h4>📱 Digital Eye Care</h4>
                        <ul>
                            <li>Limit screen time, especially for children</li>
                            <li>Use blue light filters on devices</li>
                            <li>Maintain proper posture while using devices</li>
                            <li>Take frequent breaks from screens</li>
                            <li>Adjust screen brightness to match surroundings</li>
                        </ul>
                    </div>
                    
                    <div class="info-card">
                        <h4>🎯 Our Impact Goals</h4>
                        <ul>
                            <li>Educate 100+ people in our first phase</li>
                            <li>Create awareness materials in local languages</li>
                            <li>Organize eye health workshops</li>
                            <li>Collaborate with local eye care professionals</li>
                            <li>Expand to schools and community centers</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>Contact Us</h4>
                    <p>Saint Francis De Sales School</p>
                    <p>Satgaon, Narangi</p>
                    <p>Guwahati, Assam</p>
                </div>
                <div class="footer-section">
                    <h4>Our Initiative</h4>
                    <p>Prakash Ke Pankh</p>
                    <p>Myopia Awareness Program</p>
                    <p>Student-led Health Initiative</p>
                </div>
                <div class="footer-section">
                    <h4>Get Involved</h4>
                    <p>Join our awareness campaigns</p>
                    <p>Share our mission</p>
                    <p>Support eye health education</p>
                </div>
            </div>
            
            <div class="social-links">
                <a href="#" title="Facebook">📘</a>
                <a href="#" title="Instagram">📷</a>
                <a href="#" title="WhatsApp">💬</a>
                <a href="#" title="Email">📧</a>
            </div>
            
            <p style="margin-top: 2rem; padding-top: 2rem; border-top: 1px solid #4a5568;">
                &copy; 2025 Prakash Ke Pankh. Made with ❤️ by Chayan Kashyap & Arnab Jyoti Parashar
            </p>
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

        // Header background change on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
                header.style.boxShadow = '0 4px 30px rgba(0, 0, 0, 0.2)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
                header.style.boxShadow = '0 4px 30px rgba(0, 0, 0, 0.1)';
            }
        });

        // Add animation class when elements come into view
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe cards for animation
        document.querySelectorAll('.about-card, .founder-card, .info-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.transition = 'all 0.6s ease';
            observer.observe(card);
        });
    </script>
</body>
</html>
