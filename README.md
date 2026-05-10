<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saul.K | Portfolio</title>
    <style>
        :root {
            --neon-blue: #00d4ff;
            --terminal-green: #00ff41;
            --bg-dark: #0a0b10;
            --card-bg: #161b22;
            --text-main: #e6edf3;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Consolas', 'Courier New', monospace;
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Scanline Effect */
        body::before {
            content: " ";
            display: block;
            position: fixed;
            top: 0; left: 0; bottom: 0; right: 0;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), 
                        linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
            z-index: 9999;
            background-size: 100% 4px, 3px 100%;
            pointer-events: none;
        }

        header {
            height: 60vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            border-bottom: 1px solid var(--neon-blue);
            background: radial-gradient(circle at center, #112240 0%, var(--bg-dark) 70%);
        }

        .glitch-wrapper {
            font-size: 3.5rem;
            font-weight: bold;
            color: var(--neon-blue);
            text-transform: uppercase;
            letter-spacing: 5px;
            margin-bottom: 1rem;
        }

        .tagline {
            color: var(--terminal-green);
            font-size: 1.2rem;
        }

        nav {
            position: sticky;
            top: 0;
            background: rgba(10, 11, 16, 0.95);
            padding: 1rem;
            display: flex;
            justify-content: center;
            gap: 2rem;
            border-bottom: 1px solid #30363d;
            z-index: 1000;
        }

        nav a {
            color: var(--text-main);
            text-decoration: none;
            font-size: 0.9rem;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--neon-blue);
            text-shadow: 0 0 8px var(--neon-blue);
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        h2 {
            border-left: 4px solid var(--neon-blue);
            padding-left: 1rem;
            margin-bottom: 2rem;
            font-size: 2rem;
            color: var(--neon-blue);
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 4px;
            border: 1px solid #30363d;
            transition: transform 0.2s, border-color 0.2s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--neon-blue);
        }

        .card h3 {
            color: var(--terminal-green);
            margin-bottom: 0.5rem;
        }

        .skill-tag {
            display: inline-block;
            background: #1f2937;
            padding: 4px 10px;
            margin: 5px;
            border-radius: 3px;
            font-size: 0.8rem;
            border: 1px solid #38bdf8;
        }

        footer {
            text-align: center;
            padding: 3rem;
            border-top: 1px solid #30363d;
            font-size: 0.8rem;
            color: #8b949e;
        }

        .highlight { color: var(--neon-blue); }

        @media (max-width: 600px) {
            .glitch-wrapper { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="glitch-wrapper">SAUL.K</div>
        <div class="tagline">> Systems. Security. Software.</div>
    </header>

    <nav>
        <a href="#about">ABOUT</a>
        <a href="#projects">PROJECTS</a>
        <a href="#skills">SKILLS</a>
    </nav>

    <div class="container" id="about">
        <h2>01_Mission</h2>
        <p>I am a developer focused on building efficient, secure, and interactive digital ecosystems. From coding robust logic in <span class="highlight">Python</span> and <span class="highlight">GDScript</span> to architecting educational portals with <span class="highlight">3D Geomorphology models</span>, my goal is to bridge the gap between complex data and user experience.</p>
    </div>

    <div class="container" id="projects">
        <h2>02_Deployments</h2>
        <div class="grid">
            <div class="card">
                <h3>Geo-Educational Portal</h3>
                <p>An interactive Grade 12 Geography platform. Integrates Three.js for 3D globe visualization and syllabus-specific geomorphology modules.</p>
            </div>
            <div class="card">
                <h3>AI-Driven Notepad</h3>
                <p>Advanced Android application using Kotlin and Jetpack Compose. Features automated tagging and smart summarization logic.</p>
            </div>
            <div class="card">
                <h3>Godot Systems</h3>
                <p>Developing custom game mechanics and modular scripts in GDScript, pushing the boundaries of lightweight game architecture.</p>
            </div>
        </div>
    </div>

    <div class="container" id="skills">
        <h2>03_Toolkit</h2>
        <div class="card">
            <p><strong>Languages:</strong> 
                <span class="skill-tag">Python</span> 
                <span class="skill-tag">GDScript</span> 
                <span class="skill-tag">Kotlin</span> 
                <span class="skill-tag">HTML/CSS/JS</span>
            </p><br>
            <p><strong>Sec-Ops:</strong> 
                <span class="skill-tag">Nmap</span> 
                <span class="skill-tag">Kali Linux</span> 
                <span class="skill-tag">Ethical Hacking</span>
            </p><br>
            <p><strong>Engines:</strong> 
                <span class="skill-tag">Godot</span> 
                <span class="skill-tag">Three.js</span>
            </p>
        </div>
    </div>

    <footer>
        <p>TERMINAL_SESSION: 2026 // LOC_ID: KZN_RSA</p>
        <p>Optimized for low-bandwidth environments.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
