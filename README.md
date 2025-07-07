<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aumkesh Chaudhary - Digital Architect</title>
    <!-- Font Awesome for icons -->

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">


    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Cormorant+Garamond:wght@300;400;600&display=swap');
        
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Cormorant Garamond', serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 30%, #16213e 60%, #0f0f0f 100%);
            color: #e0e0e0;
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #fff;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }
        
        .container {
            position: relative;
            z-index: 2;
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
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(138, 43, 226, 0.1) 0%, transparent 70%);
            animation: pulse 8s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }
        
        .name {
            font-family: 'Cinzel', serif;
            font-size: 4rem;
            font-weight: 700;
            background: linear-gradient(45deg, #8A2BE2, #9370DB, #DDA0DD, #8A2BE2);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 6s ease infinite;
            text-shadow: 0 0 50px rgba(138, 43, 226, 0.5);
            margin-bottom: 1rem;
            transform: perspective(1000px) rotateX(10deg);
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: #b19cd9;
            margin-bottom: 2rem;
            font-weight: 300;
            letter-spacing: 2px;
            text-shadow: 0 0 20px rgba(177, 156, 217, 0.5);
        }
        
        .typing-effect {
            font-size: 1.2rem;
            color: #dda0dd;
            min-height: 2rem;
            margin-bottom: 3rem;
            position: relative;
        }
        
        .typing-effect::after {
            content: '|';
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0; }
        }
        
        .section {
            margin: 4rem 0;
            padding: 2rem;
            background: rgba(20, 20, 20, 0.8);
            border-radius: 20px;
            border: 1px solid rgba(138, 43, 226, 0.3);
            backdrop-filter: blur(10px);
            transform: perspective(1000px) rotateY(2deg);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .section::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #8A2BE2, #9370DB, #DDA0DD, #8A2BE2);
            border-radius: 20px;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .section:hover::before {
            opacity: 0.5;
        }
        
        .section:hover {
            transform: perspective(1000px) rotateY(0deg) scale(1.02);
            box-shadow: 0 20px 40px rgba(138, 43, 226, 0.3);
        }
        
        .section-title {
            font-family: 'Cinzel', serif;
            font-size: 2.5rem;
            color: #9370DB;
            margin-bottom: 1.5rem;
            text-align: center;
            text-shadow: 0 0 30px rgba(147, 112, 219, 0.5);
        }
        
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .about-card {
            background: rgba(30, 30, 30, 0.9);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(138, 43, 226, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .about-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(138, 43, 226, 0.1), transparent);
            transition: left 0.5s ease;
        }
        
        .about-card:hover::before {
            left: 100%;
        }
        
        .about-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(138, 43, 226, 0.2);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .skill-item {
            background: rgba(30, 30, 30, 0.9);
            padding: 1.5rem;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(138, 43, 226, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .skill-item::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: radial-gradient(circle, rgba(138, 43, 226, 0.3) 0%, transparent 70%);
            transition: all 0.3s ease;
            transform: translate(-50%, -50%);
        }
        
        .skill-item:hover::before {
            width: 200%;
            height: 200%;
        }
        
        .skill-item:hover {
            transform: translateY(-10px) scale(1.1);
            box-shadow: 0 15px 30px rgba(138, 43, 226, 0.3);
        }
        
        .skill-icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            color: #9370DB;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-link {
            display: block;
            padding: 1.5rem;
            background: rgba(30, 30, 30, 0.9);
            border-radius: 15px;
            text-decoration: none;
            color: #e0e0e0;
            border: 1px solid rgba(138, 43, 226, 0.2);
            transition: all 0.3s ease;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .contact-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(138, 43, 226, 0.1), rgba(147, 112, 219, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .contact-link:hover::before {
            opacity: 1;
        }
        
        .contact-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(138, 43, 226, 0.3);
        }
        
        .quote {
            text-align: center;
            font-size: 1.3rem;
            font-style: italic;
            color: #b19cd9;
            margin: 3rem 0;
            padding: 2rem;
            background: rgba(20, 20, 20, 0.6);
            border-radius: 15px;
            border: 1px solid rgba(138, 43, 226, 0.2);
            position: relative;
        }
        
        .quote::before {
            content: '"';
            font-size: 4rem;
            color: #8A2BE2;
            position: absolute;
            top: -1rem;
            left: 1rem;
            opacity: 0.3;
        }
        
        .quote::after {
            content: '"';
            font-size: 4rem;
            color: #8A2BE2;
            position: absolute;
            bottom: -3rem;
            right: 1rem;
            opacity: 0.3;
        }
        
        .floating-element {
            position: fixed;
            pointer-events: none;
            z-index: 1;
        }
        
        .floating-orb {
            width: 100px;
            height: 100px;
            background: radial-gradient(circle, rgba(138, 43, 226, 0.3) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .particle {
            position: fixed;
            width: 3px;
            height: 3px;
            background: #8A2BE2;
            border-radius: 50%;
            pointer-events: none;
            z-index: 1;
        }
        
        @media (max-width: 768px) {
            .name {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .about-grid,
            .skills-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }
            
            .section {
                transform: none;
                margin: 2rem 0;
            }
        }
    </style>
</head>
<body>
    <div class="stars"></div>

    <div class="container">
        <div class="hero">
            <h1 class="name">Aumkesh Chaudhary</h1>
            <p class="subtitle">Digital Architect of Tomorrow</p>
            <div class="typing-effect" id="typing-text"></div>
        </div>

        <div class="section">
            <h2 class="section-title">∞ About Me</h2>
            <div class="about-grid">
                <div class="about-card">
                    <h3 style="color: #9370DB; margin-bottom: 1rem;">🎓 Academic Journey</h3>
                    <p>BS in Computer Science and Data Analytics at the Indian Institute of Technology, Patna. Investigating complex systems through a lens of both structure and curiosity.</p>
                </div>
                <div class="about-card">
                    <h3 style="color: #9370DB; margin-bottom: 1rem;">🧠 Research Passion</h3>
                    <p>Exploring the depths of Machine Learning, Mathematical Modeling, and Scientific Simulations. Bridging the gap between theoretical knowledge and real-world applications.</p>
                </div>
                <div class="about-card">
                    <h3 style="color: #9370DB; margin-bottom: 1rem;">🔬 Philosophy</h3>
                    <p>Driven by curiosity and guided by logic, I believe in learning through building, experimenting, and asking the right questions. Every problem is a puzzle waiting to be solved.</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">Technical Competence</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-python"></i></div>
                    <div>Python</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-java"></i></div>
                    <div>Java</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-chart-line"></i></div>
                    <div>R</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <div>SQL</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-linux"></i></div>
                    <div>Linux</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-git-alt"></i></div>
                    <div>Git</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-react"></i></div>
                    <div>React</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-globe"></i></div>
                    <div>Django</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-vials"></i></div>
                    <div>MATLAB</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title"> Current Explorations</h2>
            <div class="about-grid">
                <div class="about-card">
                    <h3 style="color: #9370DB; margin-bottom: 1rem;">🧮 Scientific Computing</h3>
                    <p>Delving into advanced mathematical modeling and computational simulations that bridge theoretical concepts with practical applications.</p>
                </div>
                <div class="about-card">
                    <h3 style="color: #9370DB; margin-bottom: 1rem;">🎯 Advanced ML</h3>
                    <p>Mastering Reinforcement Learning, Bayesian Inference, and cutting-edge Deep Learning architectures for Vision and Language processing.</p>
                </div>
                <div class="about-card">
    <h3 style="color: #6B8E23; margin-bottom: 1rem;">🌿 Ecology</h3>
    <p>Investigating the complex interactions within ecosystems using computational approaches, with a focus on understanding animal behavior and environmental dynamics.</p>
</div>

            </div>
        </div>

        <div class="section">
    <h2 class="section-title">🌐 Connect with Me</h2>
    <div class="contact-grid">
        <a href="mailto:aumkeshchaudhary@gmail.com" class="contact-link">
            <div style="font-size: 2rem; margin-bottom: 0.5rem;">
                <i class="fas fa-envelope"></i>
            </div>
            <div>Email</div>
        </a>
        <a href="https://www.linkedin.com/in/aumkeshchaudhary/" class="contact-link" target="_blank">
            <div style="font-size: 2rem; margin-bottom: 0.5rem;">
                <i class="fab fa-linkedin"></i>
            </div>
            <div>LinkedIn</div>
        </a>
        <a href="https://github.com/aumkeshchaudhary" class="contact-link" target="_blank">
            <div style="font-size: 2rem; margin-bottom: 0.5rem;">
                <i class="fab fa-github"></i>
            </div>
            <div>GitHub</div>
        </a>
    </div>
</div>


        <div class="quote">
            The most beautiful thing we can experience is the mysterious. It is the source of all true art and science.
            <br><br>
            <em>— Albert Einstein</em>
        </div>
    </div>

    <!-- Floating elements and scripts -->
    <div class="floating-element floating-orb" style="top: 10%; left: 10%;"></div>
    <div class="floating-element floating-orb" style="top: 60%; right: 10%; animation-delay: -2s;"></div>
    <div class="floating-element floating-orb" style="bottom: 20%; left: 20%; animation-delay: -4s;"></div>

    <script>
        // JavaScript unchanged – stars, typing effect, particles, etc.
        // Keep all existing JavaScript as-is
        function createStars() {
            const starsContainer = document.querySelector('.stars');
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 3 + 's';
                starsContainer.appendChild(star);
            }
        }

        function typeText() {
            const texts = [
                "Aspiring Researcher | Data Thinker",
                "ML | AI | Mathematical Modeling",
                "Exploring Intelligence Through Computation",
                "Building Tomorrow's Solutions Today"
            ];
            let textIndex = 0;
            let charIndex = 0;
            let isDeleting = false;
            const typingElement = document.getElementById('typing-text');

            function type() {
                const currentText = texts[textIndex];

                if (isDeleting) {
                    typingElement.textContent = currentText.substring(0, charIndex - 1);
                    charIndex--;
                } else {
                    typingElement.textContent = currentText.substring(0, charIndex + 1);
                    charIndex++;
                }

                if (!isDeleting && charIndex === currentText.length) {
                    setTimeout(() => isDeleting = true, 2000);
                } else if (isDeleting && charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % texts.length;
                }

                setTimeout(type, isDeleting ? 50 : 100);
            }

            type();
        }

        function createParticles() {
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 5 + 's';
                document.body.appendChild(particle);

                let x = Math.random() * window.innerWidth;
                let y = Math.random() * window.innerHeight;
                let vx = (Math.random() - 0.5) * 2;
                let vy = (Math.random() - 0.5) * 2;

                function animateParticle() {
                    x += vx;
                    y += vy;

                    if (x < 0 || x > window.innerWidth) vx *= -1;
                    if (y < 0 || y > window.innerHeight) vy *= -1;

                    particle.style.left = x + 'px';
                    particle.style.top = y + 'px';

                    requestAnimationFrame(animateParticle);
                }

                animateParticle();
            }
        }

        document.addEventListener('mousemove', (e) => {
            const cursor = document.createElement('div');
            cursor.style.position = 'fixed';
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
            cursor.style.width = '10px';
            cursor.style.height = '10px';
            cursor.style.background = 'rgba(138, 43, 226, 0.5)';
            cursor.style.borderRadius = '50%';
            cursor.style.pointerEvents = 'none';
            cursor.style.zIndex = '1000';
            cursor.style.animation = 'fade-out 1s ease-out forwards';
            document.body.appendChild(cursor);

            setTimeout(() => {
                cursor.remove();
            }, 1000);
        });

        const style = document.createElement('style');
        style.textContent = `
            @keyframes fade-out {
                from { opacity: 1; transform: scale(1); }
                to { opacity: 0; transform: scale(0); }
            }
        `;
        document.head.appendChild(style);

        createStars();
        typeText();
        createParticles();

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        });

        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
    </script>
</body>
</html>
