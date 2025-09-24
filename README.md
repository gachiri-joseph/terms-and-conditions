# terms-and-conditions
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>

    <title>Joseph Kaigai - Portfolio</title>
    <style>
        /* Base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: background-color 0.3s, color 0.3s, border-color 0.3s;
        }

        body {
            min-height: 100vh;
            padding: 20px;
            font-family: 'Courier New', monospace;
        }

        .page-container {
            width: 100%;
            max-width: 1400px;
            margin: 0 auto;
            min-height: 100vh;
            padding: 0 20px;
        }

        /* Light Theme */
        body.light {
            background: #ffffff;
            color: #000000;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
        }

        .light .page-container {
            background: #ffffff;
        }

        /* Dark Theme */
        body.dark {
            background: #000000;
            color: #ffffff;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
        }

        .dark .page-container {
            background: #000000;
        }

        /* Header Styles */
        .site-header {
            padding: 0 0 15px 0;
            margin-bottom: 15px;
            position: relative;
        }

        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
            width: 100%;
            position: relative;
            padding: 0;
        }  /* Logo Section */
        .logo-section {
            width: 200px;
            padding: 12px 16px;
            font-size: 11px;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-image {
            height: 55px;
            width: auto;
        }

        .light .logo-section {
            background: #ffffff;
            color: #000000;
            border-bottom: 1px solid #000000;
            box-shadow: none;
        }

        .dark .logo-section {
            background: #000000;
            color: #ffffff;
            border-bottom: 1px solid #ffffff;
            box-shadow: none;
        }

        .logo-title {
            font-size: 14px;
            font-weight: bold;
            margin: 0;
        }  .cli .logo-title {
            color: #00FF00;
        }

        .light .logo-title {
            color: #000000;
        }

        .dark .logo-title {
            color: #ffffff;
        }

        .logo-subtitle {
            font-size: 10px;
            margin: 0;
        }

        .light .logo-subtitle {
            color: #333333;
        }

        .dark .logo-subtitle {
            color: #cccccc;
        }

        /* Header Banner */
        .header-banner {
            flex: 1;
            height: 70px;
            background-size: cover;
            margin: 0 10px;
        }

        .banner-image {
            width: 70%;
            height: 100%;
            object-fit: cover;
        }
  @media (max-width: 450px) {
            .banner-image {
                display: none;
            }
        }

        /* Theme Toggle Styles */
        .theme-toggle-container {
            z-index: 1000;
            display: flex;
            gap: 10px;
        }

        .theme-toggle {
            padding: 8px 12px;
            font-size: 12px;
            font-weight: bold;
            cursor: pointer;
            border: none;
            margin-left: 5px;
            transition: all 0.2s ease;
        }

        .light .theme-toggle {
            background: #ffffff;
            color: #000000;
            border-bottom: 1px solid #000000;
        }

        .light .theme-toggle.active {
            background: #000000;
            color: #ffffff;
        }

        .dark .theme-toggle {
            background: #000000;
            color: #ffffff;
            border-bottom: 1px solid #ffffff;
        }

        .dark .theme-toggle.active {
            background: #ffffff;
            color: #000000;
        }
   /* Main Content Layout */
        .main-content {
            display: flex;
            gap: 20px;
            margin: 30px auto;
            width: 100%;
            max-width: 1200px;
        }

        /* Left Sidebar */
        .left-sidebar {
            flex: 0 0 200px;
        }

        .sidebar-section {
            padding: 12px;
            margin-bottom: 15px;
        }

        .light .sidebar-section {
            background: #ffffff;
            border-top: 1px solid #000000;
            box-shadow: none;
        }

        .dark .sidebar-section {
            background: #000000;
            border-top: 1px solid #ffffff;
            box-shadow: none;
        }

        .sidebar-title {
            font-size: 11px;
            font-weight: bold;
            margin-bottom: 8px;
            text-transform: uppercase;
        }

        .sidebar-content {
            font-size: 10px;
            line-height: 1.4;
        }

        /* Sidebar Buttons */
        .sidebar-button {
            padding: 8px 12px;
            font-size: 10px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            margin: 8px 0;
            text-transform: uppercase;
            transition: all 0.2s ease;
            border: none;
        }

        .light .sidebar-button {
            background: #ffffff;
            border-bottom: 1px solid #000000;
            color: #000000;
        }

        .light .sidebar-button:hover {
            background: #000000;
            color: #ffffff;
        }

        .dark .sidebar-button {
            background: #000000;
            border-bottom: 1px solid #ffffff;
            color: #ffffff;
        }

        .dark .sidebar-button:hover {
            background: #ffffff;
            color: #000000;
        }

        /* Skill bars */
        .skill-bar {
            margin: 8px 0;
        }

        .skill-name {
            font-size: 10px;
            margin-bottom: 4px;
        }

        .skill-progress {
            width: 100%;
            height: 10px;
            overflow: hidden;
        }

        .light .skill-progress {
            background: #ffffff;
            border-bottom: 1px solid #000000;
        }

        .dark .skill-progress {
            background: #000000;
            border-bottom: 1px solid #ffffff;
        }

        .skill-fill {
            height: 100%;
        }

        .light .skill-fill {
            background: #000000;
        }

        .dark .skill-fill {
            background: #ffffff;
        }

        /* Middle Section */
        .middle-section {
            flex: 1 0 500px;
        }
    /* Tab Container */
        .tab-wrapper {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0 15px;
            gap: 10px;
        }

        .hamburger {
            display: none;
            font-size: 24px;
            cursor: pointer;
            padding: 10px;
            z-index: 10;
            background-color: transparent;
            border: none;
        }

        .tab-container {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 0;
        }

        .light .tab-container {
            background: #ffffff;
            border-bottom: 1px solid #000000;
        }

        .dark .tab-container {
            background: #000000;
            border-bottom: 1px solid #ffffff;
        }

        /* Tabs */
        .tab {
            padding: 10px 20px;
            font-weight: bold;
            font-size: 11px;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            position: relative;
            text-align: center;
            border: none;
            transition: background-color 0.2s ease;
        }

        .light .tab {
            background: #ffffff;
            border-bottom: 1px solid #000000;
            color: #000000;
        }

        .light .tab:hover {
            background: #f0f0f0;
        }

        .light .tab.active {
            background: #ffffff;
            color: #000000;
            border-bottom: 2px solid #000000;
            z-index: 2;
        }

        .dark .tab {
            background: #000000;
            border-bottom: 1px solid #ffffff;
            color: #ffffff;
        }

        .dark .tab:hover {
            background: #333333;
        }

        .dark .tab.active {
            background: #000000;
            color: #ffffff;
            border-bottom: 2px solid #ffffff;
            z-index: 2;
        }

        /* Tab Content */
        .tab-content {
            padding: 20px;
            font-size: 12px;
            line-height: 1.5;
            min-height: 400px;
        }

        .light .tab-content {
            background: #ffffff;
            border-top: 1px solid #000000;
            color: #000000;
            box-shadow: none;
        }

        .dark .tab-content {
            background: #000000;
            border-top: 1px solid #ffffff;
            color: #ffffff;
            box-shadow: none;
        }

        .tab-content.hidden {
            display: none;
        }

        /* Feature Boxes */
        .feature-box {
            padding: 20px;
            margin: 20px 0;
        }

        .light .feature-box {
            background: #ffffff;
            border-top: 1px solid #000000;
            box-shadow: none;
        }

        .dark .feature-box {
            background: #000000;
            border-top: 1px solid #ffffff;
            box-shadow: none;
        }

        .feature-box h3 {
            font-size: 13px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .feature-box p {
            font-size: 11px;
            line-height: 1.4;
            margin-bottom: 8px;
        }

        /* Links */
        .links {
            cursor: pointer;
            padding: 2px 4px;
            text-decoration: none;
            transition: color 0.2s ease;
        }

        .light .links {
            color: #000000;
            font-weight: bold;
        }

        .dark .links {
            color: #ffffff;
            font-weight: bold;
        }
        </style>
        </head>
        

<body class="dark">
    <div class="page-container">
        <!-- Header -->
        <div class="site-header">
            <div class="header-content">
                <div class="logo-section">
                    <img src="https://images.unsplash.com/photo-1535189043414-47a3c49a0bed?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGtvcmVhfGVufDB8fDB8fHww"
                        alt="Logo" class="logo-image">
                    <div>
                        <div class="logo-title">JOSEPH KAIGAI</div>
                        <div class="logo-subtitle">Portfolio 2025</div>
                    </div>
                </div>

                <div class="header-banner">
                    <img src="https://images.unsplash.com/photo-1535189043414-47a3c49a0bed?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGtvcmVhfGVufDB8fDB8fHww"
                        alt="Banner" class="banner-image">
                </div>

                <div class="theme-toggle-container">
                    <button class="theme-toggle" id="lightTheme" title="Light Mode">☀️</button>
                    <button class="theme-toggle active" id="darkTheme" title="Dark Mode">🌙</button>
                    <button class="theme-toggle" id="cliTheme" title="Terminal Mode">💻</button>
                </div>
            </div>
        </div>

        <div class="main-content">
            <!-- Left Sidebar -->
            <div class="left-sidebar">
                <div class="sidebar-section">
                    <div class="sidebar-title">Quick Stats:</div>
                    <div class="sidebar-content">
                        <strong>2+</strong> Years Experience<br>
                        <strong>5+</strong> Projects Completed<br>
                        <strong>10+</strong> Systems Integrated<br>
                        <button class="sidebar-button" onclick="switchTab('contact')">Get In Touch!</button>
                    </div>
                </div>

                <div class="sidebar-section">
                    <div class="sidebar-title">Technical Skills:</div>
                    <div class="sidebar-content">
                        <div class="skill-bar">
                            <div class="skill-name">Java (Spring Boot)</div>
                            <div class="skill-progress">
                                <div class="skill-fill" style="width: 85%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-name">JS/React/React Native</div>
                            <div class="skill-progress">
                                <div class="skill-fill" style="width: 80%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-name">Relational && non-relational Databases</div>
                            <div class="skill-progress">
                                <div class="skill-fill" style="width: 75%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-name">Cloud computing</div>
                            <div class="skill-progress">
                                <div class="skill-fill" style="width: 75%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="sidebar-section">
                    <button class="sidebar-button" onclick="handleDownloadResume()">Download Resume</button>
                </div>

                <div class="sidebar-section">
                    <div class="sidebar-title">CURRENT STATUS</div>
                    <div class="sidebar-content">
                        Currently employed at Jubilee Insurance as a Junior Integration Officer.
                        <br><br>
                        <button class="sidebar-button" onclick="switchTab('about')">
                            View My Experience
                        </button>
                        <br>
                        <strong>Areas of Expertise:</strong>
                        <br>• Backend Development (Java Spring Boot)
                        <br>• System Integration
                        <br>• API Development
                        <br>• Technical Support
                        <br><br>
                        Available for interesting side projects and collaborations.
                    </div>
                </div>
            </div>

            <!-- Middle Section -->
            <div class="middle-section">
                <div class="tab-wrapper">
                    <button class="hamburger" onclick="toggleMobileMenu()">☰</button>
                    <div class="tab-container" id="tabContainer">
                        <button class="tab active" onclick="switchTab('home')">HOME</button>
                        <button class="tab" onclick="switchTab('about')">ABOUT</button>
                        <button class="tab" onclick="switchTab('projects')">PROJECTS</button>
                        <button class="tab" onclick="switchTab('contact')">CONTACT</button>
                    </div>
                </div>

                <!-- Home Tab -->
                <div class="tab-content" id="homeTab">
                    <div class="hero-section">
                        <h1 class="hero-title">Joseph Kaigai</h1>
                        <h2 class="hero-subtitle">Software Developer</h2>
                        <p class="hero-description">
                            IT professional with 2+ years of experience specializing in Java Spring Boot backend
                            development
                            and React/React Native frontend. Passionate about building efficient systems and solving
                            complex
                            integration challenges.
                        </p>
                    </div>
                    <div class="feature-box">
                        <h3>Core Competencies</h3>
                        <p><strong>Backend Development:</strong> Building robust APIs with Java Spring Boot,
                            microservices architecture</p>
                        <p><strong>Frontend Development:</strong> Creating responsive UIs with React and React Native
                        </p>
                        <p><strong>System Integration:</strong> Connecting disparate systems for seamless data flow</p>
                        <p><strong>Problem Solving:</strong> Troubleshooting complex technical issues</p>
                    </div>
                    <div class="feature-box">
                        <h3>Current Focus</h3>
                        <p>Enhancing my skills in:</p>
                        <p>• Advanced Spring Boot features and best practices</p>
                        <p>• React Native mobile development</p>
                        <p>• Cloud-native application development</p>
                        <p>• API security and performance optimization</p>
                    </div>
                    <div class="feature-box">
                        <h3>Looking For Opportunities</h3>
                        <p>Available for interesting side projects and collaborations.</p>
                    </div>
                </div>

                <!-- About Tab -->
                <div class="tab-content hidden" id="aboutTab">
                    <h2>Professional Profile</h2>

                    <div class="feature-box">
                        <h3>About Me</h3>
                        <p>
                            Motivated and adaptable IT professional with hands-on experience in tech support and a
                            growing skill set in backend development and system integration.
                            Skilled in supporting system operations, resolving technical issues, and contributing to the
                            development of backend systems using Java (Spring Boot).
                        </p>
                        <p>
                            A reliable team player with a solid understanding of microservices and integration
                            workflows. Eager to continue learning and apply technical knowledge to solve real-world
                            business challenges.
                        </p>
                    </div>

                    <div class="feature-box">
                        <h3>Technical Expertise</h3>
                        <p><strong>Programming & Frameworks:</strong> Java (Spring Boot), JavaScript (React, React
                            Native, Node.js)</p>
                        <p><strong>APIs & Security:</strong> RESTful & SOAP APIs, OAuth2, JWT</p>
                        <p><strong>Databases:</strong> MySQL, PostgreSQL, MongoDB</p>
                        <p><strong>Messaging & Caching:</strong> Kafka, Redis</p>
                        <p><strong>DevOps & Cloud:</strong> Docker, AWS</p>
                        <p><strong>Architecture:</strong> API Management, Microservices</p>
                        <p><strong>Testing & Monitoring:</strong> Unit Testing (JUnit)</p>
                    </div>

                    <div class="feature-box">
                        <h3>Work Experience</h3>

                        <div class="experience-item">
                            <h4>Junior Integration Officer | Jubilee Insurance | Nov 2024–Present</h4>
                        </div>

                        <div class="experience-item">
                            <h4>Technical Support | Jubilee Insurance | May 2024–Nov 2024</h4>
                        </div>
                    </div>
                </div>

                <!-- Projects Tab -->
                <div class="tab-content hidden" id="projectsTab">
                    <h2>My Projects</h2>
                    <p>
                        Here are some of the projects I've worked on that demonstrate my technical capabilities:
                    </p>

                    <div class="project-grid">
                        <div class="project-card">
                            <div class="project-image">
                                <img src="https://images.unsplash.com/photo-1535189043414-47a3c49a0bed?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGtvcmVhfGVufDB8fDB8fHww"
                                    alt="E-Commerce Platform" style="width: 100%; height: 100%;">
                            </div>
                            <div class="project-info">
                                <h3 class="project-title">E-Commerce Platform</h3>
                                <p class="project-description">
                                    Currently developing a full-featured e-commerce platform with:
                                </p>
                                <ul style="padding: 10px;">
                                    <li>Product catalog and inventory management</li>
                                    <li>User authentication and authorization</li>
                                    <li>Payment gateway integration</li>
                                    <li>Order processing system</li>
                                </ul>
                                <div class="project-tech">
                                    <span class="tech-tag">React</span>
                                    <span class="tech-tag">Spring Boot</span>
                                    <span class="tech-tag">MySQL</span>
                                    <span class="tech-tag">AWS</span>
                                </div>
                                <div class="project-links">
                                    <div class="popup-wrapper">
                                        <button class="project-link" onclick="showPopup('demo')">View Demo</button>
                                        <div class="popup-themed" id="demoPopup">Not yet ready</div>
                                    </div>
                                    <div class="popup-wrapper">
                                        <button class="project-link" onclick="showPopup('code')">Code Samples</button>
                                        <div class="popup-themed" id="codePopup">Not yet ready</div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="project-card">
                            <div class="project-image">
                                <img src="https://images.unsplash.com/photo-1535189043414-47a3c49a0bed?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTJ8fGtvcmVhfGVufDB8fDB8fHww"
                                    alt="School Resource App" style="width: 100%; height: 100%;">
                            </div>
                            <div class="project-info">
                                <h3 class="project-title">School Resource App</h3>
                                <p class="project-description">
                                    Mobile application for educational resource sharing featuring:
                                </p>
                                <ul style="padding: 10px;">
                                    <li>Cross-platform development with React Native</li>
                                    <li>Document upload/download functionality</li>
                                    <li>User role-based access control</li>
                                    <li>Real-time notifications</li>
                                </ul>
                                <div class="project-tech">
                                    <span class="tech-tag">React Native</span>
                                    <span class="tech-tag">PostgreSQL</span>
                                    <span class="tech-tag">Supabase</span>
                                </div>
                                <div class="project-links">
                                    <div class="popup-wrapper">
                                        <button class="project-link" onclick="showPopup('demoSite')">App
                                            Preview</button>
                                        <div class="popup-themed" id="demoSitePopup">Not yet ready</div>
                                    </div>
                                    <div class="popup-wrapper">
                                        <button class="project-link" onclick="showPopup('codeSite')">Code
                                            Samples</button>
                                        <div class="popup-themed" id="codeSitePopup">Not yet ready</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="feature-box">
                        <h3>Other Technical Work</h3>
                        <p><strong>Open Source Contributions:</strong> Bug fixes and documentation for Spring Boot
                            projects</p>
                        <p><strong>Learning Projects:</strong> API gateway implementation, microservices POC</p>
                        <p><strong>Technical Writing:</strong> Documentation for internal APIs and integration workflows
                        </p>
                    </div>
                </div>

                <!-- Contact Tab -->
                <div class="tab-content hidden" id="contactTab">
                    <h2>Get In Touch</h2>
                    <p>
                        I'm always interested in new opportunities, collaborations, or just a friendly chat about
                        technology.
                        Feel free to reach out using the form below or through any of my social channels.
                    </p>
                    <form class="contact-form" id="contactForm">
                        <h2>Send me a message. Let's have a chat!</h2>
                        <div class="form-group">
                            <label for="from_name" class="form-label">Name</label>
                            <input type="text" id="from_name" name="from_name" placeholder="Your name.." required
                                class="form-input">
                        </div>

                        <div class="form-group">
                            <label for="from_email" class="form-label">E-mail</label>
                            <input type="email" id="from_email" name="from_email" placeholder="Your email.." required
                                class="form-input">
                        </div>

                        <div class="form-group">
                            <label for="message" class="form-label">Message</label>
                            <textarea name="message" rows="8" cols="30" placeholder="Your message.." required
                                class="form-textarea"></textarea>
                        </div>

                        <input type="submit" class="submit-button" value="Send">
                        <div id="formMessage"></div>
                    </form>

                    <div class="feature-box">
                        <h3>Other Ways to Connect</h3>
                        <p><strong>Phone:</strong> +254********</p>
                        <p><strong>Email:</strong> <a href=""
                                class="links">joseph.gachiri1@gmail.com</a></p>
                        <p><strong>LinkedIn:</strong> <a href=""
                                target="_blank" class="links">my linkedIn</a></p>
                        <p><strong>Location:</strong> Nairobi, Kenya (Open to remote work)</p>
                    </div>

                    <div class="feature-box">
                        <h3>Response Time</h3>
                        <p>I typically respond to emails within 24 hours during business days. For urgent inquiries,
                            feel free to call or send a message on LinkedIn.</p>
                        <p><strong>Availability:</strong> Available for interesting side projects and collaborations.
                        </p>
                    </div>
                </div>
            </div>

            <!-- Right Sidebar -->
            <div class="right-sidebar">
                <div class="sidebar-section">
                    <div class="sidebar-title">CERTIFICATIONS</div>
                    <div class="sidebar-content">
                        <!-- <strong>Spring Boot Fundamentals</strong> - Udemy (2024)
                        <br><br> -->
                        <strong>AWS Cloud Practitioner</strong> - In Progress
                        <br><br>
                        <strong>Oracle OCI</strong> - In Progress
                    </div>
                </div>

                <div class="sidebar-section">
                    <div class="sidebar-title">CURRENTLY LEARNING</div>
                    <div class="sidebar-content">
                        <ul style="padding-left: 10px;">
                            <li>Advanced AWS Services</li>
                            <li>Kubernetes Orchestration</li>
                            <li>Microservices Patterns</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer class="footer">
            <div class="footer-content">
                <p>&copy; 2025 Joseph Kaigai. All rights reserved.</p>
                <div class="footer-divider"></div>
                <p>
                    Designed with 😎 and inspired by
                    <a href="https://www.habbo.com/" target="_blank" rel="noopener noreferrer">@Habbo Hotel</a>
                </p>
            </div>
        </footer>
    </div>

    <!-- Popup Message -->
    <div class="popup-message" id="popupMessage"></div>

    <script>
        // Theme management
        let currentTheme = localStorage.getItem('theme') || 'dark';

        function setTheme(theme) {
            currentTheme = theme;
            document.body.className = theme;
            localStorage.setItem('theme', theme);

            // Update theme toggle buttons
            document.querySelectorAll('.theme-toggle').forEach(btn => {
                btn.classList.remove('active');
            });

            if (theme === 'light') {
                document.getElementById('lightTheme').classList.add('active');
            } else if (theme === 'dark') {
                document.getElementById('darkTheme').classList.add('active');
            } else if (theme === 'cli') {
                document.getElementById('cliTheme').classList.add('active');
            }
        }

        // Initialize theme
        setTheme(currentTheme);

        // Theme toggle event listeners
        document.getElementById('lightTheme').addEventListener('click', () => setTheme('light'));
        document.getElementById('darkTheme').addEventListener('click', () => setTheme('dark'));
        document.getElementById('cliTheme').addEventListener('click', () => setTheme('cli'));

        // Tab management
        let activeTab = 'home';

        function switchTab(tabId) {
            // Hide all tab contents
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.add('hidden');
            });

            // Remove active class from all tabs
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
            });

            // Show selected tab content
            document.getElementById(tabId + 'Tab').classList.remove('hidden');

            // Add active class to selected tab
            event.target.classList.add('active');

            activeTab = tabId;

            // Close mobile menu
            document.getElementById('tabContainer').classList.remove('show');
        }

        // Mobile menu toggle
        function toggleMobileMenu() {
            const tabContainer = document.getElementById('tabContainer');
            tabContainer.classList.toggle('show');
        }

        // Project popup management
        function showPopup(key) {
            const popupElement = document.getElementById(key + 'Popup');
            if (popupElement) {
                popupElement.classList.add('show');
                setTimeout(() => {
                    popupElement.classList.remove('show');
                }, 2000);
            }
        }

        // Resume download handler
        function handleDownloadResume() {
            const popup = document.getElementById('popupMessage');
            popup.textContent = 'Kindly contact me for my resume';
            popup.classList.add('show');

            // Switch to contact tab
            switchTab('contact');

            setTimeout(() => {
                popup.classList.remove('show');
            }, 3000);
        }

        // Contact form handler
        // Initialize EmailJS with the public key
        (function () {
            emailjs.init("");
        })();

        // Contact form handler
        document.getElementById('contactForm').addEventListener('submit', function (e) {
            e.preventDefault();

            const messageDiv = document.getElementById('formMessage');
            const submitButton = document.querySelector('.submit-button');

            // Show loading state
            submitButton.value = 'Sending...';
            submitButton.disabled = true;
            messageDiv.innerHTML = '<p class="message">Sending your message...</p>';

            // Send email using EmailJS
            emailjs.sendForm('', '', this)
                .then(function (response) {
                    console.log('SUCCESS!', response.status, response.text);
                    messageDiv.innerHTML = '<p class="message success">Thank you for your message! I\'ll get back to you soon.</p>';

                    // Reset form
                    document.getElementById('contactForm').reset();

                    // Clear message after 5 seconds
                    setTimeout(() => {
                        messageDiv.innerHTML = '';
                    }, 5000);

                }, function (error) {
                    console.log('FAILED...', error);
                    messageDiv.innerHTML = '<p class="message error">Sorry, there was an error sending your message. Please try again or contact me directly.</p>';
                })
                .finally(function () {
                    // Reset button state
                    submitButton.value = 'Send';
                    submitButton.disabled = false;
                });
        });
        // Initialize tab clicks for dynamically generated tabs
        document.addEventListener('DOMContentLoaded', function () {
            document.querySelectorAll('.tab').forEach((tab, index) => {
                const tabs = ['home', 'about', 'projects', 'contact'];
                tab.addEventListener('click', function () {
                    switchTab(tabs[index]);
                });
            });
        });
    </script>
</body>
</html>
</html>
