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
            --cyber-pink: #ff006e;
            --cyber-cyan: #00d4ff;
            --cyber-dark: #0a0e27;
            --cyber-darker: #050811;
            --text-primary: #ffffff;
            --text-secondary: #b0b9c6;
            --glow-cyan: rgba(0, 212, 255, 0.3);
            --glow-pink: rgba(255, 0, 110, 0.3);
        }

        body {
            font-family: 'Courier New', monospace;
            background: linear-gradient(135deg, var(--cyber-darker) 0%, var(--cyber-dark) 100%);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: repeating-linear-gradient(
                0deg,
                rgba(0, 212, 255, 0.03) 0px,
                rgba(0, 212, 255, 0.03) 1px,
                transparent 1px,
                transparent 2px
            );
            pointer-events: none;
            z-index: 1;
            animation: scanlines 8s linear infinite;
        }

        @keyframes scanlines {
            0% { transform: translateY(0); }
            100% { transform: translateY(10px); }
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(5, 8, 17, 0.95);
            backdrop-filter: blur(10px);
            padding: 1.5rem 2rem;
            z-index: 1000;
            border-bottom: 1px solid var(--cyber-cyan);
            box-shadow: 0 0 15px rgba(0, 212, 255, 0.15);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            z-index: 2;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: var(--cyber-cyan);
            text-shadow: 0 0 10px var(--glow-cyan);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            position: relative;
        }

        nav a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 1px;
            background: var(--cyber-cyan);
            transition: width 0.3s ease;
            box-shadow: 0 0 5px var(--cyber-cyan);
        }

        nav a:hover {
            color: var(--cyber-cyan);
            text-shadow: 0 0 8px var(--glow-cyan);
        }

        nav a:hover::before { width: 100%; }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            margin-top: 60px;
            position: relative;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            color: var(--cyber-cyan);
            text-shadow: 0 0 20px var(--glow-cyan);
            letter-spacing: 2px;
            animation: fadeIn 1s ease;
        }

        .hero-content .subtitle {
            font-size: 1.2rem;
            color: var(--cyber-pink);
            margin-bottom: 2rem;
            letter-spacing: 1px;
            text-transform: uppercase;
            animation: fadeIn 1.2s ease;
        }

        .hero-content .bio {
            font-size: 1rem;
            max-width: 750px;
            margin: 0 auto 3rem;
            color: var(--text-secondary);
            line-height: 1.8;
            animation: fadeIn 1.4s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeIn 1.6s ease;
        }

        .btn {
            padding: 0.8rem 2rem;
            border: 1px solid;
            border-radius: 2px;
            font-size: 0.9rem;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            font-weight: bold;
            letter-spacing: 1px;
            text-transform: uppercase;
            font-family: 'Courier New', monospace;
            transition: all 0.3s ease;
        }

        .btn-primary {
            border-color: var(--cyber-cyan);
            color: var(--cyber-cyan);
            background: rgba(0, 212, 255, 0.05);
        }

        .btn-primary:hover {
            background: rgba(0, 212, 255, 0.15);
            box-shadow: 0 0 15px var(--glow-cyan);
        }

        .btn-secondary {
            border-color: var(--cyber-pink);
            color: var(--cyber-pink);
            background: rgba(255, 0, 110, 0.05);
        }

        .btn-secondary:hover {
            background: rgba(255, 0, 110, 0.15);
            box-shadow: 0 0 15px var(--glow-pink);
        }

        section {
            padding: 6rem 0;
            position: relative;
            border-top: 1px solid rgba(0, 212, 255, 0.1);
        }

        section h2 {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            text-transform: uppercase;
            letter-spacing: 3px;
            color: var(--cyber-cyan);
            text-shadow: 0 0 15px var(--glow-cyan);
            position: relative;
            z-index: 2;
        }

        section h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--cyber-pink), transparent);
            margin: 1rem auto 0;
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            position: relative;
            z-index: 2;
        }

        .card {
            background: rgba(0, 212, 255, 0.03);
            padding: 2rem;
            border: 1px solid rgba(0, 212, 255, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, var(--cyber-cyan), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card:hover {
            background: rgba(0, 212, 255, 0.08);
            border-color: var(--cyber-cyan);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.15);
        }

        .card:hover::before { opacity: 1; }

        .card h3 {
            color: var(--cyber-pink);
            margin-bottom: 1rem;
            font-size: 1.2rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .card-content {
            position: relative;
            z-index: 2;
        }

        .list-item {
            color: var(--text-secondary);
            padding: 0.5rem 0;
            display: flex;
            align-items: center;
        }

        .list-item::before {
            content: '▸';
            color: var(--cyber-cyan);
            margin-right: 0.8rem;
        }

        .proficiency-item {
            margin-bottom: 1.5rem;
        }

        .proficiency-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .proficiency-bar {
            background: rgba(0, 212, 255, 0.1);
            height: 2px;
            border: 1px solid rgba(0, 212, 255, 0.2);
            overflow: hidden;
        }

        .proficiency-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink));
            box-shadow: 0 0 8px var(--cyber-cyan);
            animation: widthAnimation 1s ease forwards;
        }

        @keyframes widthAnimation {
            from { width: 0; }
        }

        .project-card {
            background: rgba(0, 212, 255, 0.03);
            padding: 2.5rem;
            border: 1px solid rgba(0, 212, 255, 0.2);
            transition: all 0.3s ease;
            position: relative;
            z-index: 2;
        }

        .project-card:hover {
            background: rgba(0, 212, 255, 0.08);
            border-color: var(--cyber-cyan);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.15);
        }

        .project-card h3 {
            color: var(--cyber-cyan);
            margin-bottom: 1rem;
            font-size: 1.3rem;
            text-transform: uppercase;
            text-shadow: 0 0 10px var(--glow-cyan);
        }

        .project-card p {
            color: var(--text-secondary);
            line-height: 1.8;
            margin-bottom: 1rem;
        }

        .timeline {
            position: relative;
            padding: 2rem 0;
        }

        .timeline-item {
            margin-bottom: 2.5rem;
            padding-left: 2rem;
            position: relative;
            z-index: 2;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 1px;
            height: 100%;
            background: linear-gradient(180deg, var(--cyber-cyan), transparent);
            box-shadow: 0 0 10px rgba(0, 212, 255, 0.2);
        }

        .timeline-dot {
            position: absolute;
            left: -8px;
            top: 0;
            width: 15px;
            height: 15px;
            background: var(--cyber-pink);
            border: 2px solid var(--cyber-cyan);
            border-radius: 50%;
            box-shadow: 0 0 10px var(--glow-pink);
        }

        .timeline-item h3 {
            color: var(--cyber-cyan);
            margin-bottom: 0.3rem;
            font-size: 1.1rem;
            text-transform: uppercase;
        }

        .timeline-item p {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            position: relative;
            z-index: 2;
        }

        .contact-card {
            background: rgba(0, 212, 255, 0.03);
            padding: 2rem;
            border: 1px solid rgba(0, 212, 255, 0.2);
            text-align: center;
            transition: all 0.3s ease;
        }

        .contact-card:hover {
            background: rgba(0, 212, 255, 0.08);
            border-color: var(--cyber-cyan);
            box-shadow: 0 0 15px rgba(0, 212, 255, 0.15);
        }

        .contact-card h3 {
            color: var(--cyber-pink);
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            font-size: 0.95rem;
        }

        .contact-card a {
            color: var(--cyber-cyan);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .contact-card a:hover {
            text-shadow: 0 0 10px var(--glow-cyan);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
            position: relative;
            z-index: 2;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: rgba(0, 212, 255, 0.08);
            border: 1px solid var(--cyber-cyan);
            color: var(--cyber-cyan);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.3rem;
        }

        .social-links a:hover {
            background: rgba(0, 212, 255, 0.2);
            box-shadow: 0 0 15px var(--glow-cyan);
        }

        footer {
            background: rgba(5, 8, 17, 0.98);
            padding: 2rem;
            text-align: center;
            color: var(--text-secondary);
            border-top: 1px solid rgba(0, 212, 255, 0.1);
            font-size: 0.85rem;
            letter-spacing: 1px;
            position: relative;
            z-index: 2;
        }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 2.5rem; }
            section h2 { font-size: 2rem; }
            nav ul { gap: 1rem; font-size: 0.85rem; }
            .cta-buttons { flex-direction: column; }
            .btn { width: 100%; }
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <div class="logo">> aj.calunia</div>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#hobbies">Hobbies</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <h1>> A.J. L. Calunia</h1>
            <p class="subtitle">[ Information Systems Developer ]</p>
            <p class="bio">
                Hello! My name is A.J. L. Calunia, and I was born on December 3, 2006. I am a curious, friendly, and determined person who enjoys learning new things and taking on challenges that help me grow. I value honesty, respect, and perseverance, and I strive to maintain a positive attitude in everything I do. In my free time, I enjoy playing sports, gaming, spending time with friends and family, and exploring topics that interest me. I believe that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone, and I am always looking for opportunities to improve myself and discover new interests.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">[ Get In Touch ]</a>
                <a href="#projects" class="btn btn-secondary">[ View Work ]</a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2>About</h2>
            <div class="content-grid">
                <div class="card">
                    <div class="card-content">
                        <p style="line-height: 1.8; color: var(--text-secondary);">
                            I am someone who believes that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone. I am always looking for opportunities to improve myself and discover new interests. My approach to life is driven by curiosity and a determination to make a meaningful impact through technology and personal excellence.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="hobbies">
        <div class="container">
            <h2>Hobbies & Sports</h2>
            <div class="content-grid">
                <div class="card">
                    <h3>🏀 Basketball</h3>
                    <div class="card-content">
                        <p style="color: var(--text-secondary);">Passionate player and enthusiast. Basketball keeps me sharp, connected with the community, and maintains my competitive spirit.</p>
                    </div>
                </div>
                <div class="card">
                    <h3>🚴 Cycling</h3>
                    <div class="card-content">
                        <p style="color: var(--text-secondary);">Explorer of roads and trails. Cycling is my escape, my meditation, and my way to stay active and healthy.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2>Technical & Soft Skills</h2>
            <div class="content-grid">
                <div class="card">
                    <h3>⚙️ Technical Skills</h3>
                    <div class="card-content">
                        <div class="proficiency-item">
                            <div class="proficiency-label">
                                <span>Java / Swing</span>
                                <span>70%</span>
                            </div>
                            <div class="proficiency-bar">
                                <div class="proficiency-fill" style="width: 70%;"></div>
                            </div>
                        </div>
                        <div class="proficiency-item">
                            <div class="proficiency-label">
                                <span>SQL / MySQL</span>
                                <span>65%</span>
                            </div>
                            <div class="proficiency-bar">
                                <div class="proficiency-fill" style="width: 65%;"></div>
                            </div>
                        </div>
                        <div class="proficiency-item">
                            <div class="proficiency-label">
                                <span>NetBeans IDE</span>
                                <span>80%</span>
                            </div>
                            <div class="proficiency-bar">
                                <div class="proficiency-fill" style="width: 80%;"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <h3>💬 Soft Skills</h3>
                    <div class="card-content">
                        <div class="list-item">Communication</div>
                        <div class="list-item">Cooking</div>
                        <div class="list-item">Team Collaboration</div>
                        <div class="list-item">Continuous Learning</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2>Projects</h2>
            <div class="project-card">
                <h3>🏨 Information Systems Technological Plan for Maycel Hometel</h3>
                <p>
                    <strong>Description:</strong> Proposing technology-based solutions to improve the operations and services of Maycel Hometel. The plan aims to enhance efficiency in managing reservations, guest records, billing, and daily administrative tasks through the implementation of an integrated information system.
                </p>
                <p>
                    By utilizing modern technologies and digital tools, the project seeks to streamline business processes, improve data accuracy, strengthen security, and provide a better overall experience for both management and guests. The proposed system supports informed decision-making and helps the establishment adapt to the growing demands of the hospitality industry.
                </p>
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container">
            <h2>Education</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h3>Bachelor of Science in Information Systems (BSIS)</h3>
                    <p><strong>Davao del Norte State College</strong> | Currently Pursuing</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h3>High School - GAS Strand</h3>
                    <p><strong>Francisco Bustamante National Highschool</strong> | Completed</p>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <h3>Elementary Education</h3>
                    <p><strong>Armed Forces of the Philippines Logistics Command Elementary School</strong> | Completed</p>
                </div>
            </div>
        </div>
    </section>

    <section id="achievements">
        <div class="container">
            <h2>Certifications & Awards</h2>
            <div class="content-grid">
                <div class="card">
                    <h3>4️CODM Competition</h3>
                    <div class="card-content">
                        <p style="color: var(--cyber-cyan); font-size: 1.2rem; font-weight: bold;">4TH PLACER</p>
                        <p style="color: var(--text-secondary); margin-top: 0.5rem; font-size: 0.9rem;">BEYTE FEST EVENT</p>
                    </div>
                </div>
                <div class="card">
                    <h3>MTV Spoof</h3>
                    <div class="card-content">
                        <p style="color: var(--cyber-cyan); font-size: 1.2rem; font-weight: bold;">1ST RUNNER UP</p>
                        <p style="color: var(--text-secondary); margin-top: 0.5rem; font-size: 0.9rem;">BEYTE FEST EVENT</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2>Work Experience</h2>
            <div class="content-grid">
                <div class="card">
                    <h3>🚚 Delivery & Catering</h3>
                    <div class="card-content">
                        <p style="color: var(--text-secondary);">Professional experience in delivery and catering operations. Managed customer orders, ensured timely service delivery, and maintained high standards of customer satisfaction. This experience developed my organizational, communication, and time management skills.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Get In Touch</h2>
            <div class="contact-info">
                <div class="contact-card">
                    <h3>📞 Phone</h3>
                    <a href="tel:09581881471">09581881471</a>
                </div>
                <div class="contact-card">
                    <h3>📧 Email</h3>
                    <a href="mailto:ajcalunia90@gmail.com">ajcalunia90@gmail.com</a>
                </div>
                <div class="contact-card">
                    <h3>👤 Facebook</h3>
                    <a href="https://www.facebook.com/aj.calunia" target="_blank">aj.calunia</a>
                </div>
            </div>
            <div class="social-links">
                <a href="https://www.facebook.com/aj.calunia" target="_blank" title="Facebook">f</a>
                <a href="https://github.com/caluniaaj-code" target="_blank" title="GitHub">⌘</a>
            </div>
        </div>
    </section>

    <footer>
        <p>© 2026 A.J. L. CALUNIA | BORN: 03.12.2006 | SYSTEM STATUS: OPERATIONAL</p>
    </footer>

    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
