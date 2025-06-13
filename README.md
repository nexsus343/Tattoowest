```html
<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tattoo_west - Студія тату</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a1a1a;
            --secondary: #e63946;
            --accent: #f1faee;
            --light: #f8f9fa;
            --gold: #ffd700;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--primary);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: rgba(26, 26, 26, 0.95);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 15px;
        }
        
        .logo h1 {
            font-size: 28px;
            color: var(--light);
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: var(--light);
            text-decoration: none;
            text-transform: uppercase;
            font-size: 14px;
            font-weight: 500;
            letter-spacing: 1px;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary);
            bottom: 0;
            left: 0;
            transition: var(--transition);
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1605640840605-14ac1855827b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 4rem;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            text-transform: uppercase;
            font-weight: 500;
            letter-spacing: 1px;
            transition: var(--transition);
            border: 2px solid var(--secondary);
        }
        
        .btn:hover {
            background: transparent;
            color: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        /* Services Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background: var(--secondary);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            text-align: center;
            padding: 30px;
            backdrop-filter: blur(10px);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            background: rgba(230, 57, 70, 0.1);
        }
        
        .service-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        /* Artists Section */
        .artists {
            background: url('https://images.unsplash.com/photo-1579546929662-711aa81148cf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1920&q=80');
            background-attachment: fixed;
            background-size: cover;
            position: relative;
        }
        
        .artists::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(26, 26, 26, 0.9);
        }
        
        .artists .container {
            position: relative;
            z-index: 2;
        }
        
        .artists-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .artist-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            transition: var(--transition);
            text-align: center;
        }
        
        .artist-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
        }
        
        .artist-img {
            height: 300px;
            overflow: hidden;
        }
        
        .artist-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .artist-card:hover .artist-img img {
            transform: scale(1.1);
        }
        
        .artist-info {
            padding: 20px;
        }
        
        .artist-info h3 {
            font-size: 1.5rem;
            margin-bottom: 5px;
        }
        
        .artist-info p {
            color: var(--secondary);
            font-style: italic;
            margin-bottom: 15px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 35px;
            height: 35px;
            background: var(--secondary);
            color: white;
            border-radius: 50%;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--light);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        /* Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }
        
        .gallery-item {
            height: 250px;
            overflow: hidden;
            border-radius: 5px;
            position: relative;
            cursor: pointer;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(230, 57, 70, 0.3);
            opacity: 0;
            transition: var(--transition);
        }
        
        .gallery-item:hover::after {
            opacity: 1;
        }
        
        /* Booking Section */
        .booking {
            background: linear-gradient(to right, var(--primary), #2a2a2a);
        }
        
        .booking-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .booking-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 5px;
            color: var(--light);
            font-family: 'Montserrat', sans-serif;
        }
        
        .form-group textarea {
            height: 120px;
            resize: none;
        }
        
        .booking-info h3 {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        
        .info-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }
        
        .info-icon {
            font-size: 1.5rem;
            color: var(--secondary);
            margin-right: 15px;
            min-width: 30px;
        }
        
        /* Footer */
        footer {
            background: #0d0d0d;
            padding: 60px 0 30px;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-col h4 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h4::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 2px;
            background: var(--secondary);
            bottom: 0;
            left: 0;
        }
        
        .footer-col p {
            margin-bottom: 15px;
        }
        
        .footer-links li {
            list-style: none;
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #aaa;
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .social-links-footer {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .booking-container {
                grid-template-columns: 1fr;
            }
            
            .hero h2 {
                font-size: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
            }
            
            .menu-toggle {
                display: block;
                font-size: 1.5rem;
                cursor: pointer;
            }
            
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 70px 0;
            }
        }
        
        @media (max-width: 480px) {
            .hero h2 {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <h1>TATTOO_<span>WEST</span></h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Головна</a></li>
                    <li><a href="#services">Послуги</a></li>
                    <li><a href="#artists">Майстри</a></li>
                    <li><a href="#gallery">Галерея</a></li>
                    <li><a href="#booking">Запис</a></li>
                    <li><a href="#contact">Контакти</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h2>СТВОРЮЄМО МИСТЕЦТВО НА ВАШОМУ ТІЛІ</h2>
            <p>Tattoo_west - це сучасний тату салон, де професійні майстри втілюють ваші ідеї в унікальні тату. Працюємо з найкращими матеріалами та дотримуємося найвищих стандартів безпеки.</p>
            <a href="#booking" class="btn">Записатися на сеанс</a>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Наші послуги</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3>Художнє татуювання</h3>
                    <p>Індивідуальний дизайн та виконання художніх татуювань будь-якої складності.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-redo"></i>
                    </div>
                    <h3>Перекриття татуювань</h3>
                    <p>Професійне перекриття старих або невдалих татуювань новим дизайном.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-eraser"></i>
                    </div>
                    <h3>Видалення татуювань</h3>
                    <p>Видалення небажаних татуювань за допомогою сучасних лазерних технологій.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-ring"></i>
                    </div>
                    <h3>Пірсинг</h3>
                    <p>Безпечний пірсинг різних частин тіла з використанням гіпоалергенних матеріалів.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-pencil-alt"></i>
                    </div>
                    <h3>Консультація та дизайн</h3>
                    <p>Розробка індивідуального дизайну та консультація з професійним майстром.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-first-aid"></i>
                    </div>
                    <h3>Догляд після процедур</h3>
                    <p>Рекомендації та професійні засоби для правильного догляду за татуюванням.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Artists Section -->
    <section class="section artists" id="artists">
        <div class="container">
            <div class="section-title">
                <h2>Наші майстри</h2>
            </div>
            <div class="artists-grid">
                <div class="artist-card">
                    <div class="artist-img">
                        <img src="https://images.unsplash.com/photo-1579546929662-711aa81148cf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Майстер Олександр">
                    </div>
                    <div class="artist-info">
                        <h3>Олександр</h3>
                        <p>Художник-татуїст</p>
                        <p>Спеціалізація: орнаментальний стиль, графика</p>
                        <div class="social-links">
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                        </div>
                    </div>
                </div>
                <div class="artist-card">
                    <div class="artist-img">
                        <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Майстер Катерина">
                    </div>
                    <div class="artist-info">
                        <h3>Катерина</h3>
                        <p>Майстер пірсингу</p>
                        <p>Спеціалізація: мікродермалі, класичний пірсинг</p>
                        <div class="social-links">
                            <a href="#"><i class="fab fa-instagram"></i></a>
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                        </div>
                    </div>
                </div>
                <div class="artist-card">
                    <div class="artist-img">
                        <img src="https://images.unsplash.com/photo-1567532939604-b6b5b0e160de
