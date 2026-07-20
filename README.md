<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>e-Laporan GBK | Sistem Pintar Penjanaan Laporan Kaunseling Berasaskan AI</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #0F172A;
            --primary-light: #1E293B;
            --white: #FFFFFF;
            --gold: #D4AF37;
            --gold-light: #F4E8A2;
            --teal: #0D9488;
            --teal-light: #CCFBF1;
            --gray-bg: #F8FAFC;
            --gray-border: #E2E8F0;
            --text-main: #334155;
            --text-muted: #64748B;
            --shadow: 0 10px 30px -5px rgba(15, 23, 42, 0.08);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
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
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--white);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(12px);
            z-index: 1000;
            border-bottom: 1px solid var(--gray-border);
            padding: 1rem 0;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-brand {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            text-decoration: none;
            color: var(--primary);
            font-weight: 700;
            font-size: 1.25rem;
        }

        .nav-logo-mini {
            width: 36px;
            height: 36px;
            background: var(--primary);
            color: var(--gold);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            font-weight: 800;
            font-size: 0.9rem;
            letter-spacing: -1px;
            border: 1px solid var(--gold);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-main);
            font-weight: 500;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--teal);
        }

        .nav-cta {
            background: var(--primary) !important;
            color: var(--white) !important;
            padding: 0.6rem 1.25rem;
            border-radius: 50px;
            font-weight: 600 !important;
            transition: var(--transition);
        }

        .nav-cta:hover {
            background: var(--teal) !important;
            transform: translateY(-2px);
        }

        /* Hero Section */
        header.hero {
            min-height: 100vh;
            background: linear-gradient(135deg, var(--primary) 0%, #1a2c4e 100%);
            color: var(--white);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 8rem 2rem 5rem 2rem;
            position: relative;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            z-index: 2;
        }

        .hero-logo-container {
            width: 90px;
            height: 90px;
            background: rgba(255, 255, 255, 0.05);
            border: 2px solid var(--gold);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem auto;
            box-shadow: 0 0 30px rgba(212, 175, 55, 0.2);
            animation: float 4s ease-in-out infinite;
        }

        .hero-logo-text {
            font-size: 2.25rem;
            font-weight: 800;
            color: var(--gold);
            letter-spacing: -2px;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .hero-innovation {
            font-size: 0.85rem;
            font-weight: 700;
            letter-spacing: 4px;
            color: var(--gold);
            text-transform: uppercase;
            margin-bottom: 0.5rem;
        }

        .hero-tagline {
            font-size: 1rem;
            font-weight: 500;
            letter-spacing: 2px;
            color: var(--teal-light);
            text-transform: uppercase;
            margin-bottom: 1.5rem;
        }

        .hero-title {
            font-size: clamp(2.5rem, 5vw, 4.5rem);
            font-weight: 800;
            margin-bottom: 1.5rem;
            letter-spacing: -1px;
            background: linear-gradient(to right, #ffffff, #e2e8f0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-subtitle {
            font-size: clamp(1rem, 2vw, 1.25rem);
            color: var(--text-muted);
            margin-bottom: 2.5rem;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
            color: #cbd5e1;
        }

        .btn-primary {
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            background: var(--gold);
            color: var(--primary);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.05rem;
            text-decoration: none;
            transition: var(--transition);
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.3);
            border: none;
            cursor: pointer;
        }

        .btn-primary:hover {
            background: #e6c547;
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(212, 175, 55, 0.4);
        }

        /* General Section Styling */
        section {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 4rem auto;
        }

        .section-badge {
            display: inline-block;
            background: var(--teal-light);
            color: var(--teal);
            padding: 0.4rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
        }

        .section-title {
            font-size: clamp(2rem, 3vw, 2.75rem);
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 1rem;
            letter-spacing: -0.5px;
        }

        .section-desc {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        /* About Section */
        .about-section {
            background: var(--gray-bg);
            border-radius: 24px;
            padding: 4rem;
            margin: 4rem auto;
            box-shadow: var(--shadow);
            border: 1px solid var(--gray-border);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.25rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .about-text p {
            color: var(--text-main);
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        .about-features-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .about-features-list li {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-weight: 600;
            color: var(--primary);
        }

        .about-features-list i {
            color: var(--teal);
            background: var(--teal-light);
            width: 28px;
            height: 28px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.85rem;
        }

        .about-visual {
            background: var(--white);
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.04);
            border: 1px solid var(--gray-border);
            position: relative;
        }

        .about-visual::before {
            content: '';
            position: absolute;
            top: -10px;
            right: -10px;
            width: 100px;
            height: 100px;
            background: radial-gradient(var(--gold) 10%, transparent 70%);
            opacity: 0.2;
            z-index: 0;
        }

        .stat-card-mini {
            display: flex;
            align-items: center;
            gap: 1.5rem;
            padding: 1.25rem;
            background: var(--gray-bg);
            border-radius: 12px;
            margin-bottom: 1rem;
        }

        .stat-icon {
            width: 50px;
            height: 50px;
            background: var(--teal);
            color: var(--white);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.25rem;
        }

        .stat-info h4 {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--primary);
        }

        .stat-info p {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin: 0;
        }

        /* Features Section */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: var(--white);
            border: 1px solid var(--gray-border);
            padding: 2.5rem;
            border-radius: 20px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .feature-card:hover {
            transform: translateY(-8px);
            border-color: var(--teal);
            box-shadow: 0 20px 40px rgba(13, 148, 136, 0.1);
        }

        .feature-card::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--teal), var(--gold));
            opacity: 0;
            transition: var(--transition);
        }

        .feature-card:hover::after {
            opacity: 1;
        }

        .feature-icon-wrapper {
            width: 60px;
            height: 60px;
            background: var(--teal-light);
            color: var(--teal);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .feature-card:hover .feature-icon-wrapper {
            background: var(--primary);
            color: var(--gold);
        }

        .feature-card h3 {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.75rem;
        }

        .feature-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* AI Generator Section */
        .generator-section {
            background: linear-gradient(135deg, var(--primary) 0%, #162238 100%);
            border-radius: 30px;
            padding: 5rem 3rem;
            color: var(--white);
            margin: 6rem auto;
            box-shadow: 0 25px 50px -12px rgba(15, 23, 42, 0.25);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }

        .generator-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: start;
        }

        .generator-form .form-group {
            margin-bottom: 1.5rem;
        }

        .generator-form label {
            display: block;
            font-weight: 600;
            font-size: 0.95rem;
            margin-bottom: 0.5rem;
            color: #e2e8f0;
        }

        .generator-form select,
        .generator-form textarea {
            width: 100%;
            padding: 0.85rem 1rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 12px;
            color: var(--white);
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-size: 0.95rem;
            transition: var(--transition);
        }

        .generator-form select option {
            background: var(--primary);
            color: var(--white);
        }

        .generator-form select:focus,
        .generator-form textarea:focus {
            outline: none;
            border-color: var(--gold);
            background: rgba(255, 255, 255, 0.08);
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.2);
        }

        .generator-form textarea {
            resize: vertical;
            min-height: 100px;
        }

        .btn-generate {
            width: 100%;
            background: var(--gold);
            color: var(--primary);
            padding: 1rem;
            border-radius: 12px;
            font-weight: 700;
            font-size: 1rem;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
            margin-top: 2rem;
        }

        .btn-generate:hover {
            background: #e6c547;
            transform: translateY(-2px);
            box-shadow: 0 12px 25px rgba(212, 175, 55, 0.4);
        }

        /* Output Box */
        .generator-output-wrapper {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            position: relative;
            min-height: 520px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .output-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding-bottom: 1rem;
        }

        .output-header h3 {
            font-size: 1.25rem;
            color: var(--gold);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .ai-status-badge {
            background: rgba(13, 148, 136, 0.2);
            color: var(--teal-light);
            padding: 0.25rem 0.75rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
            border: 1px solid var(--teal);
        }

        .output-content {
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            gap: 1.25rem;
        }

        .output-placeholder {
            margin: auto;
            text-align: center;
            color: var(--text-muted);
            padding: 2rem;
        }

        .output-placeholder i {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: rgba(255, 255, 255, 0.2);
        }

        .output-section-item {
            background: rgba(0, 0, 0, 0.2);
            border-left: 4px solid var(--gold);
            padding: 1.25rem;
            border-radius: 0 12px 12px 0;
            display: none;
            animation: fadeIn 0.5s ease forwards;
        }

        .output-section-item.active {
            display: block;
        }

        .output-section-item h4 {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--gold);
            margin-bottom: 0.5rem;
            font-weight: 700;
        }

        .output-section-item p {
            font-size: 0.95rem;
            color: #e2e8f0;
            line-height: 1.5;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .output-actions {
            margin-top: 1.5rem;
            display: flex;
            gap: 1rem;
            display: none;
        }

        .btn-action-sub {
            flex: 1;
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: var(--white);
            padding: 0.75rem;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .btn-action-sub:hover {
            background: rgba(255, 255, 255, 0.15);
            border-color: var(--white);
        }

        /* Why Choose Section */
        .why-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2rem;
        }

        .why-card {
            background: var(--white);
            border: 1px solid var(--gray-border);
            padding: 2.5rem 2rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .why-card:hover {
            transform: translateY(-5px);
            border-color: var(--gold);
        }

        .why-icon {
            width: 70px;
            height: 70px;
            background: var(--teal-light);
            color: var(--teal);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.75rem;
            margin: 0 auto 1.5rem auto;
        }

        .why-card h3 {
            font-size: 1.15rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.75rem;
        }

        .why-card p {
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: var(--white);
            padding: 4rem 2rem 2rem 2rem;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--white);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.75rem;
        }

        .footer-tagline {
            color: var(--gold);
            font-size: 0.95rem;
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 2rem;
        }

        .footer-divider {
            height: 1px;
            background: rgba(255, 255, 255, 0.1);
            margin: 2rem 0;
        }

        .footer-copyright {
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        /* Responsive Design */
        @media (max-width: 968px) {
            .about-grid,
            .generator-container {
                grid-template-columns: 1fr;
                gap: 2.5rem;
            }
            .about-section {
                padding: 2.5rem;
            }
            .generator-section {
                padding: 3rem 1.5rem;
            }
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <a href="#" class="nav-brand">
                <div class="nav-logo-mini">RR</div>
                e-Laporan GBK
            </a>
            <ul class="nav-links">
                <li><a href="#about">Tentang Sistem</a></li>
                <li><a href="#features">Fungsi Utama</a></li>
                <li><a href="#generator">Jana AI</a></li>
                <li><a href="#why-choose">Kelebihan</a></li>
                <li><a href="#generator" class="nav-cta">Mula Sekarang</a></li>
            </ul>
        </div>
    </nav>

    <!-- 1. Hero Section -->
    <header class="hero">
        <div class="hero-content">
            <div class="hero-logo-container">
                <span class="hero-logo-text">RR</span>
            </div>
            <div class="hero-innovation">INNOVATION</div>
            <div class="hero-tagline">FORWARD TOGETHER</div>
            <h1 class="hero-title">e-Laporan GBK</h1>
            <p class="hero-subtitle">Sistem Pintar Penjanaan Laporan Kaunseling Berasaskan AI untuk Guru Bimbingan dan Kaunseling</p>
            <a href="#generator" class="btn-primary">
                <i class="fa-solid fa-wand-magic-sparkles"></i> Mula Jana Laporan
            </a>
        </div>
    </header>

    <!-- 2. About Section -->
    <div style="max-width: 1200px; margin: 0 auto; padding: 0 2rem;">
        <section id="about" class="about-section">
            <div class="about-grid">
                <div class="about-text">
                    <span class="section-badge">Mengenai Platform</span>
                    <h2>Transformasi Digital Pengurusan Kaunseling Sekolah</h2>
                    <p>e-Laporan GBK direka khas untuk memperkasakan tugasan harian Guru Bimbingan dan Kaunseling di Malaysia dengan menggabungkan teknologi Kepintaran Buatan (AI) yang selamat, pantas dan beretika.</p>
                    <p>Sistem ini membantu kaunselor merangka laporan bimbingan yang terperinci, teratur dan mematuhi standard amalan profesional perkhidmatan bimbingan dan kaunseling sekolah.</p>
                    <ul class="about-features-list">
                        <li><i class="fa-solid fa-check"></i> Mengurangkan beban dokumentasi rutin</li>
                        <li><i class="fa-solid fa-check"></i> Cadangan intervensi berasaskan teori profesional</li>
                        <li><i class="fa-solid fa-check"></i> Memenuhi piawaian pengurusan KPM</li>
                    </ul>
                </div>
                <div class="about-visual">
                    <div class="stat-card-mini">
                        <div class="stat-icon"><i class="fa-solid fa-brain"></i></div>
                        <div class="stat-info">
                            <h4>Teknologi AI Pintar</h4>
                            <p>Penjanaan teks automatik yang relevan dengan isu murid</p>
                        </div>
                    </div>
                    <div class="stat-card-mini">
                        <div class="stat-icon"><i class="fa-solid fa-book-open"></i></div>
                        <div class="stat-info">
                            <h4>Teori Kaunseling Sahih</h4>
                            <p>Integrasi teori moden seperti CBT, REBT & Reality Therapy</p>
                        </div>
                    </div>
                    <div class="stat-card-mini">
                        <div class="stat-icon"><i class="fa-solid fa-shield-halved"></i></div>
                        <div class="stat-info">
                            <h4>Kerahsiaan & Keselamatan</h4>
                            <p>Pematuhan etika kerahsiaan data murid sekolah</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- 3. Features Section -->
    <section id="features">
        <div class="section-header">
            <span class="section-badge">Modul Sistem</span>
            <h2 class="section-title">Fungsi & Modul Komprehensif</h2>
            <p class="section-desc">Direka bentuk untuk menampung pelbagai skop perkhidmatan bimbingan dan kaunseling di institusi pendidikan.</p>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-user"></i></div>
                <h3>Laporan Kaunseling Individu</h3>
                <p>Merekod sesi bimbingan personal satu-dengan-satu dengan analisis isu peribadi, emosi, atau sahsiah secara mendalam.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-users"></i></div>
                <h3>Laporan Kaunseling Kelompok</h3>
                <p>Menyelaras dokumentasi dinamika kumpulan kecil murid dengan merumus isu bersama dan dinamika interaksi kelompok.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-chalkboard-user"></i></div>
                <h3>Bimbingan Kelas</h3>
                <p>Menghasilkan laporan modul psikoedukasi, motivasi akademik, dan kesedaran kerjaya secara bersemuka di dalam kelas.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-handshake"></i></div>
                <h3>Konsultasi</h3>
                <p>Merekod sesi perbincangan profesional bersama pentadbir, guru mata pelajaran, atau ibu bapa berkenaan kebajikan murid.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-file-lines"></i></div>
                <h3>Jana Perkara, Persoalan & Intervensi GBK</h3>
                <p>Automatik membina ringkasan isu (Perkara), soalan penerokaan bermakna (Persoalan), dan tindakan susulan (Intervensi).</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon-wrapper"><i class="fa-solid fa-book-bookmark"></i></div>
                <h3>Berasaskan Teori Kaunseling</h3>
                <p>Pemilihan kerangka teori terapeutik yang tepat bagi memastikan intervensi berlandaskan landasan sains psikologi yang sah.</p>
            </div>
        </div>
    </section>

    <!-- 4. AI Report Generator Section -->
    <div style="max-width: 1200px; margin: 0 auto; padding: 0 2rem;">
        <section id="generator" class="generator-section" style="padding: 0; background: transparent; box-shadow: none; border: none;">
            <div style="background: linear-gradient(135deg, var(--primary) 0%, #162238 100%); border-radius: 30px; padding: 4rem 3rem; border: 1px solid rgba(212, 175, 55, 0.2);">
                <div class="section-header" style="margin-bottom: 3rem;">
                    <span class="section-badge" style="background: rgba(212, 175, 55, 0.15); color: var(--gold);">Demo Interaktif AI</span>
                    <h2 class="section-title" style="color: var(--white);">Penjana Laporan Pintar GBK</h2>
                    <p class="section-desc" style="color: #cbd5e1;">Cuba masukkan parameter di bawah dan saksikan bagaimana AI membantu merangka draf laporan anda serta-merta.</p>
                </div>
                
                <div class="generator-container">
                    <!-- Form Inputs -->
                    <div class="generator-form">
                        <div class="form-group">
                            <label><i class="fa-solid fa-layer-group"></i> Jenis Sesi</label>
                            <select id="jenisSesi">
                                <option value="Individu">Individu</option>
                                <option value="Kelompok">Kelompok</option>
                                <option value="Bimbingan Kelas">Bimbingan Kelas</option>
                                <option value="Konsultasi">Konsultasi</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label><i class="fa-solid fa-compass"></i> Pendekatan</label>
                            <select id="pendekatan">
                                <option value="Pencegahan">Pencegahan</option>
                                <option value="Perkembangan">Perkembangan</option>
                                <option value="Pemulihan">Pemulihan</option>
                                <option value="Krisis">Krisis</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label><i class="fa-solid fa-bullseye"></i> Fokus Utama</label>
                            <select id="fokusUtama" onchange="updateSubFokus()">
                                <option value="Pembangunan & Perkembangan Sahsiah Diri Murid">1. Pembangunan & Perkembangan Sahsiah Diri Murid</option>
                                <option value="Pendidikan Kerjaya Murid">2. Pendidikan Kerjaya Murid</option>
                                <option value="Peningkatan Disiplin Murid">3. Peningkatan Disiplin Murid</option>
                                <option value="Psikososial & Kesejahteraan Mental Murid">4. Psikososial & Kesejahteraan Mental Murid</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label><i class="fa-solid fa-list-check"></i> Sub Fokus</label>
                            <select id="subFokus">
                                <!-- Dynamic options filled via JS -->
                            </select>
                        </div>

                        <div class="form-group">
                            <label><i class="fa-solid fa-atom"></i> Teori Kaunseling</label>
                            <select id="teori">
                                <option value="Reality Therapy">Reality Therapy (Glasser)</option>
                                <option value="CBT">CBT (Cognitive Behavioral Therapy)</option>
                                <option value="Person Centered">Person Centered (Carl Rogers)</option>
                                <option value="REBT">REBT (Albert Ellis)</option>
                                <option value="Solution Focused">Solution Focused Brief Therapy</option>
                                <option value="Adlerian">Adlerian Therapy</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label><i class="fa-solid fa-pen-nib"></i> Masukan Isu Murid</label>
                            <textarea id="isuMurid" placeholder="Cth: Murid kerap hadir lewat ke sekolah, hilang fokus dalam kelas akibat tidur lewat melayari telefon bimbit, dan menunjukkan tanda kurang motivasi belajar."></textarea>
                        </div>

                        <button type="button" class="btn-generate" onclick="generateReport()">
                            <i class="fa-solid fa-wand-magic-sparkles"></i> Jana Laporan AI Sekarang
                        </button>
                    </div>

                    <!-- Output Panel -->
                    <div class="generator-output-wrapper">
                        <div>
                            <div class="output-header">
                                <h3><i class="fa-solid fa-robot"></i> Draf Laporan Pintar AI</h3>
                                <span class="ai-status-badge" id="aiStatus"><i class="fa-solid fa-circle" style="font-size: 8px;"></i> Sedia Diguna</span>
                            </div>

                            <div class="output-content" id="outputContent">
                                <div class="output-placeholder" id="outputPlaceholder">
                                    <i class="fa-solid fa-file-waveform"></i>
                                    <p>Sila lengkapkan pilihan borang di sebelah kiri dan klik butang <strong>"Jana Laporan AI Sekarang"</strong> untuk melihat hasil draf laporan profesional anda.</p>
                                </div>

                                <div class="output-section-item" id="boxPerkara">
                                    <h4>A. Perkara</h4>
                                    <p id="textPerkara"></p>
                                </div>

                                <div class="output-section-item" id="boxPersoalan">
                                    <h4>B. Persoalan</h4>
                                    <p id="textPersoalan"></p>
                                </div>

                                <div class="output-section-item" id="boxIntervensi">
                                    <h4>C. Intervensi GBK</h4>
                                    <p id="textIntervensi"></p>
                                </div>
                            </div>
                        </div>

                        <div class="output-actions" id="outputActions">
                            <button class="btn-action-sub" onclick="copyReport()"><i class="fa-solid fa-copy"></i> Salin Teks</button>
                            <button class="btn-action-sub" onclick="resetForm()"><i class="fa-solid fa-rotate-right"></i> Semula</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- 5. Why Choose e-Laporan GBK -->
    <section id="why-choose">
        <div class="section-header">
            <span class="section-badge">Kelebihan Sistem</span>
            <h2 class="section-title">Mengapa Memilih e-Laporan GBK?</h2>
            <p class="section-desc">Penyelesaian pintar yang dirangka khusus mengikut keperluan landskap pendidikan sekolah di Malaysia.</p>
        </div>
        <div class="why-grid">
            <div class="why-card">
                <div class="why-icon"><i class="fa-solid fa-clock"></i></div>
                <h3>Menjimatkan masa menyediakan laporan</h3>
                <p>Memotong masa penulisan dokumentasi manual sehingga 70%, membolehkan kaunselor lebih fokus kepada sesi bimbingan bersemuka.</p>
            </div>
            <div class="why-card">
                <div class="why-icon"><i class="fa-solid fa-clipboard-list"></i></div>
                <h3>Format sistematik dan profesional</h3>
                <p>Struktur ayat yang rapi, rasmi, serta mematuhi piawaian pelaporan kaunseling berkualiti tinggi untuk rujukan pentadbir sekolah.</p>
            </div>
            <div class="why-card">
                <div class="why-icon"><i class="fa-solid fa-folder-open"></i></div>
                <h3>Membantu dokumentasi GBK</h3>
                <p>Memastikan setiap fail kes, rekod bimbingan, dan rekod intervensi tersusun kemas, teratur serta mudah diakses pada bila-bila masa.</p>
            </div>
            <div class="why-card">
                <div class="why-icon"><i class="fa-solid fa-microchip"></i></div>
                <h3>Sokongan teknologi AI dalam kaunseling</h3>
                <p>Memanfaatkan keupayaan AI mutakhir bagi mencadangkan pandangan psikologi, persoalan terbuka, dan teknik terapi yang tepat.</p>
            </div>
        </div>
    </section>

    <!-- 6. Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-logo">
                <div class="nav-logo-mini">RR</div>
                e-Laporan GBK
            </div>
            <div class="footer-tagline">Innovation • Forward Together</div>
            <p class="footer-copyright">Hak Cipta Terpelihara © 2026 e-Laporan GBK. Direka khas untuk Guru Bimbingan dan Kaunseling Malaysia.</p>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Sub-fokus data options mapping
        const subFokusData = {
            "Pembangunan & Perkembangan Sahsiah Diri Murid": [
                "Keyakinan & Konsep Kendiri Positif",
                "Pengurusan Emosi & Kestabilan Diri",
                "Kemahiran Komunikasi & Interpersonal",
                "Ketahanan Diri (Resilience)"
            ],
            "Pendidikan Kerjaya Murid": [
                "Penerokaan Minat & Hala Tuju Selepas SPM",
                "Pemilihan Aliran Akademik / TVET",
                "Kesedaran Kerjaya Masa Depan",
                "Ujian Psikometrik & Profil Diri"
            ],
            "Peningkatan Disiplin Murid": [
                "Isu Kehadiran & Ponteng Sekolah",
                "Masalah Tingkah Laku & Salahlaku Disiplin",
                "Pengurusan Masa & Tanggungjawab",
                "Pengaruh Rakan Sebaya Negatif"
            ],
            "Psikososial & Kesejahteraan Mental Murid": [
                "Tekanan Akademik & Stres Peperiksaan",
                "Kebimbangan (Anxiety) & Kebosanan Belajar",
                "Hubungan Keluarga & Konflik Rumah Tangga",
                "Kesejahteraan Emosi Menyeluruh (Well-being)"
            ]
        };

        function updateSubFokus() {
            const fokusSelect = document.getElementById("fokusUtama");
            const subFokusSelect = document.getElementById("subFokus");
            const selectedFokus = fokusSelect.value;

            subFokusSelect.innerHTML = "";
            if (subFokusData[selectedFokus]) {
                subFokusData[selectedFokus].forEach(item => {
                    const opt = document.createElement("option");
                    opt.value = item;
                    opt.textContent = item;
                    subFokusSelect.appendChild(opt);
                });
            }
        }

        // Initialize sub-fokus on load
        window.onload = function() {
            updateSubFokus();
        };

        function generateReport() {
            const jenisSesi = document.getElementById("jenisSesi").value;
            const pendekatan = document.getElementById("pendekatan").value;
            const fokus = document.getElementById("fokusUtama").value;
            const subFokus = document.getElementById("subFokus").value;
            const teori = document.getElementById("teori").value;
            const isu = document.getElementById("isuMurid").value.trim() || "Murid menunjukkan keperluan bimbingan khusus bagi meningkatkan potensi diri dan pencapaian akademik.";

            // UI loading simulation
            const statusBadge = document.getElementById("aiStatus");
            statusBadge.innerHTML = `<i class="fa-solid fa-spinner fa-spin" style="font-size: 8px;"></i> AI Sedang Menjana...`;

            setTimeout(() => {
                statusBadge.innerHTML = `<i class="fa-solid fa-circle" style="font-size: 8px; color: var(--teal);"></i> Selesai Dijana`;

                // Hide placeholder, show items
                document.getElementById("outputPlaceholder").style.display = "none";
                document.getElementById("boxPerkara").classList.add("active");
                document.getElementById("boxPersoalan").classList.add("active");
                document.getElementById("boxIntervensi").classList.add("active");
                document.getElementById("outputActions").style.display = "flex";

                // Generate contextual professional text
                document.getElementById("textPerkara").textContent = 
                    `Sesi ${jenisSesi.toLowerCase()} dijalankan secara profesional berteraskan pendekatan ${pendekatan.toLowerCase()} dengan memberi penumpuan kepada aspek ${fokus.toLowerCase()} (${subFokus}). Berdasarkan maklumat yang diperoleh, isu utama yang dikenal pasti melibatkan aspek adaptasi murid di mana ${isu} Keadaan ini memerlukan perhatian dan tindakan bimbingan yang terancang agar potensi murid dapat dioptimumkan semula.`;

                document.getElementById("textPersoalan").textContent = 
                    `"Bagaimanakah cara terbaik untuk anda melihat diri anda mengatasi cabaran ini, dan apakah langkah pertama yang boleh anda ambil bermula hari ini?"`;

                let intervensiText = "";
                if (teori === "Reality Therapy") {
                    intervensiText = `Menggunakan kerangka pilihan (Choice Theory), kaunselor membimbing murid menilai tingkah laku semasa mereka sama ada ia membantu atau menghalang matlamat hidup mereka. Murid dibimbing merangka pelan WDEP (Wants, Direction, Evaluation, Plan) yang komprehensif bagi mencapai komitmen perubahan kendiri yang positif.`;
                } else if (teori === "CBT") {
                    intervensiText = `Melalui pendekatan Cognitive Behavioral Therapy (CBT), kaunselor membantu murid mengenal pasti corak pemikiran negatif (automatic negative thoughts) yang mempengaruhi emosi dan tindakan mereka. Seterusnya, latihan pencabar pemikiran dan modifikasi tingkah laku diperkenalkan untuk membina ketahanan mental yang lebih sihat.`;
                } else if (teori === "Person Centered") {
                    intervensiText = `Berdasarkan pendekatan Person-Centered Carl Rogers, kaunselor menyediakan suasana yang selamat, ikhlas, dan berempati tinggi (unconditional positive regard). Ini membolehkan murid meneroka perasaan sebenar mereka secara bebas, membina keyakinan diri, serta mencapai proses penerimaan kendiri (self-actualization).`;
                } else if (teori === "REBT") {
                    intervensiText = `Mengaplikasikan kerangka ABCDE model Rational Emotive Behavior Therapy, kaunselor membantu murid membezakan antara kepercayaan rasional dan tidak rasional yang mencetuskan tekanan. Intervensi berfokus kepada proses mencabar kepercayaan tidak rasional tersebut bagi melahirkan emosi dan tindak balas yang lebih adaptif.`;
                } else if (teori === "Solution Focused") {
                    intervensiText = `Melalui Solution-Focused Brief Therapy (SFBT), sesi memfokuskan kepada kekuatan dan sumber sedia ada pada diri murid (resourceful). Teknik 'Miracle Question' dan 'Scaling Questions' digunakan untuk merangka matlamat masa depan yang jelas tanpa terlalu menumpukan kepada sejarah masalah.`;
                } else {
                    intervensiText = `Menggunakan pendekatan Adlerian, kaunselor meneroka gaya hidup murid, rasa kepunyaan (sense of belonging), serta matlamat di sebalik tingkah laku mereka. Murid digalakkan untuk memperbetulkan tanggapan keliru serta membina keberanian sosial dan tanggungjawab kolektif dalam komuniti sekolah.`;
                }

                document.getElementById("textIntervensi").textContent = intervensiText;

            }, 600);
        }

        function copyReport() {
            const p = document.getElementById("textPerkara").textContent;
            const q = document.getElementById("textPersoalan").textContent;
            const i = document.getElementById("textIntervensi").textContent;

            const fullText = `A. PERKARA:\n${p}\n\nB. PERSOALAN:\n${q}\n\nC. INTERVENSI GBK:\n${i}`;

            navigator.clipboard.writeText(fullText).then(() => {
                alert("Laporan berjaya disalin ke papan keratan (clipboard)!");
            });
        }

        function resetForm() {
            document.getElementById("outputPlaceholder").style.display = "block";
            document.getElementById("boxPerkara").classList.remove("active");
            document.getElementById("boxPersoalan").classList.remove("active");
            document.getElementById("boxIntervensi").classList.remove("active");
            document.getElementById("outputActions").style.display = "none";
            document.getElementById("aiStatus").innerHTML = `<i class="fa-solid fa-circle" style="font-size: 8px;"></i> Sedia Diguna`;
            document.getElementById("isuMurid").value = "";
        }
    </script>
</body>
</html>
