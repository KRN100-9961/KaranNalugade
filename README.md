<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Karan Nalugade - Engineering Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@300;400;700;900&family=Open+Sans:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Merriweather', serif;
            line-height: 1.6;
            color: #2c3e50;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            color: #2c3e50;
            padding: 100px 0;
            margin-bottom: 60px;
            background: white;
            border-radius: 25px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #3498db, #2980b9, #1abc9c, #3498db);
            background-size: 300% 100%;
            animation: gradientFlow 3s ease infinite;
        }

        @keyframes gradientFlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        header h1 {
            font-family: 'Merriweather', serif;
            font-size: 4rem;
            margin-bottom: 20px;
            font-weight: 900;
            color: #2c3e50;
        }

        header p {
            font-size: 1.4rem;
            margin-bottom: 40px;
            color: #34495e;
            font-weight: 400;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .contact-item {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
            padding: 15px 25px;
            border-radius: 50px;
            transition: all 0.4s ease;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 8px 25px rgba(52, 152, 219, 0.3);
        }

        .contact-item:hover {
            transform: translateY(-5px);
            background: linear-gradient(135deg, #2980b9, #1abc9c);
            box-shadow: 0 15px 35px rgba(52, 152, 219, 0.4);
        }

        .contact-item .icon {
            margin-right: 8px;
            color: white;
        }

        .section {
            background: white;
            margin: 40px 0;
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.08);
            transition: all 0.4s ease;
            border-left: 5px solid #3498db;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 60px rgba(0,0,0,0.12);
            border-left: 5px solid #2980b9;
        }

        .section h2 {
            font-family: 'Merriweather', serif;
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #2c3e50;
            font-weight: 700;
            position: relative;
            padding-bottom: 15px;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #3498db, #2980b9);
            border-radius: 2px;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 35px;
            margin-top: 40px;
        }

        .project-card {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 35px;
            transition: all 0.4s ease;
            border: 2px solid #e9ecef;
            position: relative;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #3498db, #2980b9);
            border-radius: 15px 15px 0 0;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(52, 152, 219, 0.2);
            border-color: #3498db;
        }

        .project-title {
            font-family: 'Merriweather', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 15px;
            line-height: 1.3;
        }

        .project-meta {
            font-size: 1rem;
            color: #7f8c8d;
            margin-bottom: 20px;
            font-weight: 600;
            font-style: italic;
        }

        .project-description {
            margin-bottom: 25px;
            color: #34495e;
            font-size: 1rem;
            line-height: 1.7;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            padding: 8px 16px;
            border-radius: 25px;
            font-size: 0.85rem;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(52, 152, 219, 0.3);
            transition: all 0.3s ease;
        }

        .tech-tag:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(52, 152, 219, 0.4);
        }

        .achievement {
            background: linear-gradient(135deg, #e8f5e8, #d5eadb);
            border-left: 4px solid #27ae60;
            padding: 15px 20px;
            margin: 15px 0;
            border-radius: 8px;
            font-weight: 500;
            color: #2c3e50;
            transition: all 0.3s ease;
        }

        .achievement:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(39, 174, 96, 0.2);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 35px;
        }

        .skill-category {
            background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
            color: white;
            padding: 35px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 15px 35px rgba(52, 152, 219, 0.3);
            transition: all 0.4s ease;
        }

        .skill-category:hover {
            transform: translateY(-8px);
            box-shadow: 0 25px 50px rgba(52, 152, 219, 0.4);
        }

        .skill-category h3 {
            font-family: 'Merriweather', serif;
            margin-bottom: 25px;
            font-size: 1.5rem;
            font-weight: 700;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            margin: 12px 0;
            padding: 12px 20px;
            background: rgba(255,255,255,0.2);
            border-radius: 25px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .skill-list li:hover {
            background: rgba(255,255,255,0.3);
            transform: scale(1.05);
        }

        .education-item {
            background: linear-gradient(135deg, #ecf0f1 0%, #bdc3c7 100%);
            padding: 35px;
            border-radius: 15px;
            margin: 25px 0;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: all 0.4s ease;
            border-left: 5px solid #3498db;
        }

        .education-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .degree {
            font-family: 'Merriweather', serif;
            font-size: 1.4rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 12px;
        }

        .institution {
            font-size: 1.1rem;
            color: #34495e;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .gpa {
            font-size: 1rem;
            color: #3498db;
            font-weight: 600;
        }

        .cta-section {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            color: white;
            text-align: center;
            padding: 80px 50px;
            border-radius: 20px;
            margin-top: 60px;
            box-shadow: 0 25px 50px rgba(44, 62, 80, 0.3);
            position: relative;
        }

        .cta-section h2 {
            font-family: 'Merriweather', serif;
            font-size: 2.8rem;
            margin-bottom: 25px;
            font-weight: 700;
            color: white;
        }

        .cta-section h2::after {
            display: none;
        }

        .cta-section p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            opacity: 0.9;
            font-weight: 400;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
        }

        .cta-button {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            background: linear-gradient(45deg, #3498db, #2980b9);
            color: white;
            padding: 18px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: all 0.4s ease;
            box-shadow: 0 10px 30px rgba(52, 152, 219, 0.3);
            border: 2px solid transparent;
        }

        .cta-button:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 20px 40px rgba(52, 152, 219, 0.4);
            background: white;
            color: #2980b9;
            border-color: #3498db;
        }

        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .cert-item {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 25px;
            border-radius: 12px;
            border-left: 4px solid #3498db;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }

        .cert-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(52, 152, 219, 0.2);
            border-left: 4px solid #2980b9;
        }

        .cert-title {
            font-weight: 700;
            color: #2c3e50;
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .cert-provider {
            color: #7f8c8d;
            font-weight: 500;
        }

        .summary-box {
            background: white;
            padding: 40px;
            border-radius: 15px;
            margin-bottom: 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border-left: 5px solid #3498db;
        }

        .summary-box p {
            font-size: 1.2rem;
            line-height: 1.8;
            font-weight: 400;
            color: #2c3e50;
        }

        @media (max-width: 768px) {
            header h1 { font-size: 2.8rem; }
            header p { font-size: 1.2rem; }
            .section { padding: 30px 25px; }
            .project-grid { grid-template-columns: 1fr; }
            .skills-grid { grid-template-columns: 1fr; }
            .contact-info { flex-direction: column; align-items: center; }
            .cta-buttons { flex-direction: column; align-items: center; }
        }

        .icon {
            margin-right: 8px;
            color: #3498db;
        }

        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }

        .floating-circle {
            position: absolute;
            border-radius: 50%;
            background: rgba(52, 152, 219, 0.1);
            animation: floatMove 8s ease-in-out infinite;
        }

        .floating-circle:nth-child(1) {
            width: 60px;
            height: 60px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-circle:nth-child(2) {
            width: 80px;
            height: 80px;
            top: 50%;
            right: 15%;
            animation-delay: 3s;
        }

        .floating-circle:nth-child(3) {
            width: 40px;
            height: 40px;
            bottom: 30%;
            left: 20%;
            animation-delay: 6s;
        }

        @keyframes floatMove {
            0%, 100% { transform: translateY(0px) translateX(0px); }
            25% { transform: translateY(-15px) translateX(10px); }
            50% { transform: translateY(-30px) translateX(-5px); }
            75% { transform: translateY(-15px) translateX(-10px); }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="floating-elements">
                <div class="floating-circle"></div>
                <div class="floating-circle"></div>
                <div class="floating-circle"></div>
            </div>
            
            <h1>Karan Rajendra Nalugade</h1>
            <p>Mechanical Engineering Student | Design & Analysis</p>
            
            <div class="contact-info">
                <div class="contact-item" onclick="copyToClipboard('karannalugade5@gmail.com')">
                    <i class="fas fa-envelope icon"></i>karannalugade5@gmail.com
                </div>
                <div class="contact-item" onclick="copyToClipboard('+919607102487')">
                    <i class="fas fa-phone-alt icon"></i>+91 9607102487
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt icon"></i>Bibwewadi, Pune
                </div>
                <div class="contact-item" onclick="window.open('https://www.linkedin.com/in/karan-nalugade-2b516131b/', '_blank')">
                    <i class="fab fa-linkedin icon"></i>LinkedIn Profile
                </div>
            </div>
        </header>

        <section class="section">
            <h2><i class="fas fa-user icon"></i>Summary</h2>
            <div class="summary-box">
                <p>Third-year Mechanical Engineering student with hands-on experience in design analysis, CAD modeling, and manufacturing processes. Demonstrated ability to deliver industry-relevant projects combining traditional mechanical engineering with modern technology applications. Seeking opportunities to apply theoretical knowledge in real-world manufacturing environments and contribute to product development initiatives.</p>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-rocket icon"></i>Projects</h2>
            
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-title">Design and Analysis of Stacker Reclaimer Machine (Live Industry-Sponsored Project) </div>
                    <div class="project-meta">ISGEC Heavy Engineering Ltd. | July 2025-Present</div>
                    
                    <div class="project-description">
                        <p><strong>Objective:</strong> Design critical components for bulk material handling equipment used in steel and power industries.</p>
                        <p><strong>Approach:</strong> Interpreted manufacturing drawings with GD&T requirements, modeled components and assemblies, and performed comprehensive structural analysis for strength validation.</p>
                        <p><strong>Deliverables:</strong> Complete design documentation and analysis and reports.</p>
                    </div>
                    
                    <div class="tech-stack">
                        <span class="tech-tag">SolidWorks</span>
                        <span class="tech-tag">ANSYS Mechanical</span>
                        <span class="tech-tag">GD&T</span>
                        <span class="tech-tag">Technical Documentation</span>
                    </div>
                    
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Interpreted manufacturing drawings with GD&T and surface finish requirements
                    </div>
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Performed structural analysis in ANSYS for strength and stress validation
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">Defect Detection in Material Extrusion Methods Using Artificial Intelligence</div>
                    <div class="project-meta">Academic Project | Feb 2025-May 2025</div>
                    
                    <div class="project-description">
                        <p><strong>Objective:</strong> Develop automated quality control system for 3D printing processes to reduce material waste and improve print reliability.</p>
                        <p><strong>Approach:</strong> Created dual-model system for 3D printing with real-time defect detection and STL file analysis capabilities.</p>
                        <p><strong>Outcome:</strong> Enhanced print quality control through automated fault detection and parameter optimization recommendations.</p>
                    </div>
                    
                    <div class="tech-stack">
                        <span class="tech-tag">Machine Learning</span>
                        <span class="tech-tag">Computer Vision</span>
                        <span class="tech-tag">3D Printing</span>
                        <span class="tech-tag">Quality Control</span>
                    </div>
                    
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Developed a dual-model AI system for 3D printing defect detection
                    </div>
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Improved print reliability through AI-driven fault prediction
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-title">Design Of Differential Gearbox</div>
                    <div class="project-meta">Academic Project | April 2025</div>
                    
                    <div class="project-description">
                        <p><strong>Objective:</strong> Design complete differential gearbox system for automotive application with specific torque handling requirements.</p>
                        <p><strong>Approach:</strong> Comprehensive mechanical design including gear calculations, shaft dimensioning, and with industry validation.</p>
                        <p><strong>Validation:</strong> Design parameters compared and correlated with TATA ACE specifications for automotive industry compliance.</p>
                    </div>
                    
                    <div class="tech-stack">
                        <span class="tech-tag">Mechanical Design</span>
                        <span class="tech-tag">Gear Calculations</span>
                        <span class="tech-tag">SolidWorks</span>
                        <span class="tech-tag">Automotive Systems</span>
                    </div>
                    
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Designed gears and shafts considering torque input from engine transmission
                    </div>
                    <div class="achievement">
                        <i class="fas fa-check-circle" style="color: #27ae60; margin-right: 8px;"></i>
                        Compared results with TATA ACE specifications with close dimensional correlation
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-code icon"></i>Skills</h2>
            
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-cogs" style="margin-right: 10px;"></i>Technical</h3>
                    <ul class="skill-list">
                        <li>Machine Design</li>
                        <li>Manufacturing Processes</li>
                        <li>Additive Manufacturing</li>
                        <li>GD&T</li>
                        <li>DFMA</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-wrench" style="margin-right: 10px;"></i>Tools</h3>
                    <ul class="skill-list">
                        <li>SolidWorks</li>
                        <li>AutoCAD</li>
                        <li>ANSYS Mechanical</li>
                        <li>ANSYS Fluent</li>
                        <li>Superslicer</li>
                    </ul>
                </div>
                
                <div class="skill-category">
                    <h3><i class="fas fa-users" style="margin-right: 10px;"></i>Soft Skills</h3>
                    <ul class="skill-list">
                        <li>Leadership</li>
                        <li>Coordination</li>
                        <li>Effective Communication</li>
                        <li>Quick Learning</li>
                        <li>Time Management</li>
                        <li>Multitasking</li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-graduation-cap icon"></i>Education</h2>
            
            <div class="education-item">
                <div class="degree">Bachelor of Technology in Mechanical Engineering</div>
                <div class="institution">Vishwakarma Institute of Technology, Pune-411 037</div>
                <div class="gpa">CGPA: 8.75 | SGPA: 8.96 | Aug 2024 - Ongoing</div>
            </div>
            
            <div class="education-item">
                <div class="degree">Diploma in Mechanical Engineering</div>
                <div class="institution">Sanjay Ghodawat Polytechnic, Kolhapur, Maharashtra-416 118</div>
                <div class="gpa">July 2021 - May 2024</div>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-building icon"></i>Experience</h2>
            
            <div class="project-card">
                <div class="project-title">Vishwasrao Naik Sugar Factory Ltd.</div>
                <div class="project-meta">June 2023 - July 2023</div>
                
                <div class="project-description">
                    <p>Observed preventive and corrective maintenance procedures including motors and turbines. Gained exposure to industrial operations and maintenance protocols in sugar manufacturing environment.</p>
                    <p>Applied 5S techniques, improving tool accessibility and reducing equipment search time across maintenance operations.</p>
                </div>
                
                <div class="tech-stack">
                    <span class="tech-tag">5S Methodology</span>
                    <span class="tech-tag">Equipment Maintenance</span>
                    <span class="tech-tag">Industrial Operations</span>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-award icon"></i>Certifications</h2>
            <div class="cert-grid">
                <div class="cert-item">
                    <div class="cert-title">Design for Manufacturing Fundamentals</div>
                    <div class="cert-provider">Geomiq Academy</div>
                </div>
                <div class="cert-item">
                    <div class="cert-title">Geometric Dimensioning & Tolerancing Foundation</div>
                    <div class="cert-provider">CODIENTER</div>
                </div>
                <div class="cert-item">
                    <div class="cert-title">SOLIDWORKS Advanced Level Training</div>
                    <div class="cert-provider">Udemy</div>
                </div>
                <div class="cert-item">
                    <div class="cert-title">FEA & CFD with ANSYS Mechanical & ANSYS Fluent</div>
                    <div class="cert-provider">Udemy</div>
                </div>
                <div class="cert-item">
                    <div class="cert-title">AutoCAD</div>
                    <div class="cert-provider">Elewayte</div>
                </div>
                <div class="cert-item">
                    <div class="cert-title">Python Basics Course</div>
                    <div class="cert-provider">Udemy</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2><i class="fas fa-trophy icon"></i>Extracurricular</h2>
            <div class="achievement">
                <i class="fas fa-trophy" style="color: #f39c12; margin-right: 8px;"></i>
                Runner-Up : ISTE Sponsored Paper Presentation Competition
            </div>
            <div class="achievement">
                <i class="fas fa-user-friends" style="color: #9b59b6; margin-right: 8px;"></i>
                Core Team Member : Nimbus 2K23 (National Level Event)
            </div>
            <div class="achievement">
                <i class="fas fa-user-friends" style="color: #e74c3c; margin-right: 8px;"></i>
                Participant : State Level Technical Quiz Competition (Institute Representative)
            </div>
        </section>

        <div class="cta-section">
            <h2>Let's Connect</h2>
            
            <div class="cta-buttons">
                <a href="#" class="cta-button" onclick="showContactInfo('email', event)">
                    <i class="fas fa-envelope"></i>
                    Email Me
                </a>
                <a href="#" class="cta-button" onclick="showContactInfo('phone', event)">
                    <i class="fas fa-mobile-alt"></i>
                    Call Me
                </a>
                <a href="https://www.linkedin.com/in/karan-nalugade-2b516131b/" class="cta-button" target="_blank">
                    <i class="fab fa-linkedin"></i>
                    LinkedIn
                </a>
            </div>
        </div>
    </div>

    <script>
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                // Create temporary notification
                const notification = document.createElement('div');
                notification.textContent = 'Copied to clipboard!';
                notification.style.cssText = `
