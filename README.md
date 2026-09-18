<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Deekshith K R | CSE AI Student</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #0a0a0a;
            color: #ffffff;
            line-height: 1.6;
        }

        /* NAVBAR */

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(10, 10, 10, 0.85);
            backdrop-filter: blur(15px);
            z-index: 1000;
            border-bottom: 1px solid #222;
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
        }

        .logo span {
            color: #00d9ff;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            color: #ccc;
            text-decoration: none;
            font-size: 14px;
            transition: 0.3s;
        }

        nav a:hover {
            color: #00d9ff;
        }

        /* HERO */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 100px 8% 50px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            width: 500px;
            height: 500px;
            background: #006eff;
            filter: blur(180px);
            opacity: 0.15;
            top: 10%;
            right: 5%;
        }

        .hero-content {
            max-width: 800px;
            position: relative;
            z-index: 1;
        }

        .small-title {
            color: #00d9ff;
            font-size: 16px;
            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(45px, 8vw, 85px);
            line-height: 1;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #00d9ff;
        }

        .hero h2 {
            font-size: 25px;
            color: #aaa;
            margin-bottom: 25px;
        }

        .hero p {
            color: #999;
            max-width: 650px;
            font-size: 17px;
        }

        .buttons {
            margin-top: 35px;
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 13px 25px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .primary {
            background: #00d9ff;
            color: #000;
        }

        .primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.3);
        }

        .secondary {
            border: 1px solid #444;
            color: white;
        }

        .secondary:hover {
            border-color: #00d9ff;
            color: #00d9ff;
        }

        /* SECTIONS */

        section {
            padding: 100px 8%;
        }

        .section-title {
            font-size: 40px;
            margin-bottom: 50px;
        }

        .section-title span {
            color: #00d9ff;
        }

        /* ABOUT */

        .about {
            background: #0e0e0e;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .about p {
            color: #aaa;
            font-size: 16px;
        }

        .info-card {
            background: #151515;
            padding: 30px;
            border: 1px solid #252525;
            border-radius: 15px;
        }

        .info-card h3 {
            margin-bottom: 20px;
            color: #00d9ff;
        }

        .info-card p {
            margin-bottom: 10px;
        }

        /* SKILLS */

        .skills-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .skill-card {
            background: #111;
            padding: 25px;
            border-radius: 15px;
            border: 1px solid #222;
            transition: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: #00d9ff;
        }

        .skill-card h3 {
            margin-bottom: 15px;
            color: #00d9ff;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill {
            padding: 8px 13px;
            background: #1c1c1c;
            border: 1px solid #292929;
            border-radius: 6px;
            color: #ccc;
            font-size: 13px;
        }

        /* PROJECTS */

        .projects {
            background: #0e0e0e;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: #151515;
            border: 1px solid #252525;
            padding: 30px;
            border-radius: 15px;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-8px);
            border-color: #00d9ff;
        }

        .project-number {
            color: #00d9ff;
            font-size: 14px;
            margin-bottom: 20px;
        }

        .project-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
        }

        .project-card p {
            color: #999;
            margin-bottom: 20px;
        }

        .tech {
            color: #00d9ff;
            font-size: 13px;
        }

        /* LEETCODE */

        .leetcode-box {
            padding: 50px;
            border: 1px solid #252525;
            border-radius: 20px;
            background: linear-gradient(135deg, #121212, #181818);
        }

        .leetcode-box h3 {
            font-size: 30px;
            margin-bottom: 15px;
        }

        .leetcode-box p {
            color: #999;
            max-width: 700px;
        }

        /* CONTACT */

        .contact {
            text-align: center;
        }

        .contact p {
            color: #999;
            margin-bottom: 30px;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        /* FOOTER */

        footer {
            text-align: center;
            padding: 30px;
            border-top: 1px solid #222;
            color: #666;
        }

        /* ANIMATION */

        .fade {
            opacity: 0;
            transform: translateY(30px);
            transition: 0.7s;
        }

        .fade.show {
            opacity: 1;
            transform: translateY(0);
        }

        /* MOBILE */

        @media (max-width: 800px) {

            nav ul {
                display: none;
            }

            .hero {
                padding-left: 6%;
                padding-right: 6%;
            }

            section {
                padding: 70px 6%;
            }

            .about-grid,
            .skills-container,
            .project-grid {
                grid-template-columns: 1fr;
            }

            .hero h1 {
                font-size: 50px;
            }

            .leetcode-box {
                padding: 30px;
            }
        }
    </style>
</head>

<body>

    <!-- NAVIGATION -->

    <nav>
        <div class="logo">
            Deekshith<span>.</span>
        </div>

        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>


    <!-- HERO -->

    <section class="hero" id="home">

        <div class="hero-content">

            <div class="small-title">
                B.Tech CSE — Artificial Intelligence
            </div>

            <h1>
                Deekshith <span>K R</span>
            </h1>

            <h2>
                Software Developer | DSA | AI & Data
            </h2>

            <p>
                I am a second-year Computer Science and Engineering
                (Artificial Intelligence) student focused on building
                practical software, solving algorithmic problems,
                and exploring Artificial Intelligence and Data Analytics.
            </p>

            <div class="buttons">

                <a href="#projects" class="btn primary">
                    View Projects
                </a>

                <a href="https://github.com/deekshith29891-wq"
                   target="_blank"
                   class="btn secondary">
                    GitHub
                </a>

            </div>

        </div>

    </section>


    <!-- ABOUT -->

    <section class="about fade" id="about">

        <h2 class="section-title">
            About <span>Me</span>
        </h2>

        <div class="about-grid">

            <div>
                <p>
                    I am currently pursuing B.Tech in Computer Science
                    and Engineering with a specialization in Artificial
                    Intelligence at Yenepoya University.
                </p>

                <br>

                <p>
                    My current focus is strengthening my programming,
                    Data Structures and Algorithms, full-stack development,
                    and problem-solving skills while building practical
                    projects.
                </p>

                <br>

                <p>
                    I am actively exploring Artificial Intelligence,
                    Machine Learning fundamentals, and Data Analytics.
                </p>
            </div>

            <div class="info-card">

                <h3>Quick Information</h3>

                <p><strong>Education:</strong> B.Tech CSE (AI)</p>

                <p><strong>Year:</strong> 2nd Year</p>

                <p><strong>Location:</strong> Mangaluru, Karnataka</p>

                <p><strong>Focus:</strong> Software Development</p>

                <p><strong>Goal:</strong> Software Engineering Internship</p>

            </div>

        </div>

    </section>


    <!-- SKILLS -->

    <section id="skills" class="fade">

        <h2 class="section-title">
            Technical <span>Skills</span>
        </h2>

        <div class="skills-container">

            <div class="skill-card">

                <h3>Programming</h3>

                <div class="skills">

                    <span class="skill">Python</span>
                    <span class="skill">C++</span>
                    <span class="skill">JavaScript</span>
                    <span class="skill">TypeScript</span>

                </div>

            </div>


            <div class="skill-card">

                <h3>Frontend</h3>

                <div class="skills">

                    <span class="skill">HTML</span>
                    <span class="skill">CSS</span>
                    <span class="skill">React.js</span>
                    <span class="skill">Next.js</span>

                </div>

            </div>


            <div class="skill-card">

                <h3>Backend</h3>

                <div class="skills">

                    <span class="skill">Node.js</span>
                    <span class="skill">REST APIs</span>
                    <span class="skill">Express.js</span>

                </div>

            </div>


            <div class="skill-card">

                <h3>Database & Tools</h3>

                <div class="skills">

                    <span class="skill">SQL</span>
                    <span class="skill">PostgreSQL</span>
                    <span class="skill">MongoDB</span>
                    <span class="skill">Git</span>
                    <span class="skill">GitHub</span>

                </div>

            </div>


            <div class="skill-card">

                <h3>AI & Data</h3>

                <div class="skills">

                    <span class="skill">Artificial Intelligence</span>
                    <span class="skill">Machine Learning</span>
                    <span class="skill">NumPy</span>
                    <span class="skill">Pandas</span>
                    <span class="skill">Data Analysis</span>

                </div>

            </div>


            <div class="skill-card">

                <h3>Core Computer Science</h3>

                <div class="skills">

                    <span class="skill">DSA</span>
                    <span class="skill">OOP</span>
                    <span class="skill">DBMS</span>
                    <span class="skill">Problem Solving</span>

                </div>

            </div>

        </div>

    </section>


    <!-- PROJECTS -->

    <section class="projects fade" id="projects">

        <h2 class="section-title">
            Featured <span>Projects</span>
        </h2>

        <div class="project-grid">

            <div class="project-card">

                <div class="project-number">
                    PROJECT 01
                </div>

                <h3>Job Application Tracker</h3>

                <p>
                    A web application for tracking job applications
                    using a relational database and REST APIs.
                </p>

                <div class="tech">
                    Node.js · Express.js · SQL
                </div>

            </div>


            <div class="project-card">

                <div class="project-number">
                    PROJECT 02
                </div>

                <h3>Data Analysis Project</h3>

                <p>
                    A data analysis project focused on cleaning datasets,
                    analyzing information, and identifying useful patterns.
                </p>

                <div class="tech">
                    Python · Pandas · NumPy
                </div>

            </div>


            <div class="project-card">

                <div class="project-number">
                    PROJECT 03
                </div>

                <h3>LeetCode Practice</h3>

                <p>
                    Regularly solving Data Structures and Algorithms
                    problems to improve algorithmic thinking and
                    problem-solving skills.
                </p>

                <div class="tech">
                    C++ · Python · DSA
                </div>

            </div>

        </div>

    </section>


    <!-- LEETCODE -->

    <section class="fade">

        <h2 class="section-title">
            Problem <span>Solving</span>
        </h2>

        <div class="leetcode-box">

            <h3>Data Structures & Algorithms</h3>

            <p>
                I regularly practice algorithmic problems on LeetCode,
                focusing on arrays, strings, hash maps, sorting,
                searching, and efficient problem-solving techniques.
            </p>

            <br>

            <a href="https://leetcode.com/"
               target="_blank"
               class="btn primary">
                View LeetCode
            </a>

        </div>

    </section>


    <!-- CONTACT -->

    <section class="contact fade" id="contact">

        <h2 class="section-title">
            Let's <span>Connect</span>
        </h2>

        <p>
            I am interested in software engineering internships,
            development opportunities, and technical collaborations.
        </p>

        <div class="contact-links">

            <a href="mailto:deekshith29891@gmail.com"
               class="btn primary">
                Email Me
            </a>

            <a href="https://github.com/deekshith29891-wq"
               target="_blank"
               class="btn secondary">
                GitHub
            </a>

        </div>

    </section>


    <!-- FOOTER -->

    <footer>
        © 2026 Deekshith K R. Built with HTML, CSS and JavaScript.
    </footer>


    <!-- JAVASCRIPT -->

    <script>

        const elements = document.querySelectorAll(".fade");

        const observer = new IntersectionObserver(
            (entries) => {

                entries.forEach((entry) => {

                    if (entry.isIntersecting) {
                        entry.target.classList.add("show");
                    }

                });

            },
            {
                threshold: 0.15
            }
        );

        elements.forEach((element) => {
            observer.observe(element);
        });

    </script>

</body>
</html>
