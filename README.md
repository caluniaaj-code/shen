<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A.J. L. Calunia - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #6366f1;
            --secondary-color: #8b5cf6;
            --accent-color: #ec4899;
            --dark-bg: #0f172a;
            --card-bg: #1e293b;
            --text-primary: #f1f5f9;
            --text-secondary: #cbd5e1;
            --border-color: #334155;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, var(--dark-bg) 0%, #1a1f3a 100%);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            z-index: 1000;
            border-bottom: 1px solid var(--border-color);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
            font-size: 0.95rem;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            margin-top: 60px;
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
            background: radial-gradient(circle at 20% 50%, rgba(99, 102, 241, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 80%, rgba(168, 85, 247, 0.1) 0%, transparent 50%);
            z-index: -1;
        }

        .hero-content {
            z-index: 1;
            animation: fadeInUp 0.8s ease;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero .subtitle {
            font-size: 1.5rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        .hero .bio {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto 3rem;
            color: var(--text-secondary);
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            font-weight: 600;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(99, 102, 241, 0.3);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
        }

        .btn-secondary:hover {
            background: var(--primary-color);
            color: white;
        }

        /* Sections */
        section {
            padding: 6rem 0;
            border-bottom: 1px solid var(--border-color);
        }

        section h2 {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.2);
        }

        .skill-card h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 0.5rem 0;
            display: flex;
            align-items: center;
            color: var(--text-secondary);
        }

        .skill-list li::before {
            content: '→';
            color: var(--primary-color);
            margin-right: 0.8rem;
            font-weight: bold;
        }

        /* Proficiency Bars */
        .proficiency-item {
            margin-bottom: 1.5rem;
        }

        .proficiency-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .proficiency-bar {
            background: var(--border-color);
            height: 8px;
            border-radius: 10px;
            overflow: hidden;
        }

        .proficiency-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            border-radius: 10px;
            transition: width 0.6s ease;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(99, 102, 241, 0.3);
            border-color: var(--primary-color);
        }

        .project-header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            padding: 2rem;
            color: white;
        }

        .project-header h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .project-body {
            padding: 2rem;
        }

        .project-body p {
            color: var(--text-secondary);
            line-height: 1.8;
        }

        /* Education Timeline */
        .timeline {
            position: relative;
            padding: 2rem 0;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: linear-gradient(180deg, var(--primary-color), transparent);
        }

        .timeline-item {
            margin-bottom: 3rem;
            width: 45%;
        }

        .timeline-item:nth-child(odd) {
            margin-left: 0;
            text-align: right;
            padding-right: 3rem;
        }

        .timeline-item:nth-child(even) {
            margin-left: 55%;
            text-align: left;
            padding-left: 3rem;
        }

        .timeline-content {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 8px;
            border: 1px solid var(--border-color);
        }

        .timeline-content h3 {
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .timeline-content p {
            color: var(--text-secondary);
        }

        /* Contact Section */
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .contact-item {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .contact-item a {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-item a:hover {
            color: var(--accent-color);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: var(--card-bg);
            border: 2px solid var(--border-color);
            border-radius: 50%;
            color: var(--primary-color);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.5rem;
        }

        .social-links a:hover {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            background: rgba(15, 23, 42, 0.95);
            padding: 2rem;
            text-align: center;
            color: var(--text-secondary);
            border-top: 1px solid var(--border-color);
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

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.8s ease forwards;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero .subtitle {
                font-size: 1.2rem;
            }

            nav ul {
                gap: 1rem;
                font-size: 0.9rem;
            }

            section h2 {
                font-size: 2rem;
            }

            .timeline::before {
                left: 0;
            }

            .timeline-item {
                width: 100%;
                margin-left: 0 !important;
                text-align: left;
                padding-left: 3rem;
                padding-right: 0;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">AJ Calunia</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>A.J. L. Calunia</h1>
            <p class="subtitle">Information Systems Developer</p>
            <p class="bio">
                Curious, friendly, and determined developer passionate about learning new technologies and taking on challenges that drive growth. I believe in continuous learning, honest collaboration, and pushing beyond comfort zones to achieve excellence.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">Get In Touch</a>
                <a href="#projects" class="btn btn-secondary">View My Work</a>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2>Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>🔧 Core Technologies</h3>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>Java / Swing</span>
                            <span>70%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 70%"></div>
                        </div>
                    </div>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>SQL / MySQL</span>
                            <span>65%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 65%"></div>
                        </div>
                    </div>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>NetBeans IDE</span>
                            <span>80%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 80%"></div>
                        </div>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>💬 Soft Skills</h3>
                    <ul class="skill-list">
                        <li>Communication</li>
                        <li>Team Collaboration</li>
                        <li>Continuous Learning</li>
                        <li>Problem Solving</li>
                        <li>Time Management</li>
                        <li>Cooking</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>🎯 Hobbies & Interests</h3>
                    <ul class="skill-list">
                        <li>🏀 Basketball</li>
                        <li>🚴 Cycling</li>
                        <li>🎮 Gaming</li>
                        <li>📚 Continuous Learning</li>
                        <li>👥 Spending time with friends & family</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2>Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>🏨 Maycel Hometel IS Plan</h3>
                        <p style="font-size: 0.9rem; opacity: 0.9;">Technology Solutions</p>
                    </div>
                    <div class="project-body">
                        <p>
                            Proposing technology-based solutions to improve the operations and services of Maycel Hometel. The plan aims to enhance efficiency in managing reservations, guest records, billing, and daily administrative tasks through the implementation of an integrated information system.
                        </p>
                        <p style="margin-top: 1rem; font-size: 0.9rem;">
                            <strong>Focus:</strong> Business process optimization, data accuracy, enhanced security, and improved user experience.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education">
        <div class="container">
            <h2>Education</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Bachelor of Science in Information Systems</h3>
                        <p><strong>Davao del Norte State College</strong></p>
                        <p style="font-size: 0.9rem; color: var(--primary-color);">Currently Pursuing</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>High School Diploma - GAS Strand</h3>
                        <p><strong>Francisco Bustamante National Highschool</strong></p>
                        <p style="font-size: 0.9rem; color: var(--primary-color);">General Academic Strand</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Elementary Education</h3>
                        <p><strong>Armed Forces of the Philippines Logistics Command Elementary School</strong></p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Achievements Section -->
    <section id="achievements">
        <div class="container">
            <h2>Certifications & Awards</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>🥉 CODM BEYTE FEST Event</h3>
                    <p style="color: var(--primary-color); font-size: 1.2rem; font-weight: bold;">4th Placer</p>
                </div>
                <div class="skill-card">
                    <h3>🥈 MTV Spoof - BEYTE FEST</h3>
                    <p style="color: var(--primary-color); font-size: 1.2rem; font-weight: bold;">1st Runner Up</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2>Let's Connect</h2>
            <div class="contact-container">
                <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 2rem;">
                    I'm always open to new opportunities and collaborations. Feel free to reach out!
                </p>
                <div class="contact-info">
                    <div class="contact-item">
                        <h3 style="color: var(--primary-color); margin-bottom: 1rem;">📞 Phone</h3>
                        <a href="tel:09581881471">09581881471</a>
                    </div>
                    <div class="contact-item">
                        <h3 style="color: var(--primary-color); margin-bottom: 1rem;">📧 Email</h3>
                        <a href="mailto:ajcalunia90@gmail.com">ajcalunia90@gmail.com</a>
                    </div>
                </div>
                <div class="social-links">
                    <a href="https://www.facebook.com/aj.calunia" target="_blank" title="Facebook">f</a>
                    <a href="https://github.com/caluniaaj-code" target="_blank" title="GitHub">⌘</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 A.J. L. Calunia. All rights reserved. | Born December 3, 2006</p>
    </footer>

    <script>
        // Smooth scrolling
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

        // Animate skill bars on scroll
        const observerOptions = {
            threshold: 0.5
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.skill-card, .project-card, .timeline-item').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
