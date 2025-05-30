<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Farmacia Nieto - Elaboración Magistral Personalizada</title>
    <meta name="description" content="Farmacia especializada en medicamentos magistrales, homeopatía, dermocosmética y medicina natural. Patricia Victoria Nieto, 28+ años de experiencia.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --verde-principal: #7fb069;
            --verde-oscuro: #557153;
            --verde-claro: #a4d17a;
            --verde-suave: #f0f8ec;
            --texto-oscuro: #2d3436;
            --texto-medio: #636e72;
            --texto-claro: #74b9ff;
            --blanco: #ffffff;
            --gris-claro: #f8f9fa;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--texto-oscuro);
            background-color: var(--gris-claro);
        }

        /* Header */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(15px);
            z-index: 1000;
            padding: 1rem 0;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        }

        .navbar-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand {
            display: flex;
            align-items: center;
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--verde-principal);
            text-decoration: none;
        }

        .brand-icon {
            width: 40px;
            height: 40px;
            background: var(--verde-principal);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 0.8rem;
            color: white;
            font-size: 20px;
        }

        .menu {
            display: flex;
            list-style: none;
            gap: 2.5rem;
            margin: 0;
        }

        .menu-link {
            color: var(--texto-medio);
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 0;
            position: relative;
            transition: color 0.3s ease;
        }

        .menu-link:hover {
            color: var(--verde-principal);
        }

        .menu-link::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--verde-principal);
            transition: width 0.3s ease;
        }

        .menu-link:hover::after {
            width: 100%;
        }

        .cta-button {
            background: var(--verde-principal);
            color: white;
            padding: 0.8rem 1.8rem;
            border: none;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(127, 176, 105, 0.3);
        }

        .cta-button:hover {
            background: var(--verde-oscuro);
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(127, 176, 105, 0.4);
        }

        /* Hero Section */
        .hero-section {
            background: linear-gradient(135deg, var(--verde-suave) 0%, var(--blanco) 100%);
            padding: 8rem 2rem 6rem;
            text-align: center;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .hero-title {
            font-size: clamp(2.5rem, 5vw, 4.5rem);
            font-weight: 800;
            color: var(--verde-oscuro);
            margin-bottom: 1.5rem;
            line-height: 1.1;
        }

        .hero-subtitle {
            font-size: clamp(1.3rem, 3vw, 2rem);
            color: var(--verde-principal);
            margin-bottom: 2rem;
            font-weight: 600;
        }

        .hero-text {
            font-size: 1.2rem;
            color: var(--texto-medio);
            margin-bottom: 3rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            line-height: 1.7;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 4rem;
        }

        .btn-primary {
            background: var(--verde-principal);
            color: white;
            padding: 1.2rem 2.5rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            transition: all 0.3s ease;
            box-shadow: 0 6px 20px rgba(127, 176, 105, 0.3);
        }

        .btn-primary:hover {
            background: var(--verde-oscuro);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(127, 176, 105, 0.4);
        }

        .btn-outline {
            background: transparent;
            color: var(--verde-principal);
            padding: 1.2rem 2.5rem;
            border: 2px solid var(--verde-principal);
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            transition: all 0.3s ease;
        }

        .btn-outline:hover {
            background: var(--verde-principal);
            color: white;
            transform: translateY(-3px);
        }

        /* Tarjeta Profesional */
        .professional-info {
            background: white;
            border-radius: 25px;
            padding: 3rem;
            max-width: 700px;
            margin: 0 auto;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(127, 176, 105, 0.2);
            position: relative;
            overflow: hidden;
        }

        .professional-info::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, var(--verde-principal), var(--verde-claro), var(--verde-principal));
        }

        .director-badge {
            display: inline-block;
            background: var(--verde-suave);
            color: var(--verde-principal);
            padding: 0.5rem 1.5rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
        }

        .director-name {
            font-size: 2.2rem;
            font-weight: 700;
            color: var(--verde-oscuro);
            margin-bottom: 0.5rem;
        }

        .director-title {
            font-size: 1.2rem;
            color: var(--verde-principal);
            margin-bottom: 2rem;
            font-weight: 500;
        }

        .experience-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin: 2rem 0;
            padding: 2rem 0;
            border-top: 1px solid rgba(127, 176, 105, 0.2);
            border-bottom: 1px solid rgba(127, 176, 105, 0.2);
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            display: block;
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--verde-principal);
            line-height: 1;
        }

        .stat-text {
            font-size: 0.9rem;
            color: var(--texto-medio);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 0.5rem;
            font-weight: 500;
        }

        .qualifications {
            margin-top: 2rem;
        }

        .qualification-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            font-size: 1rem;
            color: var(--texto-medio);
        }

        .qualification-item .icon {
            margin-right: 1rem;
            font-size: 1.2rem;
        }

        /* Sección de Servicios */
        .services-section {
            padding: 6rem 2rem;
            background: white;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title {
            font-size: clamp(2.2rem, 4vw, 3.5rem);
            font-weight: 700;
            color: var(--verde-oscuro);
            margin-bottom: 1rem;
        }

        .section-description {
            font-size: 1.2rem;
            color: var(--texto-medio);
            max-width: 600px;
            margin: 0 auto;
        }

        .services-grid {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }

        .service-item {
            background: var(--gris-claro);
            border-radius: 20px;
            padding: 2.5rem;
            text-align: center;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            position: relative;
            overflow: hidden;
        }

        .service-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: var(--verde-principal);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .service-item:hover::before {
            transform: scaleX(1);
        }

        .service-item:hover {
            background: white;
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            border-color: var(--verde-principal);
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            display: block;
            transition: transform 0.3s ease;
        }

        .service-item:hover .service-icon {
            transform: scale(1.1);
        }

        .service-name {
            font-size: 1.4rem;
            font-weight: 600;
            color: var(--verde-oscuro);
            margin-bottom: 1rem;
        }

        .service-description {
            color: var(--texto-medio);
            line-height: 1.6;
        }

        /* Sección de Contacto */
        .contact-section {
            padding: 6rem 2rem;
            background: var(--verde-oscuro);
            color: white;
        }

        .contact-container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .contact-info h2 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            font-weight: 700;
        }

        .contact-text {
            font-size: 1.2rem;
            margin-bottom: 3rem;
            opacity: 0.9;
            line-height: 1.6;
        }

        .contact-methods {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-method {
            display: flex;
            align-items: center;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .contact-method:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateX(8px);
            border-color: var(--verde-claro);
        }

        .contact-icon {
            font-size: 1.8rem;
            margin-right: 1.5rem;
            width: 50px;
            text-align: center;
        }

        .contact-details h4 {
            font-size: 1.2rem;
            margin-bottom: 0.3rem;
        }

        .contact-details p {
            opacity: 0.9;
            font-size: 1rem;
        }

        .pharmacy-info {
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            padding: 3rem;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .pharmacy-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--verde-claro);
        }

        .pharmacy-details {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 2rem;
        }

        .pharmacy-details strong {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--verde-claro);
        }

        /* Footer */
        .footer {
            background: #2d3436;
            color: white;
            padding: 3rem 2rem 1.5rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            color: var(--verde-claro);
            margin-bottom: 1rem;
            font-size: 1.1rem;
        }

        .footer-section p {
            margin-bottom: 0.5rem;
            opacity: 0.8;
            font-size: 0.9rem;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            padding-top: 1.5rem;
            margin-top: 2rem;
            opacity: 0.7;
        }

        /* WhatsApp flotante */
        .whatsapp-fixed {
            position: fixed;
            bottom: 25px;
            right: 25px;
            width: 65px;
            height: 65px;
            background: #25d366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
            text-decoration: none;
            z-index: 1000;
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.4);
            transition: all 0.3s ease;
            animation: floating 3s ease-in-out infinite;
        }

        @keyframes floating {
            0% { transform: translate(0, 0px); }
            50% { transform: translate(0, -8px); }
            100% { transform: translate(0, 0px); }
        }

        .whatsapp-fixed:hover {
            transform: scale(1.1);
            box-shadow: 0 12px 35px rgba(37, 211, 102, 0.6);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .menu {
                display: none;
            }

            .hero-section {
                padding: 6rem 1rem 4rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn-primary,
            .btn-outline {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }

            .contact-container {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .services-grid {
                grid-template-columns: 1fr;
                gap: 1.5rem;
            }

            .experience-stats {
                grid-template-columns: 1fr;
                gap: 1rem;
            }

            .professional-info {
                padding: 2rem;
                margin: 0 1rem;
            }

            .footer-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
        }
    </style>
</head>

<body>
    <nav class="navbar">
        <div class="navbar-container">
            <a href="#inicio" class="brand">
                <div class="brand-icon">⚕️</div>
                Farmacia Nieto
            </a>
            <ul class="menu">
                <li><a href="#inicio" class="menu-link">Inicio</a></li>
                <li><a href="#servicios" class="menu-link">Servicios</a></li>
                <li><a href="#contacto" class="menu-link">Contacto</a></li>
            </ul>
            <a href="#contacto" class="cta-button" onclick="abrirWhatsApp()">💬 WhatsApp</a>
        </div>
    </nav>

    <section id="inicio" class="hero-section">
        <div class="hero-container">
            <h1 class="hero-title">Tu camino hacia el bienestar</h1>
            <p class="hero-subtitle">Elaboración Magistral Personalizada</p>
            <p class="hero-text">
                Bajo la dirección técnica de Patricia Victoria Nieto, farmacéutica con una larga trayectoria, 
                te ofrecemos productos de calidad y una atención de excelencia personalizada para cuidar tu salud.
            </p>
            
            <div class="hero-buttons">
                <a href="#servicios" class="btn-primary">
                    <span>🔍</span> Ver Servicios
                </a>
                <a href="#contacto" class="btn-outline">
                    <span>💬</span> Consultar Ahora
                </a>
            </div>

            <div class="professional-info">
                <div class="director-badge">Dirección Técnica</div>
                <h2 class="director-name">Patricia Victoria Nieto</h2>
                <p class="director-title">Farmacéutica Profesional</p>
                
                <div class="experience-stats">
                    <div class="stat-item">
                        <span class="stat-number">28+</span>
                        <span class="stat-text">Años</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">1000+</span>
                        <span class="stat-text">Pacientes</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">8</span>
                        <span class="stat-text">Especialidades</span>
                    </div>
                </div>
                
                <div class="qualifications">
                    <div class="qualification-item">
                        <span class="icon">🎓</span>
                        Matrícula del Colegio de Farmacéuticos
                    </div>
                    <div class="qualification-item">
                        <span class="icon">🔬</span>
                        Especialista en Elaboración Magistral
                    </div>
                    <div class="qualification-item">
                        <span class="icon">📍</span>
                        Universidad Nacional
                    </div>
                    <div class="qualification-item">
                        <span class="icon">⭐</span>
                        Desde 1996 al servicio de la comunidad
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="servicios" class="services-section">
        <div class="section-header">
            <h2 class="section-title">Nuestros Servicios</h2>
            <p class="section-description">
                Formulaciones personalizadas según las necesidades específicas de cada paciente
            </p>
        </div>
        
        <div class="services-grid">
            <div class="service-item">
                <span class="service-icon">💊</span>
                <h3 class="service-name">Medicina Ortomolecular</h3>
                <p class="service-description">Tratamientos personalizados basados en el equilibrio molecular óptimo para restaurar la salud natural del organismo.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">✨</span>
                <h3 class="service-name">Dermocosmética</h3>
                <p class="service-description">Productos especializados para el cuidado de la piel, formulados específicamente para cada tipo y necesidad.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🌿</span>
                <h3 class="service-name">Homeopatía</h3>
                <p class="service-description">Preparaciones homeopáticas tradicionales elaboradas con los más altos estándares de calidad y pureza.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🔬</span>
                <h3 class="service-name">Alopatía</h3>
                <p class="service-description">Medicamentos alopáticos preparados magistralmente según prescripción médica con máxima precisión.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🧘‍♀️</span>
                <h3 class="service-name">Fitoterapia</h3>
                <p class="service-description">Tratamientos naturales a base de plantas medicinales, respaldados por la tradición y la ciencia moderna.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🌸</span>
                <h3 class="service-name">Florales</h3>
                <p class="service-description">Esencias florales de Bach y otros sistemas para el equilibrio emocional y el bienestar integral.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🦠</span>
                <h3 class="service-name">Probióticos</h3>
                <p class="service-description">Formulaciones probióticas específicas para restaurar y mantener el equilibrio de la flora intestinal.</p>
            </div>
            
            <div class="service-item">
                <span class="service-icon">🧬</span>
                <h3 class="service-name">Hormonas Bioidénticas</h3>
                <p class="service-description">Terapias hormonales personalizadas con hormonas bioidénticas para el equilibrio hormonal natural.</p>
            </div>
        </div>
    </section>

    <section id="contacto" class="contact-section">
        <div class="contact-container">
            <div class="contact-info">
                <h2>Contactanos</h2>
                <p class="contact-text">
                    Para más asesoramiento y consultas, comunicate con nosotros. 
                    ¡Cuidamos de ti de manera personalizada!
                </p>
                
                <div class="contact-methods">
                    <div class="contact-method" onclick="abrirWhatsApp()">
                        <span class="contact-icon">📱</span>
                        <div class="contact-details">
                            <h4>WhatsApp</h4>
                            <p>(+54) 291432-7031</p>
                        </div>
                    </div>
                    
                    <div class="contact-method" onclick="window.open('mailto:farmacia.nieto@hotmail.com')">
                        <span class="contact-icon">✉️</span>
                        <div class="contact-details">
                            <h4>Email</h4>
                            <p>farmacia.nieto@hotmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-method">
                        <span class="contact-icon">📍</span>
                        <div class="contact-details">
                            <h4>Ubicación</h4>
                            <p>Bahía Blanca, Buenos Aires, Argentina</p>
                        </div>
                    </div>
                    
                    <div class="contact-method">
                        <span class="contact-icon">⏰</span>
                        <div class="contact-details">
                            <h4>Horarios de Atención</h4>
                            <p>Lun-Vie: 8:00-20:00 | Sáb: 8:00-13:00</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="pharmacy-info">
                <h3>¡Estamos aquí para ayudarte!</h3>
                <div class="pharmacy-details">
                    <strong>Patricia Victoria Nieto</strong>
                    <strong>Farmacéutica - Directora Técnica</strong>
                    28+ años de experiencia profesional<br>
                    Especialista en Elaboración Magistral<br>
                    Atención personalizada desde 1996<br>
                    Comprometidos con tu bienestar
                </div>
                <a href="#" class="btn-primary" onclick="abrirWhatsApp()">
                    <span>💬</span> Consultar por WhatsApp
                </a>
            </div>
        </div>
    </section>

    <footer class="footer">
        <div class="footer-bottom">
            <p>&copy; 2024 Farmacia Nieto. Todos los derechos reservados. | Diseñado con ❤️ para tu bienestar</p>
        </div>
    </footer>

    <a href="#" class="whatsapp-fixed" onclick="abrirWhatsApp()" aria-label="Contactar por WhatsApp">💬</a>

    <script>
        function abrirWhatsApp() {
            const mensaje = "Hola, me gustaría obtener información sobre sus servicios farmacéuticos. ¡Gracias!";
            const urlWhatsApp = `https://wa.me/5492914327031?text=${encodeURIComponent(mensaje)}`;
            window.open(urlWhatsApp, '_blank');
        }

        document.querySelectorAll('a[href^="#"]').forEach(enlace => {
            enlace.addEventListener('click', function (evento) {
                evento.preventDefault();
                const destino = document.querySelector(this.getAttribute('href'));
                if (destino) {
                    destino.scrollIntoView({ 
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.background = 'rgba(255, 255, 255, 0.98)';
                navbar.style.boxShadow = '0 8px 32px rgba(0, 0, 0, 0.12)';
            } else {
                navbar.style.background = 'rgba(255, 255, 255, 0.95)';
                navbar.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.08)';
            }
        });

        const observador = new IntersectionObserver((entradas) => {
            entradas.forEach((entrada, indice) => {
                if (entrada.isIntersecting) {
                    setTimeout(() => {
                        entrada.target.style.opacity = '1';
                        entrada.target.style.transform = 'translateY(0)';
                    }, indice * 150);
                    observador.unobserve(entrada.target);
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.service-item').forEach(tarjeta => {
            tarjeta.style.opacity = '0';
            tarjeta.style.transform = 'translateY(30px)';
            tarjeta.style.transition = 'all 0.6s ease';
            observador.observe(tarjeta);
        });

        const contadores = document.querySelectorAll('.stat-number');
        const observadorContadores = new IntersectionObserver((entradas) => {
            entradas.forEach(entrada => {
                if (entrada.isIntersecting) {
                    const contador = entrada.target;
                    const objetivo = parseInt(contador.textContent.replace(/\D/g, ''));
                    const incremento = objetivo / 60;
                    let actual = 0;
                    
                    const temporizador = setInterval(() => {
                        actual += incremento;
                        if (actual >= objetivo) {
                            actual = objetivo;
                            clearInterval(temporizador);
                        }
                        const sufijo = contador.textContent.includes('+') ? '+' : '';
                        contador.textContent = Math.floor(actual) + sufijo;
                    }, 25);
                    
                    observadorContadores.unobserve(contador);
                }
            });
        }, { threshold: 0.5 });

        contadores.forEach(contador => observadorContadores.observe(contador));

        document.addEventListener('DOMContentLoaded', function() {
            console.log('✅ Farmacia Nieto - Sitio cargado exitosamente');
        });
    </script>
</body>
</html>content">
            <div class="footer-section">
                <h4>Farmacia Nieto</h4>
                <p>Tu camino hacia el bienestar desde 1996.</p>
                <p>Elaboración magistral personalizada con la más alta calidad.</p>
                <p>Comprometidos con tu salud y bienestar.</p>
            </div>
            
            <div class="footer-section">
                <h4>Nuestros Servicios</h4>
                <p>Medicina Ortomolecular</p>
                <p>Dermocosmética Especializada</p>
                <p>Homeopatía y Alopatía</p>
                <p>Fitoterapia Natural</p>
                <p>Florales de Bach</p>
                <p>Probióticos y Hormonas Bioidénticas</p>
            </div>
            
            <div class="footer-section">
                <h4>Información de Contacto</h4>
                <p>📱 WhatsApp: (+54) 291432-7031</p>
                <p>✉️ farmacia.nieto@hotmail.com</p>
                <p>📍 Bahía Blanca, Buenos Aires, Argentina</p>
                <p>⏰ Lun-Vie: 8:00-20:00 | Sáb: 8:00-13:00</p>
            </div>
            
            <div class="footer-section">
                <h4>Dirección Profesional</h4>
                <p>Directora Técnica: Patricia Victoria Nieto</p>
                <p>Matrícula Profesional Habilitada</p>
                <p>28+ años de experiencia</p>
                <p>Especialista en Elaboración Magistral</p>
                <p>Universidad Nacional</p>
            </div>
        </div>
        
        <div class="footer-
