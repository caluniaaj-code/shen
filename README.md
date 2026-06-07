<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A.J. L. Calunia - Cyberpunk Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --cyber-pink: #ff006e;
            --cyber-cyan: #00d4ff;
            --cyber-purple: #b60aff;
            --cyber-dark: #0a0e27;
            --cyber-darker: #050811;
            --neon-green: #39ff14;
            --neon-orange: #ff6600;
            --text-primary: #ffffff;
            --text-secondary: #b0b9c6;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Courier New', monospace;
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated Gradient Background */
        body {
            background: linear-gradient(-45deg, #ff006e, #00d4ff, #b60aff, #39ff14, #ff6600, #ff006e);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
            min-height: 100vh;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Overlay for content readability */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(ellipse at center, rgba(10, 14, 39, 0.85) 0%, rgba(5, 8, 17, 0.95) 100%);
            pointer-events: none;
            z-index: 1;
            animation: pulseOverlay 8s ease-in-out infinite;
        }

        @keyframes pulseOverlay {
            0%, 100% { opacity: 0.92; }
            50% { opacity: 0.88; }
        }

        /* Animated Grid Effect */
        body::after {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 212, 255, 0.05) 25%, rgba(0, 212, 255, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 212, 255, 0.05) 75%, rgba(0, 212, 255, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 212, 255, 0.05) 25%, rgba(0, 212, 255, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 212, 255, 0.05) 75%, rgba(0, 212, 255, 0.05) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
            pointer-events: none;
            z-index: 1;
            animation: gridFloat 20s linear infinite;
        }

        @keyframes gridFloat {
            0% { transform: translateY(0); }
            100% { transform: translateY(50px); }
        }

        /* Floating particles effect */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 1;
            pointer-events: none;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: rgba(0, 212, 255, 0.6);
            border-radius: 50%;
            animation: float-up 20s infinite linear;
        }

        @keyframes float-up {
            0% {
                opacity: 0;
                transform: translateY(0) translateX(0);
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                opacity: 0;
                transform: translateY(-100vh) translateX(100px);
            }
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(5, 8, 17, 0.98);
            backdrop-filter: blur(10px);
            padding: 1.5rem 2rem;
            z-index: 1000;
            border-bottom: 2px solid var(--cyber-cyan);
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.4);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 3px;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { filter: drop-shadow(0 0 10px rgba(0, 212, 255, 0.5)); }
            50% { filter: drop-shadow(0 0 20px rgba(255, 0, 110, 0.5)); }
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        nav a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 0.95rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            position: relative;
        }

        nav a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-orange));
            transition: width 0.3s ease;
            box-shadow: 0 0 10px var(--cyber-cyan);
        }

        nav a:hover {
            color: var(--cyber-cyan);
            text-shadow: 0 0 15px rgba(0, 212, 255, 0.8);
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
            z-index: 2;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-orange), var(--neon-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 3px;
            animation: fadeIn 1s ease, float 3s ease-in-out infinite;
            text-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .hero-content .subtitle {
            font-size: 1.4rem;
            color: var(--neon-orange);
            margin-bottom: 2rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            animation: fadeIn 1.2s ease;
            text-shadow: 0 0 20px rgba(255, 102, 0, 0.6);
        }

        .hero-content .bio {
            font-size: 1.05rem;
            max-width: 750px;
            margin: 0 auto 3rem;
            color: var(--text-secondary);
            line-height: 1.8;
            animation: fadeIn 1.4s ease;
            background: rgba(0, 212, 255, 0.08);
            padding: 2rem;
            border-left: 3px solid var(--cyber-cyan);
            border-right: 3px solid var(--cyber-pink);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.15);
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeIn 1.6s ease;
        }

        .btn {
            padding: 1rem 2.5rem;
            border: 2px solid;
            border-radius: 4px;
            font-size: 1rem;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            font-weight: bold;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-family: 'Courier New', monospace;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: radial-gradient(circle, rgba(255, 255, 255, 0.2), transparent);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }

        .btn:hover::before {
            width: 300px;
            height: 300px;
        }

        .btn-primary {
            border-color: var(--cyber-cyan);
            color: var(--cyber-cyan);
            background: rgba(0, 212, 255, 0.1);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.3);
        }

        .btn-primary:hover {
            background: rgba(0, 212, 255, 0.25);
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.6);
            transform: translateY(-3px);
        }

        .btn-secondary {
            border-color: var(--cyber-pink);
            color: var(--cyber-pink);
            background: rgba(255, 0, 110, 0.1);
            box-shadow: 0 0 20px rgba(255, 0, 110, 0.3);
        }

        .btn-secondary:hover {
            background: rgba(255, 0, 110, 0.25);
            box-shadow: 0 0 40px rgba(255, 0, 110, 0.6);
            transform: translateY(-3px);
        }

        section {
            padding: 6rem 0;
            position: relative;
            z-index: 2;
            border-top: 1px solid rgba(0, 212, 255, 0.2);
        }

        section h2 {
            font-size: 2.8rem;
            margin-bottom: 3rem;
            text-align: center;
            text-transform: uppercase;
            letter-spacing: 4px;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 30px rgba(0, 212, 255, 0.4);
            position: relative;
        }

        section h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--cyber-pink), var(--cyber-cyan), transparent);
            margin: 1.5rem auto 0;
            box-shadow: 0 0 15px var(--cyber-cyan);
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .card {
            background: rgba(10, 14, 39, 0.8);
            padding: 2.5rem;
            border: 2px solid var(--cyber-cyan);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 212, 255, 0.3), transparent);
            transition: left 0.5s ease;
            z-index: 0;
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: var(--neon-orange);
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.4), 0 0 20px rgba(255, 102, 0, 0.3);
        }

        .card:hover::before { left: 100%; }

        .card h3 {
            color: var(--neon-orange);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
            z-index: 1;
            text-shadow: 0 0 15px rgba(255, 102, 0, 0.5);
        }

        .card-content {
            position: relative;
            z-index: 1;
        }

        .list-item {
            color: var(--text-secondary);
            padding: 0.7rem 0;
            display: flex;
            align-items: center;
        }

        .list-item::before {
            content: '▸';
            color: var(--cyber-cyan);
            margin-right: 1rem;
            font-size: 1.3rem;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .proficiency-item {
            margin-bottom: 1.8rem;
        }

        .proficiency-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.7rem;
            font-size: 0.95rem;
            color: var(--text-secondary);
        }

        .proficiency-bar {
            background: rgba(0, 212, 255, 0.15);
            height: 3px;
            border: 1px solid rgba(0, 212, 255, 0.4);
            overflow: hidden;
            border-radius: 10px;
            box-shadow: inset 0 0 10px rgba(0, 212, 255, 0.2);
        }

        .proficiency-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-orange));
            box-shadow: 0 0 15px var(--cyber-cyan);
            animation: widthAnimation 1.5s ease forwards;
        }

        @keyframes widthAnimation {
            from { width: 0; }
        }

        .project-card {
            background: rgba(10, 14, 39, 0.8);
            padding: 3rem;
            border: 2px solid var(--cyber-cyan);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 102, 0, 0.2), transparent);
            transition: left 0.5s ease;
            z-index: 0;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: var(--neon-orange);
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.4), 0 0 20px rgba(255, 102, 0, 0.3);
        }

        .project-card:hover::before { left: 100%; }

        .project-card h3 {
            color: var(--cyber-cyan);
            margin-bottom: 1.5rem;
            font-size: 1.4rem;
            text-transform: uppercase;
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
            position: relative;
            z-index: 1;
        }

        .project-card p {
            color: var(--text-secondary);
            line-height: 1.9;
            margin-bottom: 1.2rem;
            position: relative;
            z-index: 1;
        }

        .timeline {
            position: relative;
            padding: 2rem 0;
        }

        .timeline-item {
            margin-bottom: 3rem;
            padding-left: 2.5rem;
            position: relative;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 2px;
            height: 100%;
            background: linear-gradient(180deg, var(--cyber-cyan), var(--cyber-pink), transparent);
            box-shadow: 0 0 15px rgba(0, 212, 255, 0.4);
        }

        .timeline-dot {
            position: absolute;
            left: -12px;
            top: 0;
            width: 20px;
            height: 20px;
            background: var(--neon-orange);
            border: 3px solid var(--cyber-cyan);
            border-radius: 50%;
            box-shadow: 0 0 20px var(--neon-orange), 0 0 40px rgba(0, 212, 255, 0.4);
            animation: pulse-dot 2s ease-in-out infinite;
        }

        @keyframes pulse-dot {
            0%, 100% { box-shadow: 0 0 20px var(--neon-orange), 0 0 40px rgba(0, 212, 255, 0.4); }
            50% { box-shadow: 0 0 30px var(--neon-orange), 0 0 60px rgba(0, 212, 255, 0.6); }
        }

        .timeline-item h3 {
            color: var(--cyber-cyan);
            margin-bottom: 0.5rem;
            font-size: 1.2rem;
            text-transform: uppercase;
            text-shadow: 0 0 10px rgba(0, 212, 255, 0.4);
        }

        .timeline-item p {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 2rem;
        }

        .contact-card {
            background: rgba(10, 14, 39, 0.8);
            padding: 2.5rem;
            border: 2px solid var(--cyber-cyan);
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        .contact-card:hover {
            transform: translateY(-8px);
            border-color: var(--neon-orange);
            box-shadow: 0 0 40px rgba(0, 212, 255, 0.4), 0 0 20px rgba(255, 102, 0, 0.3);
        }

        .contact-card h3 {
            color: var(--neon-orange);
            margin-bottom: 1rem;
            text-transform: uppercase;
            font-size: 1rem;
            text-shadow: 0 0 10px rgba(255, 102, 0, 0.5);
        }

        .contact-card a {
            color: var(--cyber-cyan);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .contact-card a:hover {
            text-shadow: 0 0 15px rgba(0, 212, 255, 0.8);
            color: var(--neon-orange);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 3rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background: rgba(0, 212, 255, 0.1);
            border: 2px solid var(--cyber-cyan);
            color: var(--cyber-cyan);
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.5rem;
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        .social-links a:hover {
            background: rgba(255, 102, 0, 0.2);
            border-color: var(--neon-orange);
            color: var(--neon-orange);
            box-shadow: 0 0 30px rgba(255, 102, 0, 0.5);
            transform: scale(1.1);
        }

        footer {
            background: rgba(5, 8, 17, 0.98);
            padding: 2.5rem;
            text-align: center;
            color: var(--text-secondary);
            border-top: 2px solid var(--cyber-cyan);
            font-size: 0.9rem;
            letter-spacing: 2px;
            position: relative;
            z-index: 2;
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.2);
        }

        @media (max-width: 768px) {
            .hero-content h1 { font-size: 2.5rem; }
            section h2 { font-size: 2rem; }
            nav ul { gap: 1rem; font-size: 0.85rem; }
            .cta-buttons { flex-direction: column; }
            .btn { width: 100%; }
            .card { padding: 1.5rem; }
            .project-card { padding: 1.5rem; }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>

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
            <h1>> A.J. L. CALUNIA</h1>
            <p class="subtitle">[ Information Systems Developer ]</p>
            <p class="bio">
                Hello! My name is A.J. L. Calunia, and I was born on December 3, 2006. I am a curious, friendly, and determined person who enjoys learning new things and taking on challenges that help me grow. I value honesty, respect, and perseverance, and I strive to maintain a positive attitude in everything I do. In my free time, I enjoy playing sports, gaming, spending time with friends and family, and exploring topics that interest me. I believe that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">[ Get In Touch ]</a>
                <a href="#projects" class="btn btn-secondary">[ View Work ]</a>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <div class="content-grid">
                <div class="card">
                    <div class="card-content">
                        <p style="line-height: 1.9; color: var(--text-secondary);">
                            I am someone who believes that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone. I am always looking for opportunities to improve myself and discover new interests. My passion drives me to create innovative solutions and achieve excellence in everything I do.
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
                    <h3>CODM Competition</h3>
                    <div class="card-content">
                        <p style="color: var(--cyber-cyan); font-size: 1.3rem; font-weight: bold;">4TH PLACER</p>
                        <p style="color: var(--text-secondary); margin-top: 0.8rem; font-size: 0.95rem;">BEYTE FEST EVENT</p>
                    </div>
                </div>
                <div class="card">
                    <h3>MTV Spoof</h3>
                    <div class="card-content">
                        <p style="color: var(--cyber-cyan); font-size: 1.3rem; font-weight: bold;">1ST RUNNER UP</p>
                        <p style="color: var(--text-secondary); margin-top: 0.8rem; font-size: 0.95rem;">BEYTE FEST EVENT</p>
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
        // Create floating particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 20 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 20) + 's';
            particlesContainer.appendChild(particle);
        }

        // Smooth scroll
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
