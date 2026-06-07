<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A.J. L. Calunia - Cyber Portfolio</title>
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
            --neon-blue: #0099ff;
            --text-primary: #ffffff;
            --text-secondary: #b0b9c6;
            --glow-pink: rgba(255, 0, 110, 0.3);
            --glow-cyan: rgba(0, 212, 255, 0.3);
        }

        body {
            font-family: 'Courier New', 'Courier', monospace;
            background: linear-gradient(135deg, var(--cyber-darker) 0%, var(--cyber-dark) 50%, #1a1f4d 100%);
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
            background: 
                repeating-linear-gradient(
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
            border-bottom: 2px solid var(--cyber-cyan);
            box-shadow: 0 0 20px rgba(0, 212, 255, 0.2);
        }

        nav::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(0, 212, 255, 0.05), transparent);
            pointer-events: none;
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
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 3px;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow-text 2s ease-in-out infinite;
        }

        @keyframes glow-text {
            0%, 100% { text-shadow: 0 0 20px var(--glow-cyan); }
            50% { text-shadow: 0 0 30px var(--glow-cyan), 0 0 40px var(--glow-pink); }
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
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink));
            transition: width 0.3s ease;
            box-shadow: 0 0 10px var(--cyber-cyan);
        }

        nav a:hover {
            color: var(--cyber-cyan);
            text-shadow: 0 0 10px var(--cyber-cyan);
        }

        nav a:hover::before { width: 100%; }

        .container {
            max-width: 1200px;
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
            margin-top: 80px;
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
            background: 
                radial-gradient(circle at 20% 50%, rgba(0, 212, 255, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(255, 0, 110, 0.15) 0%, transparent 50%);
            z-index: 0;
        }

        .hero::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 35px,
                rgba(0, 212, 255, 0.03) 35px,
                rgba(0, 212, 255, 0.03) 70px
            );
            animation: drift 20s linear infinite;
        }

        @keyframes drift {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .hero-content {
            z-index: 2;
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 5rem;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 4px;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glitch 3s ease-in-out infinite;
        }

        @keyframes glitch {
            0% { text-shadow: 2px 2px var(--cyber-cyan), -2px -2px var(--cyber-pink); }
            50% { text-shadow: -2px 2px var(--cyber-pink), 2px -2px var(--cyber-cyan); }
            100% { text-shadow: 2px 2px var(--cyber-cyan), -2px -2px var(--cyber-pink); }
        }

        .hero .subtitle {
            font-size: 1.8rem;
            color: var(--cyber-cyan);
            margin-bottom: 1.5rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            text-shadow: 0 0 20px var(--glow-cyan), 0 0 40px var(--glow-cyan);
        }

        .hero .bio {
            font-size: 1.1rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            color: var(--text-secondary);
            line-height: 1.9;
            padding: 2rem;
            border-left: 3px solid var(--cyber-pink);
            border-right: 3px solid var(--cyber-cyan);
            background: rgba(0, 212, 255, 0.05);
            box-shadow: 
                inset 0 0 20px rgba(0, 212, 255, 0.1),
                0 0 30px rgba(0, 212, 255, 0.2);
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border: 2px solid;
            border-radius: 0;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            font-weight: bold;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-family: 'Courier New', monospace;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .btn:hover::before { left: 100%; }

        .btn-primary {
            border-color: var(--cyber-cyan);
            color: var(--cyber-cyan);
            background: rgba(0, 212, 255, 0.1);
            box-shadow: 0 0 20px var(--glow-cyan), inset 0 0 20px rgba(0, 212, 255, 0.1);
        }

        .btn-primary:hover {
            background: rgba(0, 212, 255, 0.3);
            box-shadow: 0 0 40px var(--glow-cyan), inset 0 0 30px rgba(0, 212, 255, 0.2);
            transform: translateY(-3px);
        }

        .btn-secondary {
            border-color: var(--cyber-pink);
            color: var(--cyber-pink);
            background: rgba(255, 0, 110, 0.1);
            box-shadow: 0 0 20px var(--glow-pink), inset 0 0 20px rgba(255, 0, 110, 0.1);
        }

        .btn-secondary:hover {
            background: rgba(255, 0, 110, 0.3);
            box-shadow: 0 0 40px var(--glow-pink), inset 0 0 30px rgba(255, 0, 110, 0.2);
            transform: translateY(-3px);
        }

        section {
            padding: 8rem 0;
            position: relative;
            border-top: 1px solid rgba(0, 212, 255, 0.2);
        }

        section::before {
            content: attr(data-title);
            position: absolute;
            top: 20px;
            left: 0;
            opacity: 0.1;
            font-size: 4rem;
            text-transform: uppercase;
            letter-spacing: 10px;
            color: var(--cyber-cyan);
            pointer-events: none;
            z-index: 1;
        }

        section h2 {
            font-size: 3.5rem;
            margin-bottom: 4rem;
            text-align: center;
            text-transform: uppercase;
            letter-spacing: 4px;
            color: var(--cyber-cyan);
            position: relative;
            z-index: 2;
            text-shadow: 0 0 30px var(--glow-cyan), 0 0 60px rgba(255, 0, 110, 0.3);
        }

        section h2::before,
        section h2::after {
            content: '◆';
            color: var(--cyber-pink);
            margin: 0 1rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            position: relative;
            z-index: 2;
        }

        .skill-card {
            background: rgba(0, 212, 255, 0.05);
            padding: 2.5rem;
            border: 2px solid;
            border-image: linear-gradient(135deg, var(--cyber-cyan), var(--cyber-pink)) 1;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .skill-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(255, 0, 110, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 1;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 40px var(--glow-cyan), 0 0 60px var(--glow-pink);
            border-image: linear-gradient(135deg, var(--cyber-pink), var(--cyber-cyan)) 1;
        }

        .skill-card:hover::before { opacity: 1; }

        .skill-card > * {
            position: relative;
            z-index: 2;
        }

        .skill-card h3 {
            color: var(--cyber-pink);
            margin-bottom: 1.5rem;
            font-size: 1.4rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 0.7rem 0;
            display: flex;
            align-items: center;
            color: var(--text-secondary);
            position: relative;
            z-index: 2;
        }

        .skill-list li::before {
            content: '▸';
            color: var(--cyber-cyan);
            margin-right: 1rem;
            font-size: 1.2rem;
            animation: pulse 1.5s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .proficiency-item {
            margin-bottom: 2rem;
        }

        .proficiency-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.8rem;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .proficiency-header span:first-child {
            color: var(--cyber-cyan);
        }

        .proficiency-header span:last-child {
            color: var(--cyber-pink);
        }

        .proficiency-bar {
            background: rgba(0, 212, 255, 0.1);
            height: 4px;
            border: 1px solid var(--cyber-cyan);
            box-shadow: inset 0 0 10px rgba(0, 212, 255, 0.2);
            overflow: hidden;
        }

        .proficiency-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink), var(--neon-green));
            box-shadow: 0 0 10px var(--cyber-cyan), inset 0 0 10px rgba(0, 212, 255, 0.5);
            animation: fillBar 0.8s ease forwards;
        }

        @keyframes fillBar {
            from { width: 0; }
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            position: relative;
            z-index: 2;
        }

        .project-card {
            background: rgba(0, 212, 255, 0.05);
            border: 2px solid var(--cyber-cyan);
            overflow: hidden;
            transition: all 0.3s ease;
            position: relative;
        }

        .project-card::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(255, 0, 110, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease;
            pointer-events: none;
        }

        .project-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 0 50px var(--glow-cyan), 0 0 80px var(--glow-pink);
            border-color: var(--cyber-pink);
        }

        .project-card:hover::after { opacity: 1; }

        .project-header {
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.2), rgba(255, 0, 110, 0.2));
            padding: 2.5rem;
            border-bottom: 2px solid var(--cyber-pink);
            position: relative;
            z-index: 2;
        }

        .project-header h3 {
            font-size: 1.6rem;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--cyber-cyan);
            text-shadow: 0 0 15px var(--glow-cyan);
        }

        .project-body {
            padding: 2.5rem;
            position: relative;
            z-index: 2;
        }

        .project-body p {
            color: var(--text-secondary);
            line-height: 1.9;
        }

        .timeline {
            position: relative;
            padding: 3rem 0;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: linear-gradient(180deg, var(--cyber-cyan), var(--cyber-pink));
            box-shadow: 0 0 20px var(--cyber-cyan);
        }

        .timeline-item {
            margin-bottom: 4rem;
            width: 45%;
            position: relative;
            z-index: 2;
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

        .timeline-dot {
            position: absolute;
            width: 20px;
            height: 20px;
            background: var(--cyber-pink);
            border: 2px solid var(--cyber-cyan);
            border-radius: 50%;
            top: 0;
            right: -45px;
            box-shadow: 0 0 15px var(--cyber-pink), 0 0 25px var(--cyber-cyan);
        }

        .timeline-item:nth-child(even) .timeline-dot {
            left: -45px;
            right: auto;
        }

        .timeline-content {
            background: rgba(0, 212, 255, 0.08);
            padding: 2rem;
            border: 2px solid var(--cyber-cyan);
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.2);
            transition: all 0.3s ease;
        }

        .timeline-item:hover .timeline-content {
            box-shadow: 0 0 50px var(--glow-cyan), 0 0 70px var(--glow-pink);
            border-color: var(--cyber-pink);
        }

        .timeline-content h3 {
            color: var(--cyber-pink);
            margin-bottom: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .timeline-content p {
            color: var(--text-secondary);
        }

        .contact-container {
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 2;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .contact-item {
            background: rgba(0, 212, 255, 0.08);
            padding: 2.5rem;
            border: 2px solid var(--cyber-cyan);
            transition: all 0.3s ease;
            position: relative;
        }

        .contact-item:hover {
            box-shadow: 0 0 40px var(--glow-cyan), 0 0 60px var(--glow-pink);
            border-color: var(--cyber-pink);
            transform: translateY(-5px);
        }

        .contact-item h3 {
            color: var(--cyber-cyan);
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .contact-item a {
            color: var(--cyber-pink);
            text-decoration: none;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .contact-item a:hover {
            color: var(--cyber-cyan);
            text-shadow: 0 0 15px var(--cyber-cyan);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2.5rem;
            margin: 3rem 0;
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
            position: relative;
            overflow: hidden;
        }

        .social-links a::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, var(--cyber-cyan), var(--cyber-pink));
            transition: left 0.3s ease;
            z-index: 1;
        }

        .social-links a:hover::before { left: 100%; }

        .social-links a:hover {
            border-color: var(--cyber-pink);
            box-shadow: 0 0 30px var(--glow-cyan), 0 0 40px var(--glow-pink);
        }

        .social-links a span {
            position: relative;
            z-index: 2;
        }

        footer {
            background: rgba(5, 8, 17, 0.98);
            padding: 2rem;
            text-align: center;
            color: var(--text-secondary);
            border-top: 2px solid var(--cyber-cyan);
            position: relative;
            z-index: 2;
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.1);
        }

        footer p {
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 3rem; }
            .hero .subtitle { font-size: 1.4rem; }
            nav ul { gap: 1rem; font-size: 0.85rem; }
            section h2 { font-size: 2.5rem; }
            .timeline::before { left: 0; }
            .timeline-item {
                width: 100%;
                margin-left: 0 !important;
                text-align: left;
                padding-left: 3rem;
                padding-right: 0;
            }
            .timeline-dot { left: -45px; right: auto; }
            .timeline-item:nth-child(odd) {
                text-align: left;
                padding-right: 0;
                padding-left: 3rem;
            }
            .cta-buttons { flex-direction: column; }
            .btn { width: 100%; }
            section h2::before,
            section h2::after { display: none; }
        }

        .glitch-element { animation: glitch-entrance 0.6s ease-out; }

        @keyframes glitch-entrance {
            0% {
                opacity: 0;
                transform: translate(0, 20px) skewX(10deg);
            }
            50% {
                opacity: 0.5;
                transform: translate(-5px, 10px) skewX(-5deg);
            }
            100% {
                opacity: 1;
                transform: translate(0, 0) skewX(0);
            }
        }

        .work-section {
            background: rgba(0, 212, 255, 0.05);
            padding: 2.5rem;
            border: 2px solid var(--cyber-cyan);
            margin: 2rem 0;
            border-radius: 4px;
            position: relative;
            z-index: 2;
        }

        .work-section h4 {
            color: var(--cyber-pink);
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .work-section p {
            color: var(--text-secondary);
            line-height: 1.8;
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <div class="logo">> aj.calunia</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>> A.J. L. CALUNIA</h1>
            <p class="subtitle">[ INFORMATION SYSTEMS DEVELOPER ]</p>
            <p class="bio">
                Born December 3, 2006. Curious, friendly, and determined developer passionate about cutting-edge technology and computational excellence. I value honesty, respect, and perseverance in everything I do. Always seeking personal growth through continuous learning and stepping outside my comfort zone.
            </p>
            <div class="cta-buttons">
                <a href="#contact" class="btn btn-primary">[ INITIATE CONNECTION ]</a>
                <a href="#projects" class="btn btn-secondary">[ VIEW OPERATIONS ]</a>
            </div>
        </div>
    </section>

    <section id="about" data-title="ABOUT">
        <div class="container">
            <h2>WHO I AM</h2>
            <div class="work-section">
                <h4>🎯 CORE PHILOSOPHY</h4>
                <p>
                    I'm a curious, friendly, and determined person who enjoys learning new things and taking on challenges that help me grow. I believe that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone. I am always looking for opportunities to improve myself and discover new interests. In my free time, I enjoy playing sports, gaming, spending time with friends and family, and exploring topics that fascinate me.
                </p>
            </div>
            <div class="work-section">
                <h4>🏀 HOBBIES & INTERESTS</h4>
                <p>
                    Basketball enthusiast & cycling explorer. I believe that staying active and connected keeps the mind sharp and the spirit high. When I'm not coding, you'll find me on the court or on the road.
                </p>
            </div>
        </div>
    </section>

    <section id="skills" data-title="SKILLS">
        <div class="container">
            <h2>Technical Arsenal</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>⚙️ PROGRAMMING</h3>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>Java / Swing</span>
                            <span>70%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 70%;"></div>
                        </div>
                    </div>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>SQL / MySQL</span>
                            <span>65%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 65%;"></div>
                        </div>
                    </div>
                    <div class="proficiency-item">
                        <div class="proficiency-header">
                            <span>NetBeans IDE</span>
                            <span>80%</span>
                        </div>
                        <div class="proficiency-bar">
                            <div class="proficiency-fill" style="width: 80%;"></div>
                        </div>
                    </div>
                </div>

                <div class="skill-card">
                    <h3>💬 SOFT SKILLS</h3>
                    <ul class="skill-list">
                        <li>Communication Excellence</li>
                        <li>Team Collaboration</li>
                        <li>Time Management</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <h3>🎮 LEISURE PROTOCOLS</h3>
                    <ul class="skill-list">
                        <li>🏀 Basketball Excellence</li>
                        <li>🚴 Cycling Adventures</li>
                        <li>🎮 Gaming Mastery</li>
                        <li>📚 Knowledge Expansion</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" data-title="PROJECTS">
        <div class="container">
            <h2>Operational Deployments</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>🏨 MAYCEL HOMETEL IS</h3>
                        <p style="font-size: 0.85rem; opacity: 0.85; letter-spacing: 1px; text-transform: uppercase;">
                            [ HOSPITALITY SYSTEMS INTEGRATION ]
                        </p>
                    </div>
                    <div class="project-body">
                        <p>
                            <strong>Description:</strong> Proposing comprehensive technology-based solutions to revolutionize Maycel Hometel operations and guest services.
                        </p>
                        <p style="margin-top: 1rem;">
                            <strong>Objectives:</strong> Enhance efficiency in managing reservations, guest records, billing, and daily administrative tasks through an integrated information system utilizing modern technologies and digital tools.
                        </p>
                        <p style="margin-top: 1rem; color: var(--cyber-cyan);">
                            <strong>>> KEY_OUTCOMES:</strong> Streamlined business processes, improved data accuracy, strengthened security, enhanced user experience, informed decision-making support, and successful adaptation to growing hospitality industry demands.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="education" data-title="EDUCATION">
        <div class="container">
            <h2>Academic Background</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <h3>> BACHELOR OF SCIENCE IN INFORMATION SYSTEMS</h3>
                        <p><strong>Davao del Norte State College</strong></p>
                        <p style="font-size: 0.85rem; color: var(--cyber-cyan); margin-top: 0.5rem;">
                            [ BSIS ] - CURRENTLY PURSUING
                        </p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <h3>> SECONDARY EDUCATION - GAS STRAND</h3>
                        <p><strong>Francisco Bustamante National Highschool</strong></p>
                        <p style="font-size: 0.85rem; color: var(--cyber-cyan); margin-top: 0.5rem;">
                            [ GENERAL ACADEMIC STRAND ] - COMPLETED
                        </p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <h3>> ELEMENTARY EDUCATION</h3>
                        <p><strong>Armed Forces of the Philippines Logistics Command Elementary School</strong></p>
                        <p style="font-size: 0.85rem; color: var(--cyber-cyan); margin-top: 0.5rem;">
                            [ FOUNDATION ] - COMPLETED
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="achievements" data-title="ACHIEVEMENTS">
        <div class="container">
            <h2>Certifications & Awards</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>CODM COMPETITION</h3>
                    <p style="color: var(--cyber-cyan); font-size: 1.3rem; font-weight: bold; margin: 1rem 0;">
                        4TH PLACER
                    </p>
                    <p style="color: var(--text-secondary); font-size: 0.85rem;">
                        BEYTE FEST EVENT
                    </p>
                </div>
                <div class="skill-card">
                    <h3>MTV SPOOF</h3>
                    <p style="color: var(--cyber-cyan); font-size: 1.3rem; font-weight: bold; margin: 1rem 0;">
                        1ST RUNNER UP
                    </p>
                    <p style="color: var(--text-secondary); font-size: 0.85rem;">
                        BEYTE FEST EVENT
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience" data-title="EXPERIENCE">
        <div class="container">
            <h2>Work Experience</h2>
            <div class="work-section">
                <h4>🚚 DELIVERY & CATERING SERVICES</h4>
                <p>
                    Professional experience in delivery and catering operations. Managed customer orders, ensured timely service delivery, and maintained high standards of customer satisfaction. Developed strong communication and logistics coordination skills through real-world operational challenges.
                </p>
            </div>
        </div>
    </section>

    <section id="contact" data-title="CONTACT">
        <div class="container">
            <h2>Initialize Connection</h2>
            <div class="contact-container">
                <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 3rem; letter-spacing: 1px;">
                    [ Ready for collaborations and new opportunities. Your message awaits processing. ]
                </p>
                <div class="contact-info">
                    <div class="contact-item">
                        <h3>📞 Phone</h3>
                        <a href="tel:09581881471">09581881471</a>
                    </div>
                    <div class="contact-item">
                        <h3>📧 Email</h3>
                        <a href="mailto:ajcalunia90@gmail.com">ajcalunia90@gmail.com</a>
                    </div>
                </div>
                <div class="social-links">
                    <a href="https://www.facebook.com/aj.calunia" target="_blank" title="Facebook">
                        <span>f</span>
                    </a>
                    <a href="https://github.com/caluniaaj-code" target="_blank" title="GitHub">
                        <span>⌘</span>
                    </a>
                </div>
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
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        const observerOptions = { threshold: 0.3 };
        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('glitch-element');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.skill-card, .project-card, .timeline-item, .contact-item, .work-section').forEach(el => {
            observer.observe(el);
        });

        const glitchElements = document.querySelectorAll('h1, h2, h3, .logo');
        glitchElements.forEach(el => {
            el.addEventListener('mouseenter', function() {
                const original = this.textContent;
                const glitched = original.split('').map(() => 
                    String.fromCharCode(Math.floor(Math.random() * 26) + 65)
                ).join('');
                this.textContent = glitched;
                setTimeout(() => { this.textContent = original; }, 100);
            });
        });
    </script>
</body>
</html>
