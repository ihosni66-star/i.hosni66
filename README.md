<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>شركة نمو أعمال للتشغيل والصيانة</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@200;300;400;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 60px 0;
            position: relative;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,122.7C672,117,768,139,864,133.3C960,128,1056,96,1152,90.7C1248,85,1344,107,1392,117.3L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>') no-repeat center bottom;
            background-size: cover;
        }

        .logo {
            font-size: 4rem;
            font-weight: 900;
            color: #ffffff;
            text-shadow: 0 4px 20px rgba(0,0,0,0.3);
            margin-bottom: 20px;
            animation: fadeInDown 1s ease-out;
        }

        .company-name {
            font-size: 2.5rem;
            font-weight: 700;
            color: #f8f9fa;
            margin-bottom: 10px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .company-subtitle {
            font-size: 1.3rem;
            font-weight: 400;
            color: #e9ecef;
            margin-bottom: 40px;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        /* Services Section */
        .services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease-out;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
        }

        .service-icon {
            font-size: 4rem;
            margin-bottom: 20px;
            display: block;
        }

        .service-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 15px;
        }

        .service-description {
            font-size: 1.1rem;
            color: #6c757d;
            line-height: 1.6;
        }

        /* About Section */
        .about {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 25px;
            padding: 60px 40px;
            margin: 60px 0;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            animation: fadeIn 1s ease-out 0.9s both;
        }

        .about-title {
            font-size: 3rem;
            font-weight: 800;
            color: #2c3e50;
            margin-bottom: 30px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .about-text {
            font-size: 1.3rem;
            color: #495057;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto 40px;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .stat-item {
            padding: 20px;
            border-radius: 15px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            display: block;
        }

        .stat-label {
            font-size: 1.1rem;
            font-weight: 400;
            margin-top: 10px;
        }

        /* Contact Section */
        .contact {
            text-align: center;
            padding: 60px 0;
            color: white;
        }

        .contact-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 30px;
            animation: fadeInUp 1s ease-out 1.2s both;
        }

        .contact-info {
            font-size: 1.2rem;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease-out 1.5s both;
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .logo {
                font-size: 2.5rem;
            }
            
            .company-name {
                font-size: 1.8rem;
            }
            
            .company-subtitle {
                font-size: 1.1rem;
            }
            
            .about-title {
                font-size: 2rem;
            }
            
            .about-text {
                font-size: 1.1rem;
            }
            
            .service-card {
                padding: 30px 20px;
            }
        }

        /* Floating Elements */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-element:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }

        .floating-element:nth-child(3) {
            width: 60px;
            height: 60px;
            top: 80%;
            left: 20%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
            }
        }
    </style>
</head>
<body>
    <!-- Floating Background Elements -->
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>

    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <div class="logo">🏗️</div>
            <h1 class="company-name">شركة نمو أعمال</h1>
            <p class="company-subtitle">للتشغيل والصيانة</p>
        </header>

        <!-- Services Section -->
        <section class="services">
            <div class="service-card">
                <span class="service-icon">⚡</span>
                <h3 class="service-title">صيانة المعدات الكهربائية</h3>
                <p class="service-description">صيانة شاملة للأنظمة الكهربائية والمولدات والمعدات الكهربائية المتخصصة</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">⚙️</span>
                <h3 class="service-title">صيانة المعدات الميكانيكية</h3>
                <p class="service-description">خدمات صيانة متكاملة للتبريد والتكييف والمصاعد والمضخات</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🏥</span>
                <h3 class="service-title">صيانة المعدات الطبية</h3>
                <p class="service-description">صيانة متخصصة للأجهزة الطبية الدقيقة والغازات الطبية</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🛡️</span>
                <h3 class="service-title">السلامة والصحة المهنية</h3>
                <p class="service-description">تطوير وتنفيذ خطط السلامة الشاملة وإدارة المخاطر</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🧹</span>
                <h3 class="service-title">خدمات النظافة والزراعة</h3>
                <p class="service-description">خدمات تنظيف احترافية وصيانة المساحات الخضراء</p>
            </div>
            
            <div class="service-card">
                <span class="service-icon">🔧</span>
                <h3 class="service-title">الصيانة المدنية</h3>
                <p class="service-description">أعمال البناء والترميم والدهان والنجارة المتخصصة</p>
            </div>
        </section>

        <!-- About Section -->
        <section class="about">
            <h2 class="about-title">من نحن</h2>
            <p class="about-text">
                شركة نمو أعمال للتشغيل والصيانة هي شركة رائدة في مجال الصيانة المتكاملة، نقدم خدمات عالية الجودة 
                في صيانة المعدات الطبية والكهربائية والميكانيكية. نلتزم بمعايير الجودة العالمية ISO 9001 و ISO 14001، 
                ونضمن تقديم خدمات احترافية تلبي احتياجات عملائنا بأعلى مستويات الكفاءة والأمان.
            </p>
            
            <div class="stats">
                <div class="stat-item">
                    <span class="stat-number">5</span>
                    <span class="stat-label">سنوات خبرة</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">100+</span>
                    <span class="stat-label">مشروع مكتمل</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">50+</span>
                    <span class="stat-label">عميل راضي</span>
                </div>
                <div class="stat-item">
                    <span class="stat-number">24/7</span>
                    <span class="stat-label">دعم مستمر</span>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="contact">
            <h2 class="contact-title">تواصل معنا</h2>
            <p class="contact-info">📧 info@namoamal.com</p>
            <p class="contact-info">📱 +966 50 123 4567</p>
            <p class="contact-info">📍 المملكة العربية السعودية</p>
        </section>
    </div>
</body>
</html>
