<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pierrick DENNEMONT - Portfolio GitHub</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #1e1e2e 0%, #2d1b69 50%, #1e1e2e 100%);
            color: #ffffff;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
        }

        .header h1 {
            font-size: 3rem;
            font-weight: 300;
            margin-bottom: 20px;
            color: #ffffff;
        }

        .navigation {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .nav-item {
            background: rgba(255, 255, 255, 0.9);
            color: #333;
            padding: 12px 24px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .nav-item.active {
            background: #4c5bde;
            color: white;
        }

        .nav-item:hover {
            background: rgba(255, 255, 255, 1);
            transform: translateY(-2px);
        }

        .main-content {
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 40px;
            margin-bottom: 50px;
        }

        .profile-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .profile-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #4c5bde, #7c3aed, #ec4899, #f59e0b);
            border-radius: 20px 20px 0 0;
        }

        .profile-avatar {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: linear-gradient(135deg, #4c5bde, #7c3aed);
            margin: 0 auto 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            font-weight: bold;
            color: white;
            border: 4px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 20px 40px rgba(76, 91, 222, 0.3);
        }

        .profile-title {
            font-size: 2.5rem;
            font-weight: 600;
            margin-bottom: 10px;
            text-align: center;
        }

        .profile-subtitle {
            font-size: 1.3rem;
            color: #a8a8a8;
            text-align: center;
            margin-bottom: 30px;
        }

        .profile-description {
            font-size: 1.1rem;
            line-height: 1.7;
            color: #e0e0e0;
            margin-bottom: 40px;
        }

        .info-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            margin-bottom: 20px;
        }

        .info-card h3 {
            color: #4c5bde;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .skill-category::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #4c5bde, #7c3aed);
            border-radius: 20px 20px 0 0;
        }

        .skill-category h3 {
            color: #ffffff;
            margin-bottom: 20px;
            font-size: 1.4rem;
            font-weight: 600;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-tag {
            background: rgba(76, 91, 222, 0.2);
            color: #ffffff;
            padding: 8px 16px;
            border-radius: 25px;
            font-size: 0.9rem;
            border: 1px solid rgba(76, 91, 222, 0.3);
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            background: rgba(76, 91, 222, 0.4);
            transform: translateY(-2px);
        }

        .projects-section {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            text-align: center;
            color: #ffffff;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            margin-bottom: 20px;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #ec4899, #f59e0b);
            border-radius: 20px 20px 0 0;
        }

        .project-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #ffffff;
        }

        .project-description {
            color: #e0e0e0;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-tag {
            background: rgba(236, 72, 153, 0.2);
            color: #ffffff;
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid rgba(236, 72, 153, 0.3);
        }

        .social-section {
            text-align: center;
            margin-top: 50px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 30px;
        }

        .social-link {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            color: #ffffff;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            transform: translateY(-5px);
        }

        .social-icon {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }

        .social-link:hover .social-icon {
            background: rgba(76, 91, 222, 0.3);
            border-color: #4c5bde;
        }

        .social-icon svg {
            width: 24px;
            height: 24px;
            fill: currentColor;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: #4c5bde;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #4c5bde;
            display: block;
            margin-bottom: 5px;
        }

        .stat-label {
            color: #a8a8a8;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
                gap: 30px;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .navigation {
                gap: 10px;
            }
            
            .nav-item {
                padding: 10px 20px;
                font-size: 0.9rem;
            }
            
            .social-links {
                gap: 30px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1>Bienvenue</h1>
            <nav class="navigation">
                <a href="#" class="nav-item active">Accueil</a>
                <a href="#" class="nav-item">Présentation</a>
                <a href="#" class="nav-item">Formation</a>
                <a href="#" class="nav-item">Mes projets</a>
                <a href="#" class="nav-item">Me contacter</a>
            </nav>
        </header>

        <div class="main-content">
            <div class="profile-card">
                <div class="profile-avatar">PD</div>
                <h2 class="profile-title">Pierrick DENNEMONT</h2>
                <p class="profile-subtitle">Développeur en devenir, passionné par le web</p>
                <div class="profile-description">
                    Je m'appelle Pierrick DENNEMONT, actuellement en Master Informatique. 
                    Depuis mes premiers projets, j'ai toujours été attiré par le développement 
                    web : concevoir, coder, tester et améliorer des interfaces pour les rendre 
                    fluides, accessibles et performantes. Curieux, rigoureux et motivé, je 
                    cherche sans cesse à progresser.
                </div>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <span class="stat-number">5+</span>
                        <div class="stat-label">Projets réalisés</div>
                    </div>
                    <div class="stat-card">
                        <span class="stat-number">2025</span>
                        <div class="stat-label">Année d'alternance</div>
                    </div>
                </div>
            </div>

            <div class="info-card">
                <h3>🎓 Formation actuelle</h3>
                <p><strong>Master Informatique</strong><br>
                Université Lumière Lyon 2<br>
                2025 - ...</p>
                
                <h3 style="margin-top: 20px;">🎯 Objectif</h3>
                <p>Intégrer une entreprise en alternance pour l'année 2025-2026 afin de gagner en expérience et contribuer activement à des projets concrets.</p>
            </div>
        </div>

        <section class="projects-section">
            <h2 class="section-title">🚀 Mes projets</h2>
            <div class="project-card">
                <h3 class="project-title">Site Portfolio</h3>
                <p class="project-description">
                    Mon premier projet personnel développé en React. Une implémentation avec Express et MongoDB 
                    est prévue, ainsi qu'une initiation à Bootstrap pour la mise en forme CSS.
                </p>
                <div class="project-tech">
                    <span class="tech-tag">React</span>
                    <span class="tech-tag">JavaScript</span>
                    <span class="tech-tag">CSS</span>
                    <span class="tech-tag">Express</span>
                    <span class="tech-tag">MongoDB</span>
                </div>
            </div>
        </section>

        <section class="skills-grid">
            <div class="skill-category">
                <h3>💻 Langages acquis</h3>
                <div class="skill-tags">
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">PHP</span>
                    <span class="skill-tag">Python</span>
                    <span class="skill-tag">Java</span>
                    <span class="skill-tag">TypeScript</span>
                    <span class="skill-tag">C#</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🔧 Technologies</h3>
                <div class="skill-tags">
                    <span class="skill-tag">React</span>
                    <span class="skill-tag">Node.js</span>
                    <span class="skill-tag">Express</span>
                    <span class="skill-tag">MongoDB</span>
                    <span class="skill-tag">MySQL</span>
                    <span class="skill-tag">Git</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🎨 Frontend</h3>
                <div class="skill-tags">
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">Bootstrap</span>
                    <span class="skill-tag">Responsive Design</span>
                    <span class="skill-tag">UI/UX</span>
                </div>
            </div>

            <div class="skill-category">
                <h3>🌐 En cours d'apprentissage</h3>
                <div class="skill-tags">
                    <span class="skill-tag">Vue.js</span>
                    <span class="skill-tag">Docker</span>
                    <span class="skill-tag">AWS</span>
                    <span class="skill-tag">PostgreSQL</span>
                </div>
            </div>
        </section>

        <section class="social-section">
            <h2 class="section-title">📫 Connectons-nous !</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/votre-profil" class="social-link" target="_blank">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                        </svg>
                    </div>
                    LinkedIn
                </a>

                <a href="mailto:pierrick.dennemont@gmail.com" class="social-link">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                        </svg>
                    </div>
                    pierrick.dennemont@gmail.com
                </a>

                <a href="https://github.com/pierrickden03" class="social-link" target="_blank">
                    <div class="social-icon">
                        <svg viewBox="0 0 24 24">
                            <path d="M12 0C5.374 0 0 5.373 0 12 0 17.302 3.438 21.8 8.207 23.387c.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </div>
                    GitHub
                </a>
            </div>
        </section>
    </div>
</body>
</html>
