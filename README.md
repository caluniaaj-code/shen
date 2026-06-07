<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A.J. L. Calunia | Portfolio</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Segoe UI',sans-serif;
}

body{
    background:#f4f7fc;
    color:#333;
    line-height:1.6;
}

header{
    background:linear-gradient(135deg,#0f172a,#1e3a8a);
    color:white;
    text-align:center;
    padding:60px 20px;
}

header h1{
    font-size:3rem;
    margin-bottom:10px;
}

header p{
    font-size:1.2rem;
}

.container{
    width:90%;
    max-width:1100px;
    margin:auto;
    padding:30px 0;
}

section{
    background:white;
    margin-bottom:25px;
    padding:30px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
}

h2{
    color:#1e3a8a;
    margin-bottom:20px;
    border-left:5px solid #1e3a8a;
    padding-left:10px;
}

.about p{
    text-align:justify;
}

.skills{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
    gap:20px;
}

.skill{
    margin-bottom:15px;
}

.skill-name{
    display:flex;
    justify-content:space-between;
    margin-bottom:5px;
}

.bar{
    height:10px;
    background:#ddd;
    border-radius:20px;
}

.progress{
    height:10px;
    border-radius:20px;
    background:#1e3a8a;
}

ul{
    padding-left:20px;
}

.project-card{
    background:#f8f9ff;
    padding:20px;
    border-radius:10px;
    border-left:5px solid #1e3a8a;
}

.contact a{
    text-decoration:none;
    color:#1e3a8a;
    font-weight:bold;
}

footer{
    text-align:center;
    padding:20px;
    background:#0f172a;
    color:white;
}

.badge{
    display:inline-block;
    background:#1e3a8a;
    color:white;
    padding:8px 15px;
    border-radius:20px;
    margin:5px;
}

@media(max-width:768px){
    header h1{
        font-size:2.2rem;
    }
}
</style>
</head>
<body>

<header>
    <h1>A.J. L. Calunia</h1>
    <p>BS Information Systems Student | Aspiring IT Professional</p>
</header>

<div class="container">

    <section class="about">
        <h2>About Me</h2>
        <p>
            Hello! My name is <strong>A.J. L. Calunia</strong>, born on December 3, 2006.
            I am a curious, friendly, and determined person who enjoys learning new things and taking on challenges that help me grow.
            I value honesty, respect, and perseverance, and I strive to maintain a positive attitude in everything I do.
            In my free time, I enjoy playing sports, gaming, spending time with friends and family, and exploring topics that interest me.
            I believe that personal growth comes from experience, continuous learning, and stepping outside of my comfort zone.
        </p>
    </section>

    <section>
        <h2>Hobbies & Sports</h2>
        <span class="badge">🏀 Basketball</span>
        <span class="badge">🚴 Cycling</span>
        <span class="badge">🎮 Gaming</span>
    </section>

    <section>
        <h2>Education</h2>

        <h3>Elementary</h3>
        <p>Armed Forces of the Philippines Logistics Command Elementary School</p>

        <br>

        <h3>Senior High School</h3>
        <p>Francisco Bustamante National High School</p>
        <p><strong>GAS Strand</strong></p>

        <br>

        <h3>College</h3>
        <p>Davao del Norte State College</p>
        <p><strong>Bachelor of Science in Information Systems (BSIS)</strong></p>
    </section>

    <section>
        <h2>Technical Skills</h2>

        <div class="skills">

            <div>
                <div class="skill">
                    <div class="skill-name">
                        <span>Java / Swing</span>
                        <span>70%</span>
                    </div>
                    <div class="bar">
                        <div class="progress" style="width:70%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-name">
                        <span>SQL / MySQL</span>
                        <span>65%</span>
                    </div>
                    <div class="bar">
                        <div class="progress" style="width:65%"></div>
                    </div>
                </div>

                <div class="skill">
                    <div class="skill-name">
                        <span>NetBeans IDE</span>
                        <span>80%</span>
                    </div>
                    <div class="bar">
                        <div class="progress" style="width:80%"></div>
                    </div>
                </div>
            </div>

            <div>
                <h3>Soft Skills</h3>
                <ul>
                    <li>Communication</li>
                    <li>Cooking</li>
                    <li>Team Collaboration</li>
                    <li>Continuous Learning</li>
                </ul>
            </div>

        </div>
    </section>

    <section>
        <h2>Project</h2>

        <div class="project-card">
            <h3>Information Systems Technological Plan for Maycel Hometel</h3>

            <p>
                This project proposes technology-based solutions to improve the operations and services
                of Maycel Hometel. The plan focuses on enhancing efficiency in managing reservations,
                guest records, billing, and administrative tasks through an integrated information system.
            </p>

            <br>

            <p>
                By utilizing modern technologies and digital tools, the system streamlines business
                processes, improves data accuracy, strengthens security, and enhances the overall
                experience for both management and guests. It supports informed decision-making and
                helps the establishment adapt to the growing demands of the hospitality industry.
            </p>
        </div>
    </section>

    <section>
        <h2>Certificates & Achievements</h2>

        <ul>
            <li>🏆 4th Placer – CODM BEYTE FEST Event</li>
            <li>🥈 1st Runner-Up – MTV Spoof, BEYTE FEST Event</li>
        </ul>
    </section>

    <section>
        <h2>Work Experience</h2>

        <ul>
            <li>Delivery Services</li>
            <li>Catering Services</li>
        </ul>
    </section>

    <section class="contact">
        <h2>Contact Information</h2>

        <p><strong>Phone:</strong> 0958-188-1471</p>
        <p><strong>Email:</strong> ajcalunia90@gmail.com</p>
        <p>
            <strong>Facebook:</strong>
            <a href="https://www.facebook.com/aj.calunia" target="_blank">
                facebook.com/aj.calunia
            </a>
        </p>
    </section>

</div>

<footer>
    <p>© 2026 A.J. L. Calunia | Portfolio Website</p>
</footer>

</body>
</html>
