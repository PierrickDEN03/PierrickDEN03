<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pierrick DENNEMONT - Développeur</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #2a2d3a;
            color: white;
            min-height: 100vh;
            padding: 0;
        }

        .main-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 40px;
        }

        .profile-header {
            text-align: center;
            margin-bottom: 80px;
        }

        .profile-image {
            width: 350px;
            height: 350px;
            border-radius: 50%;
            border: 4px solid #4a4e91;
            background: linear-gradient(135deg, #4a4e91, #667eea);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            color: white;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            animation: pulse 3s infinite;
            box-shadow: 0 15px 35px rgba(74, 78, 145, 0.4);
            margin: 0 auto 30px auto;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.02); }
            100% { transform: scale(1); }
        }

        .hero-content {
            background: rgba(255, 255, 255, 0.95);
            color: #2a2d3a;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 3px solid #4a4e91;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-title {
            font-size: 3em;
            font-weight: bold;
            color: #4a4e91;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .hero-subtitle {
            font-size: 1.3em;
            color: #666;
            margin-bottom: 25px;
        }

        .hero-description {
            font-size: 1.1em;
            line-height: 1.7;
            color: #333;
        }

        .section {
            margin-bottom: 60px;
        }

        .section-title {
            font-size: 2.5em;
            text-align: center;
            margin-bottom: 40px;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .skills-section {
            margin-bottom: 60px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .skill-item {
            background: rgba(74, 78, 145, 0.2);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            color: white;
            font-weight: 500;
            border: 1px solid rgba(74, 78, 145, 0.5);
            transition: all 0.3s ease;
        }

        .skill-item:hover {
            background: rgba(74, 78, 145, 0.4);
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(74, 78, 145, 0.3);
        }

        .projects-section {
            margin-bottom: 60px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.95);
            color: #2a2d3a;
            padding: 30px;
            border-radius: 20px;
            margin-bottom: 20px;
            border-left: 5px solid #4a4e91;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
        }

        .project-title {
            font-size: 1.4em;
            font-weight: bold;
            color: #4a4e91;
            margin-bottom: 15px;
        }

        .project-description {
            line-height: 1.6;
            color: #333;
        }

        .contact-section {
            text-align: center;
            background: rgba(74, 78, 145, 0.1);
            padding: 40px;
            border-radius: 20px;
            border: 2px solid #4a4e91;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .social-link {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: white;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            transform: translateY(-5px);
        }

        .social-icon {
            width: 60px;
            height: 60px;
            background: #4a4e91;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 10px;
            transition: all 0.3s ease;
        }

        .social-link:hover .social-icon {
            background: #667eea;
            box-shadow: 0 8px 25px rgba(74, 78, 145, 0.4);
        }

        .social-icon svg {
            width: 30px;
            height: 30px;
            fill: white;
        }

        .social-label {
            font-weight: 500;
            font-size: 1.1em;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin: 50px 0;
        }

        .stat-item {
            text-align: center;
            background: rgba(74, 78, 145, 0.2);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(74, 78, 145, 0.5);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            color: white;
            display: block;
        }

        .stat-label {
            color: rgba(255, 255, 255, 0.8);
            font-size: 1.1em;
            margin-top: 10px;
        }

        @media (max-width: 768px) {
            .main-container {
                padding: 40px 20px;
            }

            .profile-image {
                width: 250px;
                height: 250px;
                font-size: 60px;
            }

            .hero-title {
                font-size: 2em;
            }

            .social-links {
                gap: 30px;
            }
        }
    </style>
</head>
<body>
    <div class="main-container">
        <section class="profile-header">
            <div class="profile-image">PD</div>
            <div class="hero-content">
                <h1 class="hero-title">Développeur en devenir, passionné par le web</h1>
                <p class="hero-subtitle">Pierrick DENNEMONT - Master Informatique</p>
                <p class="hero-description">
                    Je m'appelle Pierrick DENNEMONT, actuellement en Master Informatique. 
                    Depuis mes premiers projets, j'ai toujours été attiré par le développement 
                    web : concevoir, coder, tester et améliorer des interfaces pour les rendre 
                    fluides, accessibles et performantes. Curieux, rigoureux et motivé, je 
                    cherche sans cesse à progresser. Mon objectif : intégrer une entreprise 
                    en alternance pour l'année 2025-2026 afin de gagner en expérience et 
                    contribuer activement à des projets concrets.
                </p>
            </div>
        </section>

        <section id="competences" class="skills-section">
            <h2 class="section-title">Technologies & Compétences</h2>
            <div class="skills-grid">
                <div class="skill-item">JavaScript</div>
                <div class="skill-item">React</div>
                <div class="skill-item">Node.js</div>
                <div class="skill-item">Python</div>
                <div class="skill-item">HTML/CSS</div>
                <div class="skill-item">Git</div>
                <div class="skill-item">PostgreSQL</div>
                <div class="skill-item">Swift</div>
                <div class="skill-item">MySQL</div>
                <div class="skill-item">Elementor</div>
                <div class="skill-item">WordPress</div>
                <div class="skill-item">PHP</div>
            </div>
        </section>

        <div class="stats-container">
            <div class="stat-item">
                <span class="stat-number">25+</span>
                <span class="stat-label">Projets réalisés</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">3+</span>
                <span class="stat-label">Années d'études</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">12+</span>
                <span class="stat-label">Technologies maîtrisées</span>
            </div>
        </div>

        <section id="projets" class="projects-section">
            <h2 class="section-title">Projets réalisés</h2>
            <div class="project-card">
                <h3 class="project-title">Projet : Site Portfolio</h3>
                <p class="project-description">
                    <strong>Description :</strong> Il s'agit de mon premier projet 
                    personnel. Désireux d'être à la hauteur des 
                    attentes des différentes offres d'alternance, j'ai 
                    décidé de développer mon site en React, un 
                    framework que je n'avais pas encore étudié dans 
                    le cadre de mon cursus universitaire. Une 
                    implémentation d'une petite base de données 
                    avec Express et MongoDB est également prévue, 
                    ainsi qu'une initiation à Bootstrap pour la mise en 
                    forme en CSS est prévue à l'avenir.
                </p>
            </div>
        </section>

        <section id="contact" class="contact-section">
            <h2 class="section-title">Contactez-moi</h2>
            <p style="font-size: 1.2em; margin-bottom: 20px; color: rgba(255, 255, 255, 0.9);">
                Toujours ouvert aux nouvelles opportunités et collaborations !
            </p>
            
            <div class="social-links">
                <a href="https://linkedin.com/in/pierrick-dennemont-a9473226a/" class="social-link" target="_blank">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                        </svg>
                    </div>
                    <span class="social-label">LinkedIn</span>
                </a>

                <a href="mailto:pierrick.dennemont@gmail.com" class="social-link">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                        </svg>
                    </div>
                    <span class="social-label">pierrick.dennemont@gmail.com</span>
                </a>

                <a href="https://github.com/pierrickDEN03" class="social-link" target="_blank">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </div>
                    <span class="social-label">GitHub</span>
                </a>

                <a href="https://pierrickden03.github.io/Mon-site/" class="social-link" target="_blank">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
                        </svg>
                    </div>
                    <span class="social-label">Portfolio</span>
                </a>
            </div>
        </section>
    </div>
</body>
</html>
