<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rishabh Jaiswal - Data Analyst & Operations Specialist</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Taurus, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .header .subtitle {
            font-size: 1.2em;
            color: #666;
            margin-bottom: 20px;
        }

        .typing-animation {
            font-size: 1.1em;
            color: #0E75B6;
            font-weight: 500;
            min-height: 30px;
        }

        /* Navigation */
        .nav-tabs {
            display: flex;
            justify-content: center;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 10px;
            margin-bottom: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }

        .nav-tab {
            background: none;
            border: none;
            padding: 12px 25px;
            cursor: pointer;
            border-radius: 10px;
            margin: 0 5px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .nav-tab.active {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            transform: translateY(-2px);
        }

        .nav-tab:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Content Sections */
        .content-section {
            display: none;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .content-section.active {
            display: block;
            animation: fadeInUp 0.6s ease;
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

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .skill-category {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            border-radius: 15px;
            padding: 25px;
            color: white;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
        }

        .skill-category h3 {
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .skill-item {
            background: rgba(255, 255, 255, 0.2);
            margin: 8px 0;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9em;
        }

        /* Tech Stack */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 20px 0;
        }

        .tech-item {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 12px 20px;
            border-radius: 25px;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tech-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(79, 172, 254, 0.4);
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            padding-left: 30px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 15px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(135deg, #667eea, #764ba2);
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            padding: 25px;
            border-radius: 15px;
            margin-left: 20px;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -35px;
            top: 25px;
            width: 10px;
            height: 10px;
            background: #667eea;
            border-radius: 50%;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-5px);
        }

        .contact-item i {
            font-size: 2em;
            margin-bottom: 10px;
            color: #667eea;
        }

        .contact-item a {
            color: #333;
            text-decoration: none;
            font-weight: 500;
        }

        /* Analytics Dashboard */
        .analytics-dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .metric-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .metric-card:hover {
            transform: translateY(-5px);
        }

        .metric-value {
            font-size: 2em;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .metric-label {
            font-size: 0.9em;
            opacity: 0.9;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2em;
            }
            
            .nav-tabs {
                flex-wrap: wrap;
            }
            
            .content-section {
                padding: 20px;
            }
            
            .skills-grid,
            .contact-grid,
            .analytics-dashboard {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header fade-in">
            <div class="profile-img">
                <i class="fas fa-chart-line"></i>
            </div>
            <h1>Hi 👋, I'm Rishabh Jaiswal</h1>
            <p class="subtitle">📊 Data Analyst & Operations Specialist | 💼 Affiliate Marketing Professional 🚀</p>
            <div class="typing-animation" id="typingText">
                📊 Data Analytics Enthusiast
            </div>
        </div>

        <!-- Navigation -->
        <div class="nav-tabs fade-in">
            <button class="nav-tab active" onclick="showSection('about')">About Me</button>
            <button class="nav-tab" onclick="showSection('skills')">Skills</button>
            <button class="nav-tab" onclick="showSection('experience')">Experience</button>
            <button class="nav-tab" onclick="showSection('analytics')">Analytics</button>
            <button class="nav-tab" onclick="showSection('contact')">Contact</button>
        </div>

        <!-- About Section -->
        <div id="about" class="content-section active">
            <h2><i class="fas fa-user"></i> About Me</h2>
            <p style="font-size: 1.1em; margin: 20px 0;">
                🔭 I'm currently working as an <strong>Operations Analyst</strong> at <strong>Adcounty Media Ltd</strong> - 
                focusing on Affiliate Marketing & Advertising Services.
            </p>
            <p style="margin: 15px 0;">
                🌱 I'm currently learning <strong>Data Analytics</strong> from <strong>CodeBasics</strong> and expanding my skills in 
                <strong>🐍 Python & 🗄️ SQL</strong>
            </p>
            <p style="margin: 15px 0;">
                📊 Passionate about <strong>📈 Data-Driven Decision Making</strong> and <strong>📊 Performance Marketing Analytics</strong>
            </p>
            <p style="margin: 15px 0;">
                🌍 Based in <strong>Gurugram, Haryana, India</strong> 📍
            </p>
            <p style="margin: 15px 0;">
                🎯 Goal: <strong>Become a Senior Data Analyst by 2025</strong> 🚀
            </p>
            <div style="text-align: center; margin: 30px 0;">
                <img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" 
                     alt="Data Analytics" style="max-width: 300px; border-radius: 15px;">
            </div>
        </div>

        <!-- Skills Section -->
        <div id="skills" class="content-section">
            <h2><i class="fas fa-tools"></i> Technical Skills</h2>
            <div class="tech-stack">
                <span class="tech-item">🐍 Python</span>
                <span class="tech-item">🗄️ SQL/MySQL</span>
                <span class="tech-item">📊 Pandas</span>
                <span class="tech-item">🔢 NumPy</span>
                <span class="tech-item">📈 Matplotlib</span>
                <span class="tech-item">🎨 Seaborn</span>
                <span class="tech-item">📊 Power BI</span>
                <span class="tech-item">📈 Tableau</span>
                <span class="tech-item">💻 Jupyter</span>
                <span class="tech-item">📊 Excel</span>
                <span class="tech-item">🔧 Git</span>
            </div>

            <div class="skills-grid">
                <div class="skill-category">
                    <h3>🔍 Data Analysis</h3>
                    <div class="skill-item">📊 Exploratory Data Analysis (EDA)</div>
                    <div class="skill-item">📈 Statistical Analysis</div>
                    <div class="skill-item">🔢 Descriptive Statistics</div>
                    <div class="skill-item">📊 Data Cleaning & Preprocessing</div>
                    <div class="skill-item">🎯 A/B Testing</div>
                    <div class="skill-item">📉 Trend Analysis</div>
                </div>

                <div class="skill-category">
                    <h3>📊 Visualization & Reporting</h3>
                    <div class="skill-item">📊 Dashboard Creation</div>
                    <div class="skill-item">📈 Interactive Charts</div>
                    <div class="skill-item">📋 Business Reports</div>
                    <div class="skill-item">🎨 Data Storytelling</div>
                    <div class="skill-item">📊 KPI Monitoring</div>
                    <div class="skill-item">📈 Performance Metrics</div>
                </div>

                <div class="skill-category">
                    <h3>💼 Business Analytics</h3>
                    <div class="skill-item">🎯 Campaign Performance</div>
                    <div class="skill-item">📊 Conversion Tracking</div>
                    <div class="skill-item">💰 ROI Analysis</div>
                    <div class="skill-item">📈 Marketing Analytics</div>
                    <div class="skill-item">🔮 Predictive Analytics</div>
                    <div class="skill-item">📋 Business Intelligence</div>
                </div>
            </div>
        </div>

        <!-- Experience Section -->
        <div id="experience" class="content-section">
            <h2><i class="fas fa-briefcase"></i> Professional Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <h3>Operations Analyst</h3>
                    <h4>Adcounty Media Ltd</h4>
                    <p><i class="fas fa-calendar"></i> Present</p>
                    <ul style="margin-top: 15px;">
                        <li>💼 Managing affiliate marketing operations and advertising services</li>
                        <li>⚡ Optimizing campaign performance and conversion tracking</li>
                        <li>📊 Analyzing marketing data and ROI optimization</li>
                        <li>📈 Working with performance tracking and analytics</li>
                        <li>🔍 Data mining and insights generation</li>
                    </ul>
                </div>
            </div>

            <h3 style="margin-top: 30px;"><i class="fas fa-graduation-cap"></i> Current Learning</h3>
            <div class="timeline-item" style="margin-left: 0;">
                <h4>Data Analytics Course</h4>
                <p><strong>CodeBasics</strong></p>
                <p>Expanding skills in Python, SQL, and advanced data analytics techniques</p>
            </div>
        </div>

        <!-- Analytics Section -->
        <div id="analytics" class="content-section">
            <h2><i class="fas fa-chart-bar"></i> Data Analytics Journey</h2>
            <div style="text-align: center; margin: 20px 0;">
                <p style="font-size: 1.2em; background: linear-gradient(135deg, #667eea, #764ba2); 
                   color: white; padding: 20px; border-radius: 15px;">
                    📊 Data Collection → 🧹 Data Cleaning → 🔍 Analysis → 📈 Visualization → 💡 Insights → 📋 Decisions
                </p>
            </div>

            <div class="analytics-dashboard">
                <div class="metric-card">
                    <div class="metric-value">2+</div>
                    <div class="metric-label">Years Experience</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">10+</div>
                    <div class="metric-label">Tools & Technologies</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">100+</div>
                    <div class="metric-label">Campaigns Analyzed</div>
                </div>
                <div class="metric-card">
                    <div class="metric-value">∞</div>
                    <div class="metric-label">Insights Generated</div>
                </div>
            </div>

            <h3 style="margin-top: 30px;"><i class="fas fa-target"></i> Focus Areas</h3>
            <ul style="list-style: none; padding: 0;">
                <li style="margin: 10px 0;"><i class="fas fa-chart-line" style="color: #667eea;"></i> Data Analytics & Visualization</li>
                <li style="margin: 10px 0;"><i class="fas fa-database" style="color: #667eea;"></i> Database Management & SQL</li>
                <li style="margin: 10px 0;"><i class="fas fa-bullseye" style="color: #667eea;"></i> Marketing Analytics</li>
                <li style="margin: 10px 0;"><i class="fas fa-rocket" style="color: #667eea;"></i> Performance Optimization</li>
                <li style="margin: 10px 0;"><i class="fas fa-brain" style="color: #667eea;"></i> Predictive Analytics</li>
                <li style="margin: 10px 0;"><i class="fas fa-chart-pie" style="color: #667eea;"></i> Business Intelligence</li>
            </ul>
        </div>

        <!-- Contact Section -->
        <div id="contact" class="content-section">
            <h2><i class="fas fa-envelope"></i> Connect With Me</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <i class="fab fa-linkedin"></i>
                    <h3>LinkedIn</h3>
                    <a href="https://www.linkedin.com/in/rishabh-jaiswal-%F0%9F%87%AE%F0%9F%87%B3-499941219/" target="_blank">
                        Connect Professional Network
                    </a>
                </div>
                <div class="contact-item">
                    <i class="fab fa-instagram"></i>
                    <h3>Instagram</h3>
                    <a href="https://www.instagram.com/_.rishabh_jaiswal" target="_blank">
                        @_.rishabh_jaiswal
                    </a>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <h3>Email</h3>
                    <a href="mailto:your.email@example.com">
                        Send Message
                    </a>
                </div>
                <div class="contact-item">
                    <i class="fab fa-github"></i>
                    <h3>GitHub</h3>
                    <a href="https://github.com/rishabhjais" target="_blank">
                        View Projects
                    </a>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 30px;">
                <p style="font-size: 1.1em; color: #666;">
                    📍 Based in <strong>Gurugram, Haryana, India</strong>
                </p>
                <p style="margin-top: 10px;">
                    ⚡ Fun fact: <strong>I turn data into actionable insights (and yes, I'm still funny!) 😄</strong>
                </p>
            </div>
        </div>
    </div>

    <script>
        // Tab Navigation
        function showSection(sectionId) {
            // Hide all sections
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Remove active class from all tabs
            document.querySelectorAll('.nav-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById(sectionId).classList.add('active');
            
            // Add active class to clicked tab
            event.target.classList.add('active');
        }

        // Typing Animation
        const phrases = [
            "📊 Data Analytics Enthusiast",
            "📈 Operations Analyst", 
            "🎯 Affiliate Marketing Pro",
            "🐍 Python | 🗄️ SQL | 📊 Data Visualization",
            "📋 Turning Data into Insights 💡"
        ];
        
        let currentPhrase = 0;
        let currentChar = 0;
        let isDeleting = false;
        
        function typeAnimation() {
            const typingElement = document.getElementById('typingText');
            const currentText = phrases[currentPhrase];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, currentChar - 1);
                currentChar--;
            } else {
                typingElement.textContent = currentText.substring(0, currentChar + 1);
                currentChar++;
            }
            
            let typeSpeed = isDeleting ? 50 : 100;
            
            if (!isDeleting && currentChar === currentText.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && currentChar === 0) {
                isDeleting = false;
                currentPhrase = (currentPhrase + 1) % phrases.length;
                typeSpeed = 500;
            }
            
            setTimeout(typeAnimation, typeSpeed);
        }
        
        // Start typing animation
        typeAnimation();
        
        // Scroll animations
        function handleScrollAnimations() {
            const elements = document.querySelectorAll('.fade-in');
            const windowHeight = window.innerHeight;
            
            elements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                
                if (elementTop < windowHeight - 100) {
                    element.classList.add('visible');
                }
            });
        }
        
        // Initialize animations
        window.addEventListener('scroll', handleScrollAnimations);
        window.addEventListener('load', handleScrollAnimations);
        
        // Add hover effects to tech items
        document.querySelectorAll('.tech-item').forEach(item => {
            item.addEventListener('mouseover', function() {
                this.style.transform = 'translateY(-5px) scale(1.05)';
            });
            
            item.addEventListener('mouseout', function() {
                this.style.transform = 'translateY(-3px) scale(1)';
            });
        });
    </script>
</body>
</html>
