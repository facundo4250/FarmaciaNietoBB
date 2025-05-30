<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Farmacia Nieto - Tu camino hacia el bienestar</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #fafafa;
        }

        .header {
            position: fixed;
            top: 0;
            width: 100%;
            height: 80px;
            background: rgba(255, 255, 255, 0.95);
            display: flex;
            align-items: center;
            padding: 0 5%;
            z-index: 1000;
            border-bottom: 1px solid #86a486;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 28px;
            font-weight: 800;
            color: #86a486;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            margin-right: 12px;
            background: #86a486;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
            margin-left: auto;
        }

        .nav-item {
            color: #666;
            text-decoration: none;
            font-weight: 500;
            padding: 10px 15px;
            border-radius: 8px;
        }

        .nav-item:hover {
            background: rgba(134, 164, 134, 0.1);
            color: #86a486;
        }

        .contact-btn {
            background: #86a486;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            margin-left: 20px;
        }

        .hero {
            background: linear-gradient(135deg, #f8fcf8, #e8f4e8);
            padding: 120px 5% 80px;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .hero h1 {
            font-size: 48px;
            font-weight: 900;
            color: #2d4a2d;
            margin-bottom: 20px;
        }

        .hero-subtitle {
            font-size: 24px;
            color: #86a486;
            margin-bottom: 30px;
            font-weight: 600;
        }

        .hero-description {
            font-size: 18px;
            color: #666;
            margin-bottom: 40px;
            max-width: 700px;
            line-height: 1.7;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
            margin-bottom: 60px;
        }

        .btn-primary {
            background: #86a486;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-secondary {
            background: transparent;
            color: #86a486;
            padding: 15px 30px;
            border: 2px solid #86a486;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-secondary:hover {
            background: #86a486;
            color: white;
        }

        .professional-highlight {
            background: white;
            border-radius: 25px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(134, 164, 134, 0.15);
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
            border: 2px solid rgba(134, 164, 134, 0.2);
        }

        .highlight-icon {
            font-size: 60px;
            margin-bottom: 20px;
            display: block;
        }

        .highlight-content h3 {
            color: #86a486;
            font-size: 18px;
            margin-bottom: 8px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .highlight-content h4 {
            color: #2d4a2d;
            font-size: 26px;
            margin-bottom: 8px;
            font-weight: 700;
        }

        .highlight-stats {
            display: flex;
            justify-content: space-around;
            margin: 25px 0;
            padding: 20px 0;
            border-top: 1px solid rgba(134, 164, 134, 0.2);
            border-bottom: 1px solid rgba(134, 164, 134, 0.2);
        }

        .highlight-stats .number {
            display: block;
            font-size: 28px;
            font-weight: 900;
            color: #86a486;
        }

        .highlight-stats .label {
            font-size: 12px;
            color: #666;
            text-transform: uppercase;
        }

        .credentials-mini p {
            color: #666;
            font-size: 14px;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .services {
            padding: 80px 5%;
            background: white;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            font-weight: 800;
            color: #2d4a2d;
            margin-bottom: 20px;
        }

        .section-subtitle {
            text-align: center;
            font-size: 20px;
            color: #86a486;
            margin-bottom: 60px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .service-card {
            background: #f8fcf8;
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            border: 2px solid rgba(134, 164, 134, 0.1);
            transition: all 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(134, 164, 134, 0.15);
            border-color: #86a486;
        }

        .service-icon {
            font-size: 48px;
            margin-bottom: 20px;
            display: block;
        }

        .service-card h3 {
            color: #2d4a2d;
            font-size: 20px;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .service-card p {
            color: #666;
            line-height: 1.6;
        }

        .contact {
            padding: 80px 5%;
            background: #2d4a2d;
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .contact h2 {
            font-size: 36px;
            margin-bottom: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            cursor: pointer;
        }

        .contact-item:hover {
            background: rgba(255, 255, 255, 0.15);
        }

        .contact-item span {
            font-size: 30px;
            margin-right: 20px;
        }

        .contact-item h4 {
            margin-bottom: 5px;
            font-size: 18px;
        }

        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: #25d366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 30px;
            text-decoration: none;
            z-index: 1000;
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.4);
        }

        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero {
                padding: 100px 5% 60px;
            }
            
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="logo">
            <div class="logo-icon">⚕️</div>
            Farmacia Nieto
        </div>
        <nav class="nav-menu">
            <a href="#inicio" class="nav-item">Inicio</a>
            <a href="#servicios" class="nav-item">Servicios</a>
            <a href="#contacto" class="nav-item">Contacto</a>
        </nav>
        <button class="contact-btn" onclick="openWhatsApp()">💬 WhatsApp</button>
    </header>

    <main>
        <section id="inicio" class="hero">
            <h1>Tu camino hacia el bienestar</h1>
            <p class="hero-subtitle">Elaboración Magistral Personalizada</p>
            <p class="hero-description">
                Bajo la dirección técnica de Patricia Victoria Nieto, farmacéutica con una larga trayectoria, 
                te ofrecemos productos de calidad y una atención de excelencia personalizada para cuidar tu salud.
            </p>
            <div class="hero-buttons">
                <a href="#servicios" class="btn-primary">
                    <span>🔍</span> Conocer Servicios
                </a>
                <a href="#contacto" class="btn-secondary">
                    <span>💬</span> Consultar Ahora
                </a>
            </div>
            
            <div class="professional-highlight">
                <div class="highlight-content">
                    <span class="highlight-icon">⚕️</span>
                    <h3>Dirección Técnica</h3>
                    <h4>Patricia Victoria Nieto</h4>
                    <p>Farmacéutica Profesional</p>
                    
                    <div class="highlight-stats">
                        <div class="stat">
                            <span class="number">28+</span>
                            <span class="label">Años</span>
                        </div>
                        <div class="stat">
                            <span class="number">1000+</span>
                            <span class="label">Pacientes</span>
                        </div>
                        <div class="stat">
                            <span class="number">8</span>
                            <span class="label">Especialidades</span>
                        </div>
                    </div>
                    
                    <div class="credentials-mini">
                        <p><span>🎓</span> Matrícula del Colegio de Farmacéuticos</p>
                        <p><span>🔬</span> Especialista en Elaboración Magistral</p>
                        <p><span>📍</span> Universidad Nacional</p>
                        <p><span>⭐</span> Desde 1996 al servicio de la comunidad</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="servicios" class="services">
            <h2 class="section-title">Nuestros Servicios</h2>
            <p class="section-subtitle">
                Formulaciones personalizadas según las necesidades de cada paciente
            </p>
            
            <div class="services-grid">
                <div class="service-card">
                    <span class="service-icon">💊</span>
                    <h3>Medicina Ortomolecular</h3>
                    <p>Tratamientos personalizados basados en el equilibrio molecular óptimo para restaurar la salud natural del organismo.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">✨</span>
                    <h3>Dermocosmética</h3>
                    <p>Productos especializados para el cuidado de la piel, formulados específicamente para cada tipo y necesidad.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🌿</span>
                    <h3>Homeopatía</h3>
                    <p>Preparaciones homeopáticas tradicionales elaboradas con los más altos estándares de calidad y pureza.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🔬</span>
                    <h3>Alopatía</h3>
                    <p>Medicamentos alopáticos preparados magistralmente según prescripción médica con máxima precisión.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🧘‍♀️</span>
                    <h3>Fitoterapia</h3>
                    <p>Tratamientos naturales a base de plantas medicinales, respaldados por la tradición y la ciencia moderna.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🌸</span>
                    <h3>Florales</h3>
                    <p>Esencias florales de Bach y otros sistemas para el equilibrio emocional y el bienestar integral.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🦠</span>
                    <h3>Probióticos</h3>
                    <p>Formulaciones probióticas específicas para restaurar y mantener el equilibrio de la flora intestinal.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🧬</span>
                    <h3>Hormonas Bioidénticas</h3>
                    <p>Terapias hormonales personalizadas con hormonas bioidénticas para el equilibrio hormonal natural.</p>
                </div>
            </div>
        </section>

        <section id="contacto" class="contact">
            <div class="contact-content">
                <div class="contact-info">
                    <h2>Contactanos</h2>
                    <p style="margin-bottom: 40px; font-size: 18px; opacity: 0.9;">
                        Para más asesoramiento y consultas, comunicate con nosotros. 
                        ¡Cuidamos de ti de manera personalizada!
                    </p>
                    
                    <div class="contact-item" onclick="openWhatsApp()">
                        <span>📱</span>
                        <div>
                            <h4>WhatsApp</h4>
                            <p>(+54) 291432-7031</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <span>✉️</span>
                        <div>
                            <h4>Email</h4>
                            <p>farmacia.nieto@hotmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <span>📍</span>
                        <div>
                            <h4>Ubicación</h4>
                            <p>Bahía Blanca, Buenos Aires, Argentina</p>
                        </div>
                    </div>
                    
                                            <div class="contact-item">
                        <span>⏰</span>
                        <div>
                            <h4>Horarios</h4>
                            <p>Lun-Vie: 8:00-20:00<br>Sáb: 8:00-13:00</p>
                        </div>
                    </div>
                </div>
                
                <div style="text-align: center;">
                    <h3 style="color: #9bb49b; margin-bottom: 30px;">¡Estamos aquí para ayudarte!</h3>
                    <p style="font-size: 18px; margin-bottom: 30px;">
                        Patricia Victoria Nieto<br>
                        <strong>Farmacéutica - Directora Técnica</strong><br>
                        28+ años de experiencia<br>
                        Especialista en Elaboración Magistral
                    </p>
                    <button onclick="openWhatsApp()" style="background: rgba(255,255,255,0.2); border: 2px solid white; color: white; padding: 15px 30px; border-radius: 50px; font-weight: 600; cursor: pointer;">
                        <span>💬</span> Consultar por WhatsApp
                    </button>
                </div>
            </div>
        </section>
    </main>

    <a href="#" class="whatsapp-float" onclick="openWhatsApp()">💬</a>

    <script>
        function openWhatsApp() {
            const message = "Hola, me gustaría obtener información sobre sus servicios farmacéuticos. ¡Gracias!";
            const whatsappURL = `https://wa.me/5492914327031?text=${encodeURIComponent(message)}`;
            window.open(whatsappURL, '_blank');
        }

        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html> class="nav-item">Inicio</a>
            <a href="#servicios" class="nav-item">Servicios</a>
            <a href="#contacto" class="nav-item">Contacto</a>
        </nav>
        <button class="contact-btn" onclick="openWhatsApp()">💬 WhatsApp</button>
    </header>

    <main>
        <section id="inicio" class="hero">
            <h1>Tu camino hacia el bienestar</h1>
            <p class="hero-subtitle">Elaboración Magistral Personalizada</p>
            <p class="hero-description">
                Bajo la dirección técnica de Patricia Victoria Nieto, farmacéutica con una larga trayectoria, 
                te ofrecemos productos de calidad y una atención de excelencia personalizada para cuidar tu salud.
            </p>
            <div class="hero-buttons">
                <a href="#servicios" class="btn-primary">
                    <span>🔍</span> Conocer Servicios
                </a>
                <a href="#contacto" class="btn-secondary">
                    <span>💬</span> Consultar Ahora
                </a>
            </div>
            
            <div class="professional-highlight">
                <div class="highlight-content">
                    <span class="highlight-icon">⚕️</span>
                    <h3>Dirección Técnica</h3>
                    <h4>Patricia Victoria Nieto</h4>
                    <p>Farmacéutica Profesional</p>
                    
                    <div class="highlight-stats">
                        <div class="stat">
                            <span class="number">28+</span>
                            <span class="label">Años</span>
                        </div>
                        <div class="stat">
                            <span class="number">1000+</span>
                            <span class="label">Pacientes</span>
                        </div>
                        <div class="stat">
                            <span class="number">8</span>
                            <span class="label">Especialidades</span>
                        </div>
                    </div>
                    
                    <div class="credentials-mini">
                        <p><span>🎓</span> Matrícula del Colegio de Farmacéuticos</p>
                        <p><span>🔬</span> Especialista en Elaboración Magistral</p>
                        <p><span>📍</span> Universidad Nacional</p>
                        <p><span>⭐</span> Desde 1996 al servicio de la comunidad</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="servicios" class="services">
            <h2 class="section-title">Nuestros Servicios</h2>
            <p class="section-subtitle">
                Formulaciones personalizadas según las necesidades de cada paciente
            </p>
            
            <div class="services-grid">
                <div class="service-card">
                    <span class="service-icon">💊</span>
                    <h3>Medicina Ortomolecular</h3>
                    <p>Tratamientos personalizados basados en el equilibrio molecular óptimo para restaurar la salud natural del organismo.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">✨</span>
                    <h3>Dermocosmética</h3>
                    <p>Productos especializados para el cuidado de la piel, formulados específicamente para cada tipo y necesidad.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🌿</span>
                    <h3>Homeopatía</h3>
                    <p>Preparaciones homeopáticas tradicionales elaboradas con los más altos estándares de calidad y pureza.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🔬</span>
                    <h3>Alopatía</h3>
                    <p>Medicamentos alopáticos preparados magistralmente según prescripción médica con máxima precisión.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🧘‍♀️</span>
                    <h3>Fitoterapia</h3>
                    <p>Tratamientos naturales a base de plantas medicinales, respaldados por la tradición y la ciencia moderna.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🌸</span>
                    <h3>Florales</h3>
                    <p>Esencias florales de Bach y otros sistemas para el equilibrio emocional y el bienestar integral.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🦠</span>
                    <h3>Probióticos</h3>
                    <p>Formulaciones probióticas específicas para restaurar y mantener el equilibrio de la flora intestinal.</p>
                </div>
                
                <div class="service-card">
                    <span class="service-icon">🧬</span>
                    <h3>Hormonas Bioidénticas</h3>
                    <p>Terapias hormonales personalizadas con hormonas bioidénticas para el equilibrio hormonal natural.</p>
                </div>
            </div>
        </section>

        <section id="contacto" class="contact">
            <div class="contact-content">
                <div class="contact-info">
                    <h2>Contactanos</h2>
                    <p style="margin-bottom: 40px; font-size: 18px; opacity: 0.9;">
                        Para más asesoramiento y consultas, comunicate con nosotros. 
                        ¡Cuidamos de ti de manera personalizada!
                    </p>
                    
                    <div class="contact-item" onclick="openWhatsApp()">
                        <span>📱</span>
                        <div>
                            <h4>WhatsApp</h4>
                            <p>(+54) 291432-7031</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <span>✉️</span>
                        <div>
                            <h4>Email</h4>
                            <p>farmacia.nieto@hotmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <span>📍</span>
                        <div>
                            <h4>Ubicación</h4>
                            <p>Bahía Blanca, Buenos Aires, Argentina</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <span>⏰</span>
                        <div>
                            <h4>Horarios</h4>
                            <p>Lun-Vie: 8:00-20:00<br>Sáb: 8:00-13:00</p>
                        </div>
                    </div>
                </div>
                
                <div style="text-align: center;">
                    <h3 style="color: #9bb49b; margin-bottom: 30px;">¡Estamos aquí para ayudarte!</h3>
                    <p style="font-size: 18px; margin-bottom: 30px;">
                        Patricia Victoria Nieto<br>
                        <strong>Farmacéutica - Directora Técnica</strong><br>
                        28+ años de experiencia<br>
                        Especialista en Elaboración Magistral
                    </p>
                    <button onclick="openWhatsApp()" style="background: rgba(255,255,255,0.2); border: 2px solid white; color: white; padding: 15px 30px; border-radius: 50px; font-weight: 600; cursor: pointer;">
                        <span>💬</span> Consultar por WhatsApp
                    </button>
                </div>
            </div>
        </section>
    </main>

    <a href="#" class="whatsapp-float" onclick="openWhatsApp()">💬</a>

    <script>
        function openWhatsApp() {
            const message = "Hola, me gustaría obtener información sobre sus servicios farmacéuticos. ¡Gracias!";
            const whatsappURL = `https://wa.me/5492914327031?text=${encodeURIComponent(message)}`;
            window.open(whatsappURL, '_blank');
        }

        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
