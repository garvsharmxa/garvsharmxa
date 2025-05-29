<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Garv Sharma - Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .hero {
            text-align: center;
            padding: 4rem 0;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin: 2rem;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease-out;
        }
        
        .hero h3 {
            font-size: 1.5rem;
            font-weight: 400;
            color: #e0e7ff;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out 0.2s both;
        }
        
        .wave {
            display: inline-block;
            animation: wave 2s infinite;
            transform-origin: 70% 70%;
            margin-left: 10px;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-15deg); }
        }
        
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
        
        .card {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 2rem;
            margin: 2rem 0;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            animation: slideIn 0.8s ease-out;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }
        
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .section-title {
            font-size: 2rem;
            font-weight: 600;
            color: #ffffff;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .about-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 1rem;
            border-radius: 10px;
            color: #ffffff;
            transition: all 0.3s ease;
        }
        
        .about-item:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.02);
        }
        
        .about-item strong {
            color: #fbbf24;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1rem;
        }
        
        .social-btn {
            padding: 0.75rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .social-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: all 0.5s;
        }
        
        .social-btn:hover::before {
            left: 100%;
        }
        
        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .behance { background: linear-gradient(45deg, #1769ff, #4285f4); }
        .instagram { background: linear-gradient(45deg, #833ab4, #fd1d1d, #fcb045); }
        .linkedin { background: linear-gradient(45deg, #0077b5, #00a0dc); }
        .twitter { background: linear-gradient(45deg, #1da1f2, #0d8bd9); }
        .youtube { background: linear-gradient(45deg, #ff0000, #cc0000); }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 1rem;
            border-radius: 15px;
            text-align: center;
            color: #ffffff;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .tech-item:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.05) rotate(2deg);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 1rem;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 1.5rem;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: scale(1.02);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #fbbf24;
            display: block;
        }
        
        .stat-label {
            color: #e0e7ff;
            font-weight: 500;
            margin-top: 0.5rem;
        }
        
        .quote-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.05));
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
            font-size: 1.2rem;
            color: #ffffff;
            font-style: italic;
            position: relative;
            overflow: hidden;
        }
        
        .quote-card::before {
            content: '"';
            position: absolute;
            top: -10px;
            left: 20px;
            font-size: 4rem;
            color: rgba(255, 255, 255, 0.3);
            font-family: serif;
        }
        
        .support-btn {
            display: inline-block;
            background: linear-gradient(45deg, #fbbf24, #f59e0b);
            color: #000;
            padding: 1rem 2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-top: 1rem;
        }
        
        .support-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(251, 191, 36, 0.3);
        }
        
        .visitor-count {
            text-align: center;
            margin-top: 2rem;
            color: #ffffff;
            font-size: 1.1rem;
        }
        
        .visitor-number {
            color: #fbbf24;
            font-weight: 600;
            font-size: 1.3rem;
        }
        
        .floating-shapes {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
            overflow: hidden;
        }
        
        .shape {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        .shape:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }
        
        .shape:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }
        
        .shape:nth-child(3) {
            width: 60px;
            height: 60px;
            bottom: 20%;
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
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero h3 {
                font-size: 1.2rem;
            }
            
            .container {
                padding: 1rem;
            }
            
            .social-links {
                gap: 0.5rem;
            }
            
            .social-btn {
                padding: 0.5rem 1rem;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-shapes">
        <div class="shape"></div>
        <div class="shape"></div>
        <div class="shape"></div>
    </div>
    
    <div class="container">
        <div class="hero">
            <div class="hero-content">
                <h1>Hi <span class="wave">👋</span>, I'm Garv Sharma</h1>
                <h3>🚀 Flutter & Django Enthusiast | Building NuminX | Tech Explorer</h3>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">💫 About Me</h2>
            <div class="about-grid">
                <div class="about-item">
                    <strong>🔭 Currently building:</strong> NuminX – Investing in Blue-Chip Crypto Assets for Long-Term Wealth
                </div>
                <div class="about-item">
                    <strong>🌱 Learning:</strong> DSA and New Skills
                </div>
                <div class="about-item">
                    <strong>💬 Ask me about:</strong> Flutter, App Development, APIs, Backend Integration
                </div>
                <div class="about-item">
                    <strong>📫 Reach me at:</strong> Via social links below
                </div>
                <div class="about-item">
                    <strong>⚡ Fun fact:</strong> I love mixing code with caffeine ☕ and creativity 🎨
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">🌐 Connect With Me</h2>
            <div class="social-links">
                <a href="https://behance.net/garvsharmxa" target="_blank" class="social-btn behance">Behance</a>
                <a href="https://instagram.com/garvsharmxa" target="_blank" class="social-btn instagram">Instagram</a>
                <a href="https://linkedin.com/in/garvsharmxa" target="_blank" class="social-btn linkedin">LinkedIn</a>
                <a href="https://twitter.com/garvsharmxa_" target="_blank" class="social-btn twitter">Twitter</a>
                <a href="https://youtube.com/@@garv8342" target="_blank" class="social-btn youtube">YouTube</a>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">💻 Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">C</div>
                <div class="tech-item">C++</div>
                <div class="tech-item">Dart</div>
                <div class="tech-item">Python</div>
                <div class="tech-item">Java</div>
                <div class="tech-item">Flutter</div>
                <div class="tech-item">Django</div>
                <div class="tech-item">DjangoREST</div>
                <div class="tech-item">Firebase</div>
                <div class="tech-item">iOS</div>
                <div class="tech-item">Android</div>
                <div class="tech-item">Unity</div>
                <div class="tech-item">Unreal</div>
                <div class="tech-item">SQLite</div>
                <div class="tech-item">MySQL</div>
                <div class="tech-item">HTML5</div>
                <div class="tech-item">Canva</div>
                <div class="tech-item">Figma</div>
                <div class="tech-item">Blender</div>
                <div class="tech-item">Arduino</div>
                <div class="tech-item">Postman</div>
                <div class="tech-item">Notion</div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">📊 GitHub Stats</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <span class="stat-number">150+</span>
                    <div class="stat-label">Commits This Year</div>
                </div>
                <div class="stat-card">
                    <span class="stat-number">25+</span>
                    <div class="stat-label">Public Repositories</div>
                </div>
                <div class="stat-card">
                    <span class="stat-number">10+</span>
                    <div class="stat-label">Languages Used</div>
                </div>
                <div class="stat-card">
                    <span class="stat-number">50+</span>
                    <div class="stat-label">Stars Earned</div>
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">✍️ Random Dev Quote</h2>
            <div class="quote-card">
                <p id="quote">"Code is like humor. When you have to explain it, it's bad." – Cory House</p>
            </div>
        </div>
        
        <div class="card">
            <h2 class="section-title">💰 Support My Work</h2>
            <div style="text-align: center;">
                <a href="https://buymeacoffee.com/xgrave" target="_blank" class="support-btn">
                    ☕ Buy Me a Coffee
                </a>
            </div>
        </div>
        
        <div class="visitor-count">
            <div>🚀 Profile Views: <span class="visitor-number" id="visitorCount">1,234</span></div>
        </div>
    </div>
    
    <script>
        // Animate visitor count
        function animateCounter() {
            const counter = document.getElementById('visitorCount');
            const target = 1234;
            let current = 0;
            const increment = target / 100;
            
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    current = target;
                    clearInterval(timer);
                }
                counter.textContent = Math.floor(current).toLocaleString();
            }, 20);
        }
        
        // Random dev quotes
        const quotes = [
            '"Code is like humor. When you have to explain it, it\'s bad." – Cory House',
            '"First, solve the problem. Then, write the code." – John Johnson',
            '"Experience is the name everyone gives to their mistakes." – Oscar Wilde',
            '"Any fool can write code that a computer can understand. Good programmers write code that humans can understand." – Martin Fowler',
            '"The best error message is the one that never shows up." – Thomas Fuchs'
        ];
        
        function updateQuote() {
            const quoteElement = document.getElementById('quote');
            const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
            quoteElement.textContent = randomQuote;
        }
        
        // Initialize animations
        document.addEventListener('DOMContentLoaded', function() {
            animateCounter();
            setInterval(updateQuote, 5000); // Change quote every 5 seconds
        });
        
        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.card').forEach(card => {
            observer.observe(card);
        });
    </script>
</body>
</html>
