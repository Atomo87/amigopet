<html lang="pt-BR"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amigo Pet | Petshop Profissional</title>
    <!-- Fonte Google -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&amp;display=swap" rel="stylesheet">
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary: #ff7e29;       /* laranja vibrante */
            --primary-dark: #e0650e;
            --secondary: #2d3e50;     /* azul escuro */
            --light-bg: #fff9f5;
            --gray-light: #f5f7fa;
            --text-dark: #1e2a3a;
            --text-soft: #4a5b6e;
            --white: #ffffff;
            --shadow-sm: 0 8px 20px rgba(0, 0, 0, 0.04);
            --shadow-md: 0 15px 40px rgba(0, 0, 0, 0.08);
            --radius: 20px;
            --radius-sm: 12px;
        }

        body {
            background-color: var(--white);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* ===== HEADER ===== */
        header {
            background: var(--white);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 16px 0;
        }

        .header-flex {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 26px;
            font-weight: 800;
            color: var(--secondary);
            letter-spacing: -0.5px;
        }

        .logo i {
            color: var(--primary);
            font-size: 32px;
        }

        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 36px;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            font-size: 16px;
            transition: 0.2s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -6px;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--primary);
            border-radius: 4px;
            transition: width 0.25s;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .btn {
            display: inline-block;
            background: var(--primary);
            color: var(--white);
            padding: 14px 32px;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.25s;
            border: none;
            cursor: pointer;
            font-size: 16px;
            box-shadow: 0 8px 18px rgba(255, 126, 41, 0.25);
        }

        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(255, 126, 41, 0.35);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            box-shadow: none;
            padding: 12px 30px;
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
            box-shadow: 0 8px 18px rgba(255, 126, 41, 0.3);
        }

        .menu-toggle {
            display: none;
            font-size: 26px;
            color: var(--secondary);
            background: none;
            border: none;
            cursor: pointer;
        }

        /* ===== HERO ===== */
        .hero {
            padding: 60px 0 80px;
            background: linear-gradient(135deg, #fff6ef 0%, #ffffff 100%);
            border-bottom-left-radius: 60px;
            border-bottom-right-radius: 60px;
            position: relative;
            overflow: hidden;
        }

        .hero::after {
            content: "🐾";
            font-size: 180px;
            position: absolute;
            right: 5%;
            top: 20px;
            opacity: 0.06;
            transform: rotate(15deg);
            pointer-events: none;
        }

        .hero-flex {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .hero-content {
            flex: 1;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255, 126, 41, 0.12);
            color: var(--primary);
            font-weight: 600;
            font-size: 14px;
            padding: 8px 18px;
            border-radius: 40px;
            margin-bottom: 20px;
            letter-spacing: 0.5px;
        }

        .hero h1 {
            font-size: 52px;
            line-height: 1.15;
            font-weight: 800;
            color: var(--secondary);
            margin-bottom: 24px;
        }

        .hero h1 span {
            color: var(--primary);
            position: relative;
            display: inline-block;
        }

        .hero p {
            font-size: 18px;
            color: var(--text-soft);
            margin-bottom: 36px;
            max-width: 500px;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .hero-img-wrapper {
            background: var(--primary);
            width: 100%;
            max-width: 480px;
            height: 420px;
            border-radius: 40% 60% 40% 60% / 60% 40% 60% 40%;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            box-shadow: var(--shadow-md);
            animation: morph 8s ease-in-out infinite alternate;
        }

        @keyframes morph {
            0% { border-radius: 40% 60% 40% 60% / 60% 40% 60% 40%; }
            100% { border-radius: 60% 40% 60% 40% / 40% 60% 40% 60%; }
        }

        .hero-img-wrapper img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* ===== SERVIÇOS ===== */
        .services {
            padding: 100px 0;
            background: var(--white);
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title span {
            display: inline-block;
            background: rgba(255, 126, 41, 0.1);
            color: var(--primary);
            font-weight: 600;
            font-size: 14px;
            padding: 6px 18px;
            border-radius: 40px;
            margin-bottom: 14px;
            letter-spacing: 1px;
        }

        .section-title h2 {
            font-size: 40px;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: 16px;
        }

        .section-title p {
            color: var(--text-soft);
            max-width: 600px;
            margin: 0 auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .service-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 40px 30px;
            box-shadow: var(--shadow-sm);
            transition: all 0.3s;
            border: 1px solid #f0f2f5;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-md);
            border-color: rgba(255, 126, 41, 0.2);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: rgba(255, 126, 41, 0.1);
            border-radius: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 28px;
            font-size: 36px;
            color: var(--primary);
            transition: 0.3s;
        }

        .service-card:hover .service-icon {
            background: var(--primary);
            color: white;
            transform: scale(1.05) rotate(5deg);
        }

        .service-card h3 {
            font-size: 22px;
            font-weight: 700;
            margin-bottom: 12px;
            color: var(--secondary);
        }

        .service-card p {
            color: var(--text-soft);
            font-size: 15px;
        }

        /* ===== DIFERENCIAIS ===== */
        .features {
            padding: 90px 0;
            background: var(--light-bg);
            border-radius: 60px 60px 0 0;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
        }

        .feature-item {
            text-align: center;
            padding: 20px;
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: var(--white);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 22px;
            font-size: 30px;
            color: var(--primary);
            box-shadow: var(--shadow-sm);
        }

        .feature-item h4 {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 8px;
            color: var(--secondary);
        }

        .feature-item p {
            font-size: 14px;
            color: var(--text-soft);
        }

        /* ===== DEPOIMENTOS ===== */
        .testimonials {
            padding: 100px 0;
            background: var(--white);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .testimonial-card {
            background: var(--gray-light);
            border-radius: var(--radius);
            padding: 35px 30px;
            transition: 0.3s;
        }

        .testimonial-card:hover {
            background: var(--white);
            box-shadow: var(--shadow-md);
        }

        .stars {
            color: #ffb800;
            margin-bottom: 18px;
            font-size: 14px;
        }

        .testimonial-card p {
            font-size: 16px;
            color: var(--text-soft);
            margin-bottom: 24px;
            font-style: italic;
        }

        .client-info {
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .client-avatar {
            width: 50px;
            height: 50px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: white;
            font-size: 18px;
        }

        .client-info h5 {
            font-weight: 700;
            color: var(--secondary);
        }

        .client-info span {
            font-size: 13px;
            color: var(--text-soft);
        }

        /* ===== CTA ===== */
        .cta {
            padding: 40px 0 100px;
            background: var(--white);
        }

        .cta-box {
            background: linear-gradient(120deg, var(--secondary) 0%, #1f2e3d 100%);
            border-radius: 50px;
            padding: 70px 50px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .cta-box::before {
            content: "🐕";
            font-size: 220px;
            position: absolute;
            right: 20px;
            bottom: -40px;
            opacity: 0.08;
            pointer-events: none;
        }

        .cta-content h2 {
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 12px;
            max-width: 500px;
        }

        .cta-content p {
            opacity: 0.8;
            max-width: 450px;
            margin-bottom: 28px;
        }

        .cta .btn {
            background: var(--primary);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .cta .btn:hover {
            background: #ff8f3f;
        }

        /* ===== FOOTER ===== */
        footer {
            background: #f8fafc;
            padding: 60px 0 20px;
            border-top: 1px solid #e9edf2;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1.5fr;
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-about .logo {
            margin-bottom: 16px;
        }

        .footer-about p {
            color: var(--text-soft);
            font-size: 15px;
            margin-bottom: 20px;
        }

        .social-icons {
            display: flex;
            gap: 14px;
        }

        .social-icons a {
            width: 42px;
            height: 42px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            text-decoration: none;
            transition: 0.2s;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.02);
        }

        .social-icons a:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-3px);
        }

        .footer-links h4 {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            text-decoration: none;
            color: var(--text-soft);
            transition: 0.2s;
            font-size: 15px;
        }

        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }

        .footer-contact p {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 14px;
            color: var(--text-soft);
            font-size: 15px;
        }

        .footer-contact i {
            color: var(--primary);
            width: 20px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #e2e8f0;
            color: #8a9aa8;
            font-size: 14px;
        }

        /* ===== RESPONSIVO ===== */
        @media (max-width: 1024px) {
            .hero h1 { font-size: 42px; }
            .services-grid { grid-template-columns: repeat(2, 1fr); }
            .features-grid { grid-template-columns: repeat(2, 1fr); }
            .testimonials-grid { grid-template-columns: repeat(2, 1fr); }
            .footer-grid { grid-template-columns: 1fr 1fr; }
            .cta-box { flex-direction: column; text-align: center; gap: 30px; }
            .cta-content h2 { max-width: 100%; }
            .cta-content p { max-width: 100%; }
        }

        @media (max-width: 768px) {
            .header-flex { flex-wrap: wrap; }
            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                gap: 18px;
                padding: 25px 0 10px;
                text-align: center;
            }
            .nav-links.active { display: flex; }
            .menu-toggle { display: block; }
            .header-flex .btn { display: none; } /* esconde botão no mobile, pode manter se quiser */
            .hero-flex { flex-direction: column-reverse; text-align: center; }
            .hero p { margin-left: auto; margin-right: auto; }
            .hero-buttons { justify-content: center; }
            .hero h1 { font-size: 36px; }
            .services-grid { grid-template-columns: 1fr; }
            .features-grid { grid-template-columns: 1fr; }
            .testimonials-grid { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr; gap: 30px; }
            .cta-box { padding: 45px 25px; }
            .cta-content h2 { font-size: 28px; }
            .hero-img-wrapper { height: 300px; }
            .section-title h2 { font-size: 32px; }
        }

        @media (max-width: 480px) {
            .hero h1 { font-size: 30px; }
            .btn { padding: 12px 24px; font-size: 14px; }
            .hero-buttons { flex-direction: column; align-items: center; }
        }
    </style>
</head>
<body>

    <!-- HEADER -->
    <header>
        <div class="container header-flex">
            <div class="logo">
                <i class="fas fa-paw"></i>
                Amigo<span>Pet</span>
            </div>
            <nav>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#">Início</a></li>
                    <li><a href="#servicos">Serviços</a></li>
                    <li><a href="#diferenciais">Diferenciais</a></li>
                    <li><a href="#depoimentos">Depoimentos</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
            <a href="#contato" class="btn">Agendar agora</a>
            <button class="menu-toggle" id="menuToggle"><i class="fas fa-bars"></i></button>
        </div>
    </header>

    <!-- HERO -->
    <section class="hero">
        <div class="container hero-flex">
            <div class="hero-content">
                <div class="hero-badge"><i class="fas fa-star"></i> Referência em cuidado animal</div>
                <h1>Cuidado <span>profissional</span> para quem você ama</h1>
                <p>Banho &amp; tosa, consultas veterinárias, hospedagem e muito mais. Seu pet em boas mãos, com todo carinho e segurança que ele merece.</p>
                <div class="hero-buttons">
                    <a href="#contato" class="btn">Agende um horário</a>
                    <a href="#servicos" class="btn btn-outline">Conheça os serviços</a>
                </div>
            </div>
            <div class="hero-image">
                <div class="hero-img-wrapper">
                    <!-- imagem ilustrativa de pet (fonte: unsplash) -->
                    <img src="https://images.unsplash.com/photo-1543466835-00a7907e9de1?q=80&amp;w=1000&amp;auto=format&amp;fit=crop" alt="Cachorro feliz">
                </div>
            </div>
        </div>
    </section>

    <!-- SERVIÇOS -->
    <section class="services" id="servicos">
        <div class="container">
            <div class="section-title">
                <span>NOSSOS SERVIÇOS</span>
                <h2>Tudo o que seu pet precisa</h2>
                <p>Oferecemos uma gama completa de serviços com profissionais especializados e ambiente acolhedor.</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-bath"></i></div>
                    <h3>Banho &amp; Tosa</h3>
                    <p>Produtos hipoalergênicos, secagem cuidadosa e tosa personalizada de acordo com a raça.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-stethoscope"></i></div>
                    <h3>Consultas Veterinárias</h3>
                    <p>Check-up completo, vacinação, exames e acompanhamento preventivo com equipe experiente.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-hotel"></i></div>
                    <h3>Hospedagem</h3>
                    <p>Ambiente seguro e confortável, com monitoramento 24h e atividades recreativas diárias.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-dog"></i></div>
                    <h3>Adestramento</h3>
                    <p>Treinamento comportamental positivo, obediência básica e socialização com outros pets.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-truck"></i></div>
                    <h3>Leva &amp; Traz</h3>
                    <p>Buscamos e levamos seu melhor amigo em veículo adaptado e com total segurança.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-cart-shopping"></i></div>
                    <h3>Pet Shop</h3>
                    <p>Rações premium, brinquedos, medicamentos e acessórios das melhores marcas do mercado.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- DIFERENCIAIS -->
    <section class="features" id="diferenciais">
        <div class="container">
            <div class="section-title">
                <span>POR QUE ESCOLHER A AMIGO PET?</span>
                <h2>Diferenciais que fazem a diferença</h2>
                <p>Mais que um petshop, um lugar onde seu pet é tratado como família.</p>
            </div>
            <div class="features-grid">
                <div class="feature-item">
                    <div class="feature-icon"><i class="fas fa-user-md"></i></div>
                    <h4>Equipe especializada</h4>
                    <p>Profissionais formados e apaixonados por animais.</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon"><i class="fas fa-clock"></i></div>
                    <h4>Atendimento ágil</h4>
                    <p>Horários flexíveis e agendamento online rápido.</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon"><i class="fas fa-shield-heart"></i></div>
                    <h4>Ambiente seguro</h4>
                    <p>Espaço higienizado e monitorado por câmeras.</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon"><i class="fas fa-heart"></i></div>
                    <h4>Amor em cada detalhe</h4>
                    <p>Tratamos cada pet com o carinho que ele merece.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- DEPOIMENTOS -->
    <section class="testimonials" id="depoimentos">
        <div class="container">
            <div class="section-title">
                <span>DEPOIMENTOS</span>
                <h2>O que os clientes dizem</h2>
                <p>Histórias reais de quem confia no nosso trabalho.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p>"Levo meu golden retriever há 3 anos. O cuidado com o banho e a tosa é impecável, além do carinho de toda equipe. Super recomendo!"</p>
                    <div class="client-info">
                        <div class="client-avatar">MC</div>
                        <div>
                            <h5>Mariana Costa</h5>
                            <span>Tutora do Thor</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p>"Precisei viajar e deixei minha gata na hospedagem. Recebi fotos todos os dias e ela voltou super tranquila. Serviço excepcional!"</p>
                    <div class="client-info">
                        <div class="client-avatar">RS</div>
                        <div>
                            <h5>Rafael Souza</h5>
                            <span>Tutor da Luna</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p>"O adestramento mudou o comportamento do meu beagle. Profissionais pacientes e muito atenciosos. Nota 10!"</p>
                    <div class="client-info">
                        <div class="client-avatar">CA</div>
                        <div>
                            <h5>Camila Alves</h5>
                            <span>Tutora do Bob</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta" id="contato">
        <div class="container">
            <div class="cta-box">
                <div class="cta-content">
                    <h2>Pronto para mimar seu melhor amigo?</h2>
                    <p>Agende agora mesmo um horário e ganhe 10% de desconto na primeira visita.</p>
                </div>
                <a href="#" class="btn"><i class="fab fa-whatsapp"></i> Agendar pelo WhatsApp</a>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-about">
                    <div class="logo">
                        <i class="fas fa-paw"></i>
                        Amigo<span>Pet</span>
                    </div>
                    <p>Há mais de 10 anos cuidando com amor e profissionalismo dos seus melhores amigos.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Links rápidos</h4>
                    <ul>
                        <li><a href="#">Início</a></li>
                        <li><a href="#servicos">Serviços</a></li>
                        <li><a href="#diferenciais">Diferenciais</a></li>
                        <li><a href="#depoimentos">Depoimentos</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Serviços</h4>
                    <ul>
                        <li><a href="#">Banho &amp; Tosa</a></li>
                        <li><a href="#">Veterinária</a></li>
                        <li><a href="#">Hospedagem</a></li>
                        <li><a href="#">Adestramento</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h4>Contato</h4>
                    <p><i class="fas fa-map-marker-alt"></i> Av. dos Pets, 123 – São Paulo, SP</p>
                    <p><i class="fas fa-phone-alt"></i> (11) 4002-8922</p>
                    <p><i class="fas fa-envelope"></i> contato@amigopet.com.br</p>
                    <p><i class="fas fa-clock"></i> Seg a Sáb: 8h às 19h</p>
                </div>
            </div>
            <div class="footer-bottom">
                © 2025 Amigo Pet – Todos os direitos reservados. Feito com <i class="fas fa-heart" style="color: var(--primary);"></i> para os animais.
            </div>
        </div>
    </footer>

    <!-- SCRIPT MENU MOBILE -->
    <script>
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            // muda ícone
            const icon = menuToggle.querySelector('i');
            if (navLinks.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });

        // fecha menu ao clicar em um link (mobile)
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                const icon = menuToggle.querySelector('i');
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            });
        });
    </script>

</body></html>
