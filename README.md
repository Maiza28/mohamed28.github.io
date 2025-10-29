<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed - Page Professionnelle</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.7;
            color: #333;
            background-color: #fff;
            max-width: 900px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        header {
            margin-bottom: 50px;
            padding-bottom: 30px;
            border-bottom: 1px solid #ddd;
        }

        h1 {
            font-size: 2.2em;
            font-weight: 400;
            margin-bottom: 25px;
            color: #2c3e50;
        }

        nav {
            margin-top: 25px;
        }

        nav a {
            color: #3498db;
            text-decoration: none;
            margin-right: 25px;
            font-size: 1em;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #2980b9;
            text-decoration: underline;
        }

        section {
            margin-bottom: 50px;
        }

        h2 {
            font-size: 1.6em;
            font-weight: 400;
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }

        p {
            margin-bottom: 15px;
            text-align: justify;
        }

        .interests {
            font-style: italic;
            color: #555;
            margin-bottom: 20px;
        }

        .publication {
            margin-bottom: 30px;
            padding: 20px;
            background-color: #f9f9f9;
            border-left: 3px solid #3498db;
            transition: background-color 0.3s ease;
        }

        .publication:hover {
            background-color: #f0f0f0;
        }

        .publication h3 {
            font-size: 1.2em;
            font-weight: 500;
            color: #2c3e50;
            margin-bottom: 10px;
        }

        .publication .meta {
            font-size: 0.9em;
            color: #777;
            margin-bottom: 10px;
        }

        .publication p {
            font-size: 0.95em;
            color: #555;
        }

        .links {
            margin-top: 10px;
        }

        .links a {
            color: #3498db;
            text-decoration: none;
            margin-right: 15px;
            font-size: 0.9em;
        }

        .links a:hover {
            text-decoration: underline;
        }

        .contact-info {
            background-color: #f9f9f9;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
        }

        .contact-info a {
            color: #3498db;
            text-decoration: none;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        footer {
            margin-top: 60px;
            padding-top: 20px;
            border-top: 1px solid #ddd;
            text-align: center;
            color: #777;
            font-size: 0.9em;
        }

        @media (max-width: 600px) {
            body {
                padding: 20px 15px;
            }

            h1 {
                font-size: 1.8em;
            }

            nav a {
                display: block;
                margin-bottom: 10px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Mohamed</h1>
        
        <nav>
            <a href="#about">À propos</a>
            <a href="#research">Recherche</a>
            <a href="#publications">Publications</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section id="about">
        <h2>À propos</h2>
        <p>
            Je suis [votre titre] à [votre institution]. Mes travaux se concentrent sur [domaine principal]. 
            Précédemment, j'ai été [poste précédent] à [institution précédente] dans le groupe de [nom du superviseur/collaborateur]. 
            Avant cela, j'ai obtenu mon [diplôme] à [université] sous la supervision de [nom du superviseur].
        </p>
    </section>

    <section id="research">
        <h2>Intérêts de recherche</h2>
        <p class="interests">
            Domaine 1 ; domaine 2 ; domaine 3 ; domaine 4 ; domaine 5 ; domaine 6 ; 
            domaine 7 ; domaine 8 ; domaine 9 ; domaine 10 ; domaine 11 ; domaine 12.
        </p>
        <p>
            [Ajoutez ici une description plus détaillée de vos recherches, vos projets en cours, 
            et vos objectifs scientifiques. Expliquez l'impact de votre travail et ce qui vous passionne 
            dans votre domaine.]
        </p>
    </section>

    <section id="publications">
        <h2>Publications et projets</h2>
        
        <div class="publication">
            <h3>Titre de la publication ou du projet 1</h3>
            <div class="meta">Co-auteurs (si applicable) | Nom de la revue/conférence | Année</div>
            <p>
                Description ou résumé de votre publication/projet. Expliquez les contributions principales, 
                la méthodologie utilisée, et les résultats obtenus. Cette section permet au lecteur de 
                comprendre rapidement l'essence de votre travail.
            </p>
            <div class="links">
                <a href="#">PDF</a>
                <a href="#">arXiv</a>
                <a href="#">GitHub</a>
                <a href="#">DOI</a>
            </div>
        </div>

        <div class="publication">
            <h3>Titre de la publication ou du projet 2</h3>
            <div class="meta">Co-auteurs (si applicable) | Nom de la revue/conférence | Année</div>
            <p>
                Description ou résumé de votre deuxième publication/projet. Mettez en évidence 
                les aspects innovants et l'importance de ce travail dans votre domaine.
            </p>
            <div class="links">
                <a href="#">PDF</a>
                <a href="#">arXiv</a>
                <a href="#">GitHub</a>
            </div>
        </div>

        <div class="publication">
            <h3>Titre de la publication ou du projet 3</h3>
            <div class="meta">Co-auteurs (si applicable) | Nom de la revue/conférence | Année</div>
            <p>
                Description ou résumé de votre troisième publication/projet. Expliquez comment 
                ce travail s'inscrit dans votre programme de recherche global.
            </p>
            <div class="links">
                <a href="#">PDF</a>
                <a href="#">Lien externe</a>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <div class="contact-info">
            <p><strong>Email :</strong> <a href="mailto:votre.email@institution.ca">votre.email@institution.ca</a></p>
            <p><strong>Bureau :</strong> Numéro de bureau, Bâtiment</p>
            <p><strong>Téléphone :</strong> +1 (XXX) XXX-XXXX</p>
            <p><strong>Adresse :</strong> Département, Institution, Adresse complète</p>
            <p style="margin-top: 15px;">
                <a href="https://github.com/mohamed28" target="_blank">GitHub</a> | 
                <a href="#" target="_blank">Google Scholar</a> | 
                <a href="#" target="_blank">LinkedIn</a> | 
                <a href="#" target="_blank">ORCID</a>
            </p>
        </div>
    </section>

    <footer>
        <p>&copy; 2025 Mohamed. Tous droits réservés.</p>
    </footer>
</body>
</html>
