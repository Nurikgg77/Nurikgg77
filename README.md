<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nurik - Full-Stack Developer | 3D Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html, body {
            height: 100%;
            width: 100%;
            overflow-x: hidden;
            background: #0f0f23;
            color: #ffffff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f0f23 0%, #1a0f3f 50%, #0f1f3f 100%);
            position: relative;
        }

        /* Animated background */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 50%, rgba(102, 126, 234, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(245, 87, 108, 0.1) 0%, transparent 50%);
            pointer-events: none;
            z-index: -1;
            animation: gradientShift 15s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.8;
            }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 1;
        }

        /* Header */
        header {
            text-align: center;
            padding: 3rem 0;
            margin-bottom: 4rem;
        }

        .logo {
            font-size: 32px;
            font-weight: 700;
            background: linear-gradient(135deg, #667eea, #764ba2, #f093fb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
        }

        .tagline {
            font-size: 14px;
            color: #888;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        /* Hero Section */
        .hero {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            margin-bottom: 6rem;
        }

        .hero-content h1 {
            font-size: 48px;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .hero-content p {
            font-size: 18px;
            color: #aaa;
            line-height: 1.8;
            margin-bottom: 2rem;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 32px;
            border: 2px solid;
            border-radius: 50px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-color: transparent;
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 24px rgba(102, 126, 234, 0.4);
        }

        .btn-secondary {
            border-color: #667eea;
            color: #667eea;
            background: transparent;
        }

        .btn-secondary:hover {
            background: rgba(102, 126, 234, 0.1);
        }

        /* 3D Card Container */
        .hero-3d {
            perspective: 1000px;
            height: 500px;
        }

        .card-3d {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        .card-3d-face {
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 20px;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .card-front {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
            backface-visibility: hidden;
        }

        .card-back {
            background: linear-gradient(135deg, rgba(240, 147, 251, 0.2), rgba(245, 87, 108, 0.2));
            transform: rotateY(180deg);
            backface-visibility: hidden;
        }

        .card-3d.flipped {
            transform: rotateY(180deg);
        }

        .skill-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .skill-item {
            padding: 1rem;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .skill-icon {
            font-size: 24px;
            margin-bottom: 0.5rem;
        }

        .skill-name {
            font-size: 13px;
            font-weight: 600;
        }

        .flip-text {
            font-size: 12px;
            color: #888;
            margin-top: 1rem;
            text-align: center;
        }

        /* Projects Section */
        .projects {
            margin-bottom: 6rem;
        }

        .section-title {
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            border-color: rgba(102, 126, 234, 0.5);
            box-shadow: 0 8px 32px rgba(102, 126, 234, 0.2);
            transform: translateY(-8px);
        }

        .project-icon {
            font-size: 32px;
            margin-bottom: 1rem;
        }

        .project-title {
            font-size: 20px;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .project-desc {
            font-size: 14px;
            color: #aaa;
            line-height: 1.6;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tech-badge {
            background: rgba(102, 126, 234, 0.2);
            color: #667eea;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 500;
        }

        /* Skills Section */
        .skills {
            margin-bottom: 6rem;
            text-align: center;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-box {
            background: rgba(255, 255, 255, 0.05);
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 2rem 1.5rem;
            transition: all 0.3s ease;
        }

        .skill-box:hover {
            border-color: rgba(102, 126, 234, 0.5);
            transform: scale(1.05);
        }

        .skill-category {
            font-size: 24px;
            margin-bottom: 1rem;
        }

        .skill-box h3 {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .skill-box p {
            font-size: 12px;
            color: #888;
        }

        /* Contact Section */
        .contact {
            text-align: center;
            padding: 3rem;
            background: rgba(102, 126, 234, 0.1);
            border-radius: 20px;
            border: 2px solid rgba(102, 126, 234, 0.2);
            margin-bottom: 4rem;
        }

        .contact h2 {
            font-size: 32px;
            margin-bottom: 2rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            text-decoration: none;
            color: white;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-color: transparent;
            transform: translateY(-4px);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 2px solid rgba(255, 255, 255, 0.1);
            color: #666;
            font-size: 14px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                grid-template-columns: 1fr;
            }

            .hero-content h1 {
                font-size: 32px;
            }

            .hero-3d {
                height: 300px;
            }

            .section-title {
                font-size: 24px;
            }

            .container {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="bg-animation"></div>

    <header>
        <div class="logo">◆ NURIK.DEV</div>
        <p class="tagline">Full-Stack Developer | Creative Coder</p>
    </header>

    <div class="container">
        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-content">
                <h1>Привет, я Nurik 👨‍💻</h1>
                <p>Разработчик, создающий цифровые продукты, которые вдохновляют. Специализируюсь на создании полного цикла веб-приложений, мобильных решений и современных интерфейсов.</p>
                <div class="cta-buttons">
                    <button class="btn btn-primary" onclick="viewProjects()">Смотреть Проекты</button>
                    <button class="btn btn-secondary" onclick="contactMe()">Написать Мне</button>
                </div>
            </div>

            <div class="hero-3d">
                <div class="card-3d" id="card3d">
                    <div class="card-3d-face card-front">
                        <div style="text-align: center;">
                            <div style="font-size: 80px; margin-bottom: 1rem;">👨‍💻</div>
                            <h2 style="font-size: 24px; font-weight: 700; margin-bottom: 1rem;">NURIK</h2>
                            <p style="color: #aaa; font-size: 14px;">Full-Stack Developer</p>
                            <div style="margin-top: 2rem;">
                                <p style="font-size: 13px; color: #888;">2+ лет опыта</p>
                            </div>
                        </div>
                        <p class="flip-text">Нажми для деталей →</p>
                    </div>

                    <div class="card-3d-face card-back">
                        <div class="skill-grid">
                            <div class="skill-item">
                                <div class="skill-icon">🎨</div>
                                <div class="skill-name">Frontend</div>
                            </div>
                            <div class="skill-item">
                                <div class="skill-icon">⚙️</div>
                                <div class="skill-name">Backend</div>
                            </div>
                            <div class="skill-item">
                                <div class="skill-icon">📱</div>
                                <div class="skill-name">Mobile</div>
                            </div>
                            <div class="skill-item">
                                <div class="skill-icon">🚀</div>
                                <div class="skill-name">DevOps</div>
                            </div>
                        </div>
                        <p class="flip-text">← Назад</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="projects">
            <h2 class="section-title">Мои Проекты</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-icon">🛍️</div>
                    <h3 class="project-title">E-Commerce Shop</h3>
                    <p class="project-desc">Полнофункциональный интернет-магазин с системой управления товарами</p>
                    <div class="project-tech">
                        <span class="tech-badge">Laravel</span>
                        <span class="tech-badge">MySQL</span>
                        <span class="tech-badge">JavaScript</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">🚗</div>
                    <h3 class="project-title">Car Shop Platform</h3>
                    <p class="project-desc">Специализированная платформа для продажи автомобилей</p>
                    <div class="project-tech">
                        <span class="tech-badge">Laravel</span>
                        <span class="tech-badge">Blade</span>
                        <span class="tech-badge">PHP</span>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">👤</div>
                    <h3 class="project-title">GitHub Profile</h3>
                    <p class="project-desc">Интерактивный профиль с динамической статистикой</p>
                    <div class="project-tech">
                        <span class="tech-badge">HTML/CSS</span>
                        <span class="tech-badge">GitHub</span>
                        <span class="tech-badge">API</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section class="skills">
            <h2 class="section-title">Мои Навыки</h2>
            <div class="skills-grid">
                <div class="skill-box">
                    <div class="skill-category">🎨</div>
                    <h3>Frontend</h3>
                    <p>React, HTML5, CSS3, JavaScript</p>
                </div>
                <div class="skill-box">
                    <div class="skill-category">⚙️</div>
                    <h3>Backend</h3>
                    <p>PHP, Laravel, Node.js, Python</p>
                </div>
                <div class="skill-box">
                    <div class="skill-category">💾</div>
                    <h3>Databases</h3>
                    <p>MySQL, SQL, Query Optimization</p>
                </div>
                <div class="skill-box">
                    <div class="skill-category">📱</div>
                    <h3>Mobile</h3>
                    <p>Flutter, Cross-Platform Apps</p>
                </div>
                <div class="skill-box">
                    <div class="skill-category">🔧</div>
                    <h3>Tools</h3>
                    <p>Git, Docker, VS Code, Figma</p>
                </div>
                <div class="skill-box">
                    <div class="skill-category">🚀</div>
                    <h3>Deployment</h3>
                    <p>REST APIs, CI/CD, Cloud Basics</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section class="contact">
            <h2>Давай Поработаем Вместе!</h2>
            <p style="color: #aaa; margin-bottom: 2rem; font-size: 16px;">Я открыт для интересных проектов и сотрудничества</p>
            <div class="social-links">
                <a href="https://github.com/Nurikgg77" class="social-link" target="_blank">📧</a>
                <a href="https://t.me/Nurikgg77" class="social-link" target="_blank">💬</a>
                <a href="https://instagram.com/nurik_prgrm" class="social-link" target="_blank">📸</a>
                <a href="https://www.tiktok.com/@ggnurik77" class="social-link" target="_blank">🎵</a>
            </div>
            <button class="btn btn-primary" onclick="contactMe()">Отправить Сообщение</button>
        </section>
    </div>

    <footer>
        <p>© 2026 Nurik. Создано с ❤️ | All Rights Reserved</p>
    </footer>

    <script>
        // 3D Card Flip
        const card3d = document.getElementById('card3d');
        let isFlipped = false;

        card3d.addEventListener('click', () => {
            isFlipped = !isFlipped;
            card3d.classList.toggle('flipped');
        });

        // Mouse move 3D effect
        document.addEventListener('mousemove', (e) => {
            if (isFlipped) return;
            
            const rect = card3d.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            const centerX = rect.width / 2;
            const centerY = rect.height / 2;
            
            const rotateX = (y - centerY) / 20;
            const rotateY = (centerX - x) / 20;
            
            card3d.style.transform = `rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
        });

        document.addEventListener('mouseleave', () => {
            if (!isFlipped) {
                card3d.style.transform = 'rotateX(0) rotateY(0)';
            }
        });

        // Functions
        function viewProjects() {
            document.querySelector('.projects').scrollIntoView({ behavior: 'smooth' });
        }

        function contactMe() {
            window.location.href = 'https://t.me/Nurikgg77';
        }
    </script>
</body>
</html>
