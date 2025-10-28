
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Page personnelle de [Votre Nom] - Étudiant(e) à l'Université de Sherbrooke">
    <meta name="author" content="Votre Nom">
    <title>Votre Nom - Portfolio Académique</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --text-color: #333;
            --text-light: #666;
            --bg-color: #ffffff;
            --bg-secondary: #f8f9fa;
            --border-color: #e0e0e0;
            --shadow: 0 2px 10px rgba(0,0,0,0.1);
            --shadow-hover: 0 5px 20px rgba(0,0,0,0.15);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.7;
            color: var(--text-color);
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: var(--bg-color);
            border-radius: 15px;
            box-shadow: var(--shadow);
            overflow: hidden;
            animation: fadeIn 0.6s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* En-tête avec bannière */
        .header-banner {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 60px 40px 40px;
            position: relative;
            overflow: hidden;
        }

        .header-banner::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: pulse 15s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.1) rotate(180deg); }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3em;
            font-weight: 700;
            margin-bottom: 10px;
            letter-spacing: -0.5px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }
        
        .subtitle {
            font-size: 1.3em;
            margin-bottom: 5px;
            opacity: 0.95;
            font-weight: 300;
        }
        
        .affiliation {
            font-size: 1.1em;
            opacity: 0.9;
            font-weight: 300;
        }

        /* Navigation */
        .nav-tabs {
            display: flex;
            justify-content: center;
            gap: 5px;
            padding: 20px 40px;
            background: var(--bg-secondary);
            border-bottom: 2px solid var(--border-color);
            flex-wrap: wrap;
        }

        .nav-tab {
            padding: 10px 20px;
            background: white;
            border: 2px solid var(--border-color);
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            color: var(--text-color);
        }

        .nav-tab:hover {
            background: var(--secondary-color);
            color: white;
            border-color: var(--secondary-color);
            transform: translateY(-2px);
            box-shadow: var(--shadow);
        }

        .nav-tab.active {
            background: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }

        /* Contenu principal */
        .content {
            padding: 40px;
        }

        .section {
            margin-bottom: 40px;
            animation: slideIn 0.5s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .section.hidden {
            display: none;
        }

        .section h2 {
            font-size: 2em;
            font-weight: 600;
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--secondary-color);
            position: relative;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--accent-color);
        }

        p {
            margin-bottom: 15px;
            text-align: justify;
            line-height: 1.8;
        }

        /* Cards pour projets et formations */
        .card {
            background: var(--bg-secondary);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            border-left: 4px solid var(--secondary-color);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(52, 152, 219, 0.05) 0%, transparent 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card:hover {
            transform: translateX(10px);
            box-shadow: var(--shadow-hover);
        }

        .card:hover::before {
            opacity: 1;
        }

        .card h3 {
            color: var(--primary-color);
            margin-bottom: 10px;
            font-size: 1.3em;
        }

        .card-meta {
            color: var(--text-light);
            font-size: 0.9em;
            margin-bottom: 10px;
            font-style: italic;
        }

        /* Badges pour compétences */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        .skill-category {
            background: var(--bg-secondary);
            border-radius: 10px;
            padding: 20px;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .skill-category h3 {
            color: var(--secondary-color);
            margin-bottom: 15px;
            font-size: 1.1em;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-tag {
            display: inline-block;
            background: white;
            padding: 5px 15px;
            border-radius: 20px;
            margin: 5px 5px 5px 0;
            font-size: 0.9em;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            background: var(--secondary-color);
            color: white;
            border-color: var(--secondary-color);
            transform: scale(1.05);
        }

        /* Liens sociaux */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 25px;
            background: var(--bg-secondary);
            border-radius: 30px;
            text-decoration: none;
            color: var(--text-color);
            transition: all 0.3s ease;
            border: 2px solid transparent;
            font-weight: 500;
        }

        .social-link:hover {
            background: var(--secondary-color);
            color: white;
            transform: translateY(-3px);
            box-shadow: var(--shadow);
            border-color: var(--secondary-color);
        }

        .social-link .icon {
            font-size: 1.3em;
        }

        /* Timeline pour formation */
        .timeline {
            position: relative;
            padding-left: 40px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 10px;
            top: 0;
            bottom: 0;
            width: 3px;
            background: var(--secondary-color);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            padding-left: 20px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -34px;
            top: 0;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: var(--secondary-color);
            border: 3px solid white;
            box-shadow: 0 0 0 3px var(--secondary-color);
        }

        .timeline-item h3 {
            color: var(--primary-color);
            margin-bottom: 5px;
        }

        .timeline-date {
            color: var(--text-light);
            font-size: 0.9em;
            margin-bottom: 10px;
        }

        /* Contact card */
        .contact-card {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-top: 30px;
            box-shadow: var(--shadow-hover);
        }

        .contact-card h3 {
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 15px;
            padding: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(5px);
        }

        .contact-item .icon {
            font-size: 1.5em;
        }

        .contact-item a {
            color: white;
            text-decoration: none;
        }

        .contact-item a:hover {
            text-decoration: underline;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 30px;
            background: var(--bg-secondary);
            color: var(--text-light);
            border-top: 1px solid var(--border-color);
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }

            .header-banner {
                padding: 40px 20px 30px;
            }

            .content {
                padding: 20px;
            }

            .nav-tabs {
                padding: 15px 20px;
            }

            .nav-tab {
                padding: 8px 15px;
                font-size: 0.9em;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .timeline {
                padding-left: 30px;
            }
        }

        /* Animations d'entrée */
        .fade-in {
            animation: fadeIn 0.6s ease-in;
        }

        /* Scroll smooth */
        html {
            scroll-behavior: smooth;
        }

        /* Sélection de texte */
        ::selection {
            background: var(--secondary-color);
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- En-tête avec bannière -->
        <header class="header-banner">
            <div class="header-content">
                <h1>Votre Nom</h1>
                <div class="subtitle">Étudiant(e) en [Votre programme]</div>
                <div class="affiliation">Université de Sherbrooke</div>
            </div>
        </header>

        <!-- Navigation par onglets -->
        <nav class="nav-tabs">
            <div class="nav-tab active" onclick="showSection('about')">À propos</div>
            <div class="nav-tab" onclick="showSection('education')">Formation</div>
            <div class="nav-tab" onclick="showSection('projects')">Projets</div>
            <div class="nav-tab" onclick="showSection('skills')">Compétences</div>
            <div class="nav-tab" onclick="showSection('contact')">Contact</div>
        </nav>

        <!-- Contenu principal -->
        <div class="content">
            <!-- Section À propos -->
            <section id="about" class="section">
                <h2>À propos de moi</h2>
                <p>
                    Bonjour ! Je suis étudiant(e) à l'<a href="https://www.usherbrooke.ca" target="_blank">Université de Sherbrooke</a>, 
                    actuellement inscrit(e) dans le programme de [Votre programme]. Passionné(e) par [vos domaines d'intérêt], 
                    je m'efforce constamment d'approfondir mes connaissances et de développer mes compétences.
                </p>
                <p>
                    Mon parcours académique m'a permis de travailler sur divers projets stimulants et de collaborer avec 
                    des équipes talentueuses. Je suis particulièrement intéressé(e) par [domaines spécifiques] et j'aspire 
                    à contribuer à [vos objectifs professionnels].
                </p>
                <p>
                    En dehors de mes études, je m'intéresse à [vos hobbies/intérêts personnels]. Je crois fermement en 
                    l'apprentissage continu et en l'importance de rester curieux face aux nouvelles technologies et méthodologies.
                </p>

                <!-- Liens sociaux -->
                <div class="social-links">
                    <a href="https://github.com/votre-username" target="_blank" class="social-link">
                        <span class="icon">🐙</span>
                        <span>GitHub</span>
                    </a>
                    <a href="https://linkedin.com/in/votre-profil" target="_blank" class="social-link">
                        <span class="icon">💼</span>
                        <span>LinkedIn</span>
                    </a>
                    <a href="mailto:votre.email@usherbrooke.ca" class="social-link">
                        <span class="icon">✉️</span>
                        <span>Email</span>
                    </a>
                    <a href="cv.pdf" target="_blank" class="social-link">
                        <span class="icon">📄</span>
                        <span>CV (PDF)</span>
                    </a>
                </div>
            </section>

            <!-- Section Formation -->
            <section id="education" class="section hidden">
                <h2>Parcours académique</h2>
                <div class="timeline">
                    <div class="timeline-item">
                        <h3>Baccalauréat en [Votre programme]</h3>
                        <div class="timeline-date">20XX - Présent</div>
                        <p>Université de Sherbrooke, Québec, Canada</p>
                        <p><strong>Cours pertinents :</strong> [Liste de cours importants]</p>
                        <p><strong>Moyenne cumulative :</strong> [Votre moyenne] / 4.3</p>
                    </div>

                    <div class="timeline-item">
                        <h3>DEC en [Programme collégial]</h3>
                        <div class="timeline-date">20XX - 20XX</div>
                        <p>[Nom du cégep], Québec, Canada</p>
                        <p>Diplôme d'études collégiales avec mention d'excellence</p>
                    </div>

                    <div class="timeline-item">
                        <h3>Diplôme d'études secondaires</h3>
                        <div class="timeline-date">20XX - 20XX</div>
                        <p>[Nom de l'école secondaire]</p>
                    </div>
                </div>
            </section>

            <!-- Section Projets -->
            <section id="projects" class="section hidden">
                <h2>Projets & Réalisations</h2>
                
                <div class="card">
                    <h3>🚀 Projet 1 : [Nom du projet]</h3>
                    <div class="card-meta">Technologies : Python, Flask, PostgreSQL | Date : Automne 20XX</div>
                    <p>
                        Description détaillée de votre projet. Expliquez le problème que vous avez résolu, 
                        les technologies utilisées, et les résultats obtenus. N'hésitez pas à mentionner les défis 
                        rencontrés et comment vous les avez surmontés.
                    </p>
                    <p><strong>Lien :</strong> <a href="https://github.com/votre-username/projet1" target="_blank">Voir sur GitHub</a></p>
                </div>

                <div class="card">
                    <h3>💡 Projet 2 : [Nom du projet]</h3>
                    <div class="card-meta">Technologies : React, Node.js, MongoDB | Date : Hiver 20XX</div>
                    <p>
                        Description de votre deuxième projet. Mettez en évidence vos contributions principales, 
                        les compétences développées, et l'impact du projet.
                    </p>
                    <p><strong>Lien :</strong> <a href="https://github.com/votre-username/projet2" target="_blank">Voir sur GitHub</a></p>
                </div>

                <div class="card">
                    <h3>🔬 Projet 3 : [Nom du projet]</h3>
                    <div class="card-meta">Technologies : Java, Spring Boot, Docker | Date : Printemps 20XX</div>
                    <p>
                        Description de votre troisième projet. Incluez des métriques si possible (performance, 
                        nombre d'utilisateurs, amélioration des performances, etc.).
                    </p>
                    <p><strong>Lien :</strong> <a href="https://github.com/votre-username/projet3" target="_blank">Voir sur GitHub</a></p>
                </div>
            </section>

            <!-- Section Compétences -->
            <section id="skills" class="section hidden">
                <h2>Compétences techniques</h2>
                
                <div class="skills-grid">
                    <div class="skill-category">
                        <h3>💻 Programmation</h3>
                        <div class="skill-tag">Python</div>
                        <div class="skill-tag">Java</div>
                        <div class="skill-tag">C++</div>
                        <div class="skill-tag">JavaScript</div>
                        <div class="skill-tag">TypeScript</div>
                    </div>

                    <div class="skill-category">
                        <h3>🌐 Web</h3>
                        <div class="skill-tag">HTML/CSS</div>
                        <div class="skill-tag">React</div>
                        <div class="skill-tag">Node.js</div>
                        <div class="skill-tag">Vue.js</div>
                        <div class="skill-tag">Django</div>
                    </div>

                    <div class="skill-category">
                        <h3>🗄️ Bases de données</h3>
                        <div class="skill-tag">PostgreSQL</div>
                        <div class="skill-tag">MongoDB</div>
                        <div class="skill-tag">MySQL</div>
                        <div class="skill-tag">Redis</div>
                    </div>

                    <div class="skill-category">
                        <h3>🛠️ Outils & DevOps</h3>
                        <div class="skill-tag">Git</div>
                        <div class="skill-tag">Docker</div>
                        <div class="skill-tag">Linux</div>
                        <div class="skill-tag">AWS</div>
                        <div class="skill-tag">CI/CD</div>
                    </div>

                    <div class="skill-category">
                        <h3>📊 Data & ML</h3>
                        <div class="skill-tag">Pandas</div>
                        <div class="skill-tag">NumPy</div>
                        <div class="skill-tag">Scikit-learn</div>
                        <div class="skill-tag">TensorFlow</div>
                    </div>

                    <div class="skill-category">
                        <h3>📝 Autres</h3>
                        <div class="skill-tag">LaTeX</div>
                        <div class="skill-tag">Markdown</div>
                        <div class="skill-tag">Figma</div>
                        <div class="skill-tag">Agile/Scrum</div>
                    </div>
                </div>
            </section>

            <!-- Section Contact -->
            <section id="contact" class="section hidden">
                <h2>Me contacter</h2>
                <p>
                    Je suis toujours intéressé(e) par de nouvelles opportunités, collaborations, ou simplement 
                    pour échanger sur des sujets qui nous passionnent. N'hésitez pas à me contacter !
                </p>

                <div class="contact-card">
                    <h3>Coordonnées</h3>
                    
                    <div class="contact-item">
                        <span class="icon">✉️</span>
                        <div>
                            <strong>Email</strong><br>
                            <a href="mailto:votre.email@usherbrooke.ca">votre.email@usherbrooke.ca</a>
                        </div>
                    </div>

                    <div class="contact-item">
                        <span class="icon">🐙</span>
                        <div>
                            <strong>GitHub</strong><br>
                            <a href="https://github.com/votre-username" target="_blank">github.com/votre-username</a>
                        </div>
                    </div>

                    <div class="contact-item">
                        <span class="icon">💼</span>
                        <div>
                            <strong>LinkedIn</strong><br>
                            <a href="https://linkedin.com/in/votre-profil" target="_blank">linkedin.com/in/votre-profil</a>
                        </div>
                    </div>

                    <div class="contact-item">
                        <span class="icon">📍</span>
                        <div>
                            <strong>Localisation</strong><br>
                            Sherbrooke, Québec, Canada
                        </div>
                    </div>
                </div>
            </section>
        </div>

        <!-- Pied de page -->
        <footer class="footer">
            <p>© 2025 Votre Nom. Tous droits réservés.</p>
            <p>Dernière mise à jour : Octobre 2025</p>
        </footer>
    </div>

    <script>
        // Fonction pour changer de section
        function showSection(sectionId) {
            // Cacher toutes les sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.add('hidden');
            });

            // Retirer la classe active de tous les onglets
            const tabs = document.querySelectorAll('.nav-tab');
            tabs.forEach(tab => {
                tab.classList.remove('active');
            });

            // Afficher la section sélectionnée
            const selectedSection = document.getElementById(sectionId);
            if (selectedSection) {
                selectedSection.classList.remove('hidden');
            }

            // Ajouter la classe active à l'onglet cliqué
            event.target.classList.add('active');

            // Scroll smooth vers le haut du contenu
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Animation au chargement
        document.addEventListener('DOMContentLoaded', function() {
            // Ajouter des animations d'entrée progressives
            const elements = document.querySelectorAll('.card, .skill-category, .timeline-item');
            elements.forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                setTimeout(() => {
                    el.style.transition = 'all 0.5s ease';
                    el.style.opacity = '1';
                    el.style.transform = 'translateY(0)';
                }, index * 100);
            });
        });

        // Effet de parallaxe subtil sur la bannière
        window.addEventListener('scroll', function() {
            const banner = document.querySelector('.header-banner');
            const scrolled = window.pageYOffset;
            banner.style.transform = `translateY(${scrolled * 0.5}px)`;
        });
    </script>
</body>
</html>
