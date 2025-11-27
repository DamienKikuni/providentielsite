<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Providentiel Group - Solutions Intégrées Numériques & Technologiques</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        /* RESET ET VARIABLES */
        :root {
            --primary: #1a365d;
            --secondary: #2d3748;
            --accent: #d69e2e;
            --light: #f7fafc;
            --dark: #2d3748;
            --success: #38a169;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: var(--dark);
        }
        
        /* HEADER */
        header {
            background: var(--primary);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: background 0.3s;
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        /* HERO SECTION */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 150px 0 100px;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero-tagline {
            font-size: 1.5rem;
            color: var(--accent);
            margin-bottom: 1rem;
            font-weight: bold;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .cta-button {
            display: inline-block;
            background: var(--accent);
            color: var(--primary);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(214, 158, 46, 0.4);
        }
        
        /* SECTEURS SECTION */
        .secteurs {
            padding: 80px 0;
            background: var(--light);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
            font-size: 2.5rem;
        }
        
        .section-subtitle {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--secondary);
            font-size: 1.2rem;
        }
        
        .secteurs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .secteur-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
            border-left: 4px solid var(--accent);
        }
        
        .secteur-card:hover {
            transform: translateY(-5px);
        }
        
        .secteur-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
        }
        
        /* SERVICES SECTION */
        .services {
            padding: 80px 0;
            background: white;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: var(--light);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s;
            border-top: 4px solid var(--primary);
            text-decoration: none;
            color: inherit;
            display: block;
            cursor: pointer;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
            border-top-color: var(--accent);
            text-decoration: none;
            color: inherit;
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .service-card:hover .service-icon {
            color: var(--accent);
        }
        
        /* CONTACT SECTION */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--light) 0%, white 100%);
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: start;
        }
        
        .contact-info {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: var(--light);
            border-radius: 5px;
        }
        
        .contact-icon {
            font-size: 1.5rem;
            margin-right: 1rem;
            color: var(--primary);
        }
        
        .contact-form {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
            color: var(--primary);
        }
        
        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: 2px solid #e2e8f0;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--accent);
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        /* FOOTER */
        footer {
            background: var(--secondary);
            color: white;
            padding: 3rem 0 2rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h3 {
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 0.5rem;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--primary);
            color: white;
            border-radius: 50%;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-link:hover {
            background: var(--accent);
            transform: translateY(-2px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }
        
        /* MODAL */
        .modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }
        
        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 2rem;
            border-radius: 10px;
            width: 90%;
            max-width: 600px;
            position: relative;
            animation: modalSlideIn 0.3s ease-out;
        }
        
        @keyframes modalSlideIn {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .close-modal {
            position: absolute;
            right: 1rem;
            top: 1rem;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--dark);
        }
        
        .close-modal:hover {
            color: var(--accent);
        }
        
        /* RESPONSIVE */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero-tagline {
                font-size: 1.2rem;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .modal-content {
                margin: 10% auto;
                width: 95%;
            }
        }
        
        /* ANIMATIONS */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .fade-in {
            animation: fadeInUp 0.6s ease-out;
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header>
        <nav class="nav-container">
            <div class="logo">PROVIDENTIEL GROUP</div>
            <ul class="nav-links">
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#secteurs">Secteurs</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="accueil">
        <div class="hero-content fade-in">
            <h1>Providentiel Group</h1>
            <div class="hero-tagline">Votre Partenaire Digital & Technologique</div>
            <p>Expertise multisectorielle alliant innovation numérique, développement technologique et accompagnement stratégique pour votre réussite</p>
            <a href="#contact" class="cta-button">Démarrer un Projet</a>
        </div>
    </section>

    <!-- SECTEURS SECTION -->
    <section class="secteurs" id="secteurs">
        <div class="container">
            <h2 class="section-title">Secteurs d'Activité</h2>
            <p class="section-subtitle">Une expertise diversifiée au service de votre croissance</p>
            <div class="secteurs-grid">
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">💻</div>
                    <h3>Numérique</h3>
                    <p>Transformation digitale et solutions innovantes</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🚀</div>
                    <h3>Technologique</h3>
                    <p>Technologies de pointe et innovation</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🔌</div>
                    <h3>Électronique</h3>
                    <p>Solutions électroniques avancées</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🏥</div>
                    <h3>Santé</h3>
                    <p>Innovation médicale et techno-santé</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">📈</div>
                    <h3>Économique</h3>
                    <p>Stratégies de croissance économique</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">👔</div>
                    <h3>Professionnel</h3>
                    <p>Services aux professionnels</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🎓</div>
                    <h3>Éducation</h3>
                    <p>Formation et EdTech</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🌱</div>
                    <h3>Développement</h3>
                    <p>Solutions de développement durable</p>
                </div>
                <div class="secteur-card fade-in">
                    <div class="secteur-icon">🤝</div>
                    <h3>Social</h3>
                    <p>Impact social et communautaire</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVICES SECTION -->
    <section class="services" id="services">
        <div class="container">
            <h2 class="section-title">Nos Services</h2>
            <p class="section-subtitle">Des solutions complètes pour tous vos besoins</p>
            <div class="services-grid">
                <a class="service-card fade-in" data-service="formation">
                    <div class="service-icon">🎓</div>
                    <h3>Formation Domaine Numérique</h3>
                    <p>Programmes de formation adaptés aux métiers du numérique et aux technologies émergentes</p>
                    <small style="color: var(--accent); margin-top: 1rem; display: block;">Cliquez pour en savoir plus →</small>
                </a>
                <a class="service-card fade-in" data-service="maintenance">
                    <div class="service-icon">🔧</div>
                    <h3>Maintenance Électronique</h3>
                    <p>Service de maintenance préventive et corrective pour tous vos appareils électroniques</p>
                    <small style="color: var(--accent); margin-top: 1rem; display: block;">Cliquez pour en savoir plus →</small>
                </a>
                <a class="service-card fade-in" data-service="vente">
                    <div class="service-icon">💻</div>
                    <h3>Vente de Matériel Informatique</h3>
                    <p>Distribution de matériel informatique de qualité pour professionnels et particuliers</p>
                    <small style="color: var(--accent); margin-top: 1rem; display: block;">Cliquez pour en savoir plus →</small>
                </a>
                <a class="service-card fade-in" data-service="consultation">
                    <div class="service-icon">📊</div>
                    <h3>Consultation aux Entreprises</h3>
                    <p>Accompagnement stratégique et conseil en transformation digitale pour les entreprises</p>
                    <small style="color: var(--accent); margin-top: 1rem; display: block;">Cliquez pour en savoir plus →</small>
                </a>
                <a class="service-card fade-in" data-service="startup">
                    <div class="service-icon">🚀</div>
                    <h3>Accompagnement StartUp</h3>
                    <p>Support complet pour le lancement et le développement de votre startup</p>
                    <small style="color: var(--accent); margin-top: 1rem; display: block;">Cliquez pour en savoir plus →</small>
                </a>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">Contactez-Nous</h2>
            <p class="section-subtitle">Prêt à transformer vos idées en réalité ?</p>
            
            <div class="contact-container">
                <!-- INFORMATIONS DE CONTACT -->
                <div class="contact-info fade-in">
                    <h3>Nos Coordonnées</h3>
                    <div class="contact-item">
                        <div class="contact-icon">📞</div>
                        <div>
                            <strong>Téléphone</strong><br>
                            +243 829 333 231
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📧</div>
                        <div>
                            <strong>Email</strong><br>
                            kikunidamien@gmail.com
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <strong>Adresse</strong><br>
                            443, 11e Rue, Industriel<br>
                            Limete, Kinshasa - RDC
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">🕒</div>
                        <div>
                            <strong>Heures d'Ouverture</strong><br>
                            Lun - Ven: 8h00 - 18h00<br>
                            Sam: 9h00 - 13h00
                        </div>
                    </div>
                </div>
                
                <!-- FORMULAIRE DE CONTACT -->
                <form class="contact-form fade-in">
                    <div class="form-group">
                        <label for="name">Nom Complet *</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email *</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Téléphone</label>
                        <input type="tel" id="phone">
                    </div>
                    <div class="form-group">
                        <label for="service">Service Intéressé</label>
                        <select id="service">
                            <option value="">Sélectionnez un service</option>
                            <option value="formation">Formation Numérique</option>
                            <option value="maintenance">Maintenance Électronique</option>
                            <option value="vente">Vente Matériel Informatique</option>
                            <option value="consultation">Consultation Entreprises</option>
                            <option value="startup">Accompagnement StartUp</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Message *</label>
                        <textarea id="message" placeholder="Décrivez votre projet ou demande..." required></textarea>
                    </div>
                    <button type="submit" class="cta-button">Envoyer le Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Providentiel Group</h3>
                    <p>Votre partenaire de confiance dans les domaines numérique, technologique et du développement.</p>
                    <div class="social-links">
                        <!-- REMPLACEZ LES # PAR VOS VRAIS LIENS -->
                        <a href="#" class="social-link" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="social-link" target="_blank">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="social-link" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="#" class="social-link" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="social-link" target="_blank">
                            <i class="fab fa-whatsapp"></i>
                        </a>
                    </div>
                </div>
                <div class="footer-section">
                    <h3>Services</h3>
                    <ul>
                        <li>Formation Numérique</li>
                        <li>Maintenance Électronique</li>
                        <li>Vente Matériel Informatique</li>
                        <li>Consultation Entreprises</li>
                        <li>Accompagnement StartUp</li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact Rapide</h3>
                    <p>📞 +243 829 333 231</p>
                    <p>📧 kikunidamien@gmail.com</p>
                    <p>📍 Limete, Kinshasa - RDC</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Providentiel Group. Tous droits réservés.</p>
            </div>
        </div>
    </footer>

    <!-- MODAL POUR LES SERVICES -->
    <div id="serviceModal" class="modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <div id="modal-body">
                <!-- Le contenu du service sera injecté ici -->
            </div>
        </div>
    </div>

    <script>
        // Smooth scroll pour les liens d'ancrage
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Animation du header au scroll
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(26, 54, 93, 0.95)';
                header.style.backdropFilter = 'blur(10px)';
            } else {
                header.style.background = 'var(--primary)';
                header.style.backdropFilter = 'none';
            }
        });
        
        // Animation au défilement
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.6s ease-out forwards';
                }
            });
        }, observerOptions);
        
        // Observer les éléments à animer
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });
        
        // Gestion du formulaire
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Merci pour votre message ! Nous vous contacterons très rapidement.');
            this.reset();
        });

        // MODAL POUR LES SERVICES
        const modal = document.getElementById('serviceModal');
        const modalBody = document.getElementById('modal-body');
        const closeModal = document.querySelector('.close-modal');

        // Données détaillées pour chaque service
        const servicesData = {
            formation: {
                title: "Formation Domaine Numérique",
                description: "Des programmes de formation complets et adaptés aux besoins du marché actuel.",
                details: [
                    "Formation en développement web et mobile",
                    "Cours de programmation (Python, JavaScript, Java)",
                    "Formation en cybersécurité",
                    "Ateliers d'IA et Machine Learning",
                    "Certifications reconnues internationalement"
                ],
                duree: "De 2 semaines à 6 mois",
                prix: "À partir de 150€"
            },
            maintenance: {
                title: "Maintenance Électronique",
                description: "Service complet de maintenance pour tous vos équipements électroniques.",
                details: [
                    "Maintenance préventive et corrective",
                    "Réparation d'ordinateurs et smartphones",
                    "Maintenance de réseaux informatiques",
                    "Support technique à distance",
                    "Contrats de maintenance annuels"
                ],
                duree: "Intervention sous 24h-48h",
                prix: "Devis gratuit sur demande"
            },
            vente: {
                title: "Vente de Matériel Informatique",
                description: "Distribution de matériel informatique de qualité pour tous vos besoins.",
                details: [
                    "Ordinateurs portables et de bureau",
                    "Périphériques et accessoires",
                    "Équipements réseau et serveurs",
                    "Matériel pour gamers et créateurs",
                    "Solutions sur mesure pour entreprises"
                ],
                duree: "Livraison sous 2-5 jours",
                prix: "Prix compétitifs"
            },
            consultation: {
                title: "Consultation aux Entreprises",
                description: "Accompagnement stratégique pour la transformation digitale de votre entreprise.",
                details: [
                    "Audit digital et stratégique",
                    "Transformation des processus métiers",
                    "Optimisation des coûts IT",
                    "Stratégie de présence en ligne",
                    "Formation des équipes"
                ],
                duree: "Projets de 1 à 6 mois",
                prix: "Devis personnalisé"
            },
            startup: {
                title: "Accompagnement StartUp",
                description: "Support complet du concept à la réalisation pour votre startup.",
                details: [
                    "Étude de marché et business plan",
                    "Développement du MVP",
                    "Recherche de financement",
                    "Stratégie marketing et commerciale",
                    "Mentorat et networking"
                ],
                duree: "Accompagnement sur 3-12 mois",
                prix: "Forfaits adaptés"
            }
        };

        // Gestion des clics sur les services
        document.querySelectorAll('.service-card').forEach(card => {
            card.addEventListener('click', function(e) {
                e.preventDefault();
                const serviceType = this.getAttribute('data-service');
                const service = servicesData[serviceType];
                
                if (service) {
                    modalBody.innerHTML = `
                        <h2 style="color: var(--primary); margin-bottom: 1rem;">${service.title}</h2>
                        <p style="margin-bottom: 1.5rem; font-size: 1.1rem;">${service.description}</p>
                        
                        <h3 style="color: var(--accent); margin-bottom: 1rem;">Détails du service :</h3>
                        <ul style="margin-bottom: 1.5rem; padding-left: 1.5rem;">
                            ${service.details.map(detail => `<li style="margin-bottom: 0.5rem;">${detail}</li>`).join('')}
                        </ul>
                        
                        <div style="background: var(--light); padding: 1rem; border-radius: 5px; margin-bottom: 1.5rem;">
                            <p><strong>Durée :</strong> ${service.duree}</p>
                            <p><strong>Tarif :</strong> ${service.prix}</p>
                        </div>
                        
                        <button class="cta-button" onclick="closeServiceModal(); document.querySelector('#contact').scrollIntoView({behavior: 'smooth'});">
                            Demander un devis
                        </button>
                    `;
                    modal.style.display = 'block';
                }
            });
        });

        // Fermer le modal
        closeModal.addEventListener('click', closeServiceModal);

        function closeServiceModal() {
            modal.style.display = 'none';
        }

        // Fermer le modal en cliquant à l'extérieur
        window.addEventListener('click', function(e) {
            if (e.target === modal) {
                closeServiceModal();
            }
        });
    </script>
</body>
</html>
