<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Venkata Naveen Kumar Yelem | Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2c3e50;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--secondary);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
        }
        
        .logo span {
            color: var(--primary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .menu-toggle {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), url('https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .profile-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            overflow: hidden;
            margin: 0 auto 20px;
            border: 3px solid var(--primary);
        }
        
        .profile-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero h2 {
            font-size: 24px;
            font-weight: 300;
            margin-bottom: 30px;
            color: var(--light);
        }
        
        .hero p {
            font-size: 18px;
            margin-bottom: 40px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            margin: 10px;
        }
        
        .btn:hover {
            background-color: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--secondary);
        }
        
        /* About Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 36px;
            color: var(--secondary);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-img {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .skills {
            margin-top: 30px;
        }
        
        .skill-item {
            margin-bottom: 20px;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .skill-bar {
            height: 10px;
            background-color: #ddd;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .skill-progress {
            height: 100%;
            background-color: var(--primary);
            border-radius: 5px;
        }
        
        /* Education Section */
        .education {
            background-color: #f5f7fa;
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 0;
        }
        
        .timeline::after {
            content: '';
            position: absolute;
            width: 3px;
            background-color: var(--primary);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1.5px;
        }
        
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: white;
            border: 3px solid var(--primary);
            border-radius: 50%;
            top: 15px;
            z-index: 1;
        }
        
        .left {
            left: 0;
        }
        
        .right {
            left: 50%;
        }
        
        .left::after {
            right: -10px;
        }
        
        .right::after {
            left: -10px;
        }
        
        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .timeline-content h3 {
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .timeline-content p {
            color: var(--gray);
        }
        
        .timeline-date {
            font-weight: 600;
            color: var(--primary);
        }
        
        /* Experience Section */
        .experience-item {
            display: flex;
            margin-bottom: 40px;
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .experience-img {
            flex: 1;
            min-width: 300px;
            background-size: cover;
            background-position: center;
        }
        
        .experience-text {
            flex: 2;
            padding: 30px;
        }
        
        .experience-text h3 {
            font-size: 24px;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .experience-text h4 {
            font-size: 18px;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        .experience-text ul {
            list-style-position: inside;
            margin-bottom: 20px;
        }
        
        .experience-text li {
            margin-bottom: 10px;
        }
        
        /* Projects Section */
        .projects {
            background-color: #f5f7fa;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .project-content p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .project-links a {
            display: inline-block;
            margin-right: 10px;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
        }
        
        /* Certifications Section */
        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .certification-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .certification-card:hover {
            transform: translateY(-10px);
        }
        
        .certification-img {
            height: 250px;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            border-bottom: 1px solid #eee;
        }
        
        .certification-content {
            padding: 20px;
        }
        
        .certification-content h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .certification-content p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .certification-meta {
            display: flex;
            justify-content: space-between;
            color: var(--primary);
            font-weight: 500;
        }
        
        /* Masters Goals Section */
        .goals {
            text-align: center;
        }
        
        .goals-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .goals-content p {
            margin-bottom: 20px;
            font-size: 18px;
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--secondary);
            color: white;
        }
        
        .contact .section-title h2 {
            color: white;
        }
        
        .contact .section-title h2::after {
            background-color: white;
        }
        
        .contact-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .contact-info h3 {
            font-size: 24px;
            margin-bottom: 20px;
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 10px;
            color: var(--primary);
        }
        
        .contact-form {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
        }
        
        .form-group textarea {
            height: 150px;
        }
        
        .social-links {
            margin-top: 30px;
        }
        
        .social-links a {
            display: inline-block;
            margin-right: 15px;
            color: white;
            font-size: 20px;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--primary);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 20px 0;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: var(--secondary);
                flex-direction: column;
                align-items: center;
                padding-top: 40px;
                transition: left 0.3s;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item::after {
                left: 21px;
            }
            
            .left::after,
            .right::after {
                left: 21px;
            }
            
            .right {
                left: 0;
            }
            
            .experience-item {
                flex-direction: column;
            }
            
            .experience-img {
                height: 200px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero h2 {
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Naveen<span>Yelem</span></div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#education">Education</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#certifications">Certifications</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="profile-photo">
                    <img src="images/nani-pass-photo.jpg" alt="Naveen Yelem">
                </div>
                <h1>Venkata Naveen Kumar Yelem</h1>
                <h2>Mechanical Engineer | Data Analyst | Innovator</h2>
                <p>Recent graduate with a Bachelor's degree in Mechanical Engineering, passionate about leveraging engineering principles to create innovative solutions and pursuing advanced studies in mechanical systems and data analysis.</p>
                <a href="#contact" class="btn">Contact Me</a>
                <a href="#projects" class="btn btn-outline">View Projects</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1581094794329-c8112a89af12?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="About Me">
                </div>
                <div class="about-text">
                    <h3>Professional Summary</h3>
                    <p>I am a Mechanical Engineering graduate with expertise in design, manufacturing, and mechanical systems. With strong analytical and problem-solving skills, I have successfully completed projects in robotics and automation. My academic excellence is demonstrated by competitive scores in GRE (Verbal: 161, Quant: 169) and TOEFL (91).</p>
                    
                    <div class="skills">
                        <h3>Skills</h3>
                        <div class="skill-item">
                            <div class="skill-name">
                                <span>AutoCAD</span>
                                <span>90%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 90%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-name">
                                <span>CATIA</span>
                                <span>85%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 85%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-name">
                                <span>Python</span>
                                <span>80%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 80%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-name">
                                <span>Ansys</span>
                                <span>75%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 75%;"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section class="section education" id="education">
        <div class="container">
            <div class="section-title">
                <h2>Education</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>Bachelor of Technology in Mechanical Engineering</h3>
                        <p class="timeline-date">Oct 2021 - May 2024</p>
                        <p>Bonam Venkata Chalamaiah Engineering College, JNTU Kakinada</p>
                        <p>Final Grade: 7.66 CGPA</p>
                    </div>
                </div>
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <h3>Diploma in Mechanical Engineering</h3>
                        <p class="timeline-date">Jul 2017 - Mar 2020</p>
                        <p>DR. Samuel George Institute of Engineering And Technology</p>
                        <p>Final Grade: 73.46%</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section class="section" id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Work Experience</h2>
            </div>
            <div class="experience-item">
                <div class="experience-img" style="background-image: url('https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                <div class="experience-text">
                    <h3>Data Analyst</h3>
                    <h4>Cognizant | Aug 2024 - Feb 2025</h4>
                    <ul>
                        <li>Working as a data analyst on the Atlass tool at Cognizant</li>
                        <li>Verifying designated country's speed restrictions and entering them accurately in the tool</li>
                    </ul>
                </div>
            </div>
            <div class="experience-item">
                <div class="experience-img" style="background-image: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                <div class="experience-text">
                    <h3>QA Inspector</h3>
                    <h4>Somic ZF | Nov 2019 - Apr 2020</h4>
                    <ul>
                        <li>Worked as an intern at Somic ZF company, which manufactures automobile parts</li>
                        <li>Responsible for checking product quality after manufacture</li>
                        <li>Analyzed quality data to identify trends and root causes of defects</li>
                        <li>Conducted product inspections and tests to verify conformance to specifications</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section projects" id="projects">
        <div class="container">
            <div class="section-title">
                <h2>Projects</h2>
            </div>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-img" style="background-image: url('https://images.unsplash.com/photo-1511988617509-a57c8a288659?ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80');"></div>
                    <div class="project-content">
                        <h3>Head Gesture Motion-Controlled Wheelchair</h3>
                        <p>Developed a cost-effective wheelchair controlled via head gestures, promoting accessibility for users with disabilities.</p>
                        <div class="project-links">
                            <a href="https://drive.google.com/file/d/1irXdvOortfpGvUPHNLohjSTDZrHgZk2/view?usp=sharing" target="_blank">View Project</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img" style="background-image: url('https://images.unsplash.com/photo-1581093450025-4d763231e367?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');"></div>
                    <div class="project-content">
                        <h3>Smart Ceiling Fan with Blade Control</h3>
                        <p>Designed and fabricated a ceiling fan with innovative blade inclination and swing control mechanisms.</p>
                        <div class="project-links">
                            <a href="https://drive.google.com/file/d/1TimB9L4gCZyJHDi2cYl3vgxLvMTkeoD6/view?usp=sharing" target="_blank">View Project</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img" style="background-image: url('https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80');"></div>
                    <div class="project-content">
                        <h3>Robotics & Automation Internship</h3>
                        <p>Completed international internship in mechatronics and ROS programming with FH Aachen University, Germany.</p>
                        <div class="project-links">
                            <a href="ARC INTERN REPORT NANI.pdf" download>View Report</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section class="section" id="certifications">
        <div class="container">
            <div class="section-title">
                <h2>Certifications</h2>
            </div>
            <div class="certifications-grid">
                <!-- TOEFL Certification -->
                <div class="certification-card">
                    <div class="certification-img" style="background-image: url('https://www.ets.org/s/toefl/images/toefl-logo.svg'); background-color: #f8f8f8;"></div>
                    <div class="certification-content">
                        <h3>TOEFL iBT</h3>
                        <p>English Proficiency Test with overall score of 91/120</p>
                        <div class="certification-meta">
                            <span>Test Date: Oct 15, 2024</span>
                            <span>Score: 91/120</span>
                        </div>
                        <a href="English Profiency.pdf" class="btn" download>View Certificate</a>
                    </div>
                </div>
                
                <!-- GRE Certification -->
                <div class="certification-card">
                    <div class="certification-img" style="background-image: url('https://www.ets.org/s/gre/images/gre-logo.svg'); background-color: #f8f8f8;"></div>
                    <div class="certification-content">
                        <h3>GRE General Test</h3>
                        <p>Graduate Record Examinations with excellent scores</p>
                        <div class="certification-meta">
                            <span>Test Date: Oct 29, 2024</span>
                            <span>Quant: 169 (87%)</span>
                        </div>
                        <a href="GRE Report.pdf" class="btn" download>View Certificate</a>
                    </div>
                </div>
                
                <!-- Java Full Stack Internship -->
                <div class="certification-card">
                    <div class="certification-img" style="background-image: url('https://www.kodnest.com/assets/images/logo.png'); background-color: #f8f8f8; background-size: contain;"></div>
                    <div class="certification-content">
                        <h3>Java Full Stack Internship</h3>
                        <p>Completed internship in web application development at KodNest</p>
                        <div class="certification-meta">
                            <span>Completed: Apr 19, 2024</span>
                            <span>KodNest</span>
                        </div>
                        <a href="Dream_Factory_2024-YELEM_VENKATA_NAVEEN_KUMAR.pdf" class="btn" download>View Certificate</a>
                    </div>
                </div>
                
                <!-- International Internship -->
                <div class="certification-card">
                    <div class="certification-img" style="background-image: url('https://skillap.live/assets/images/logo.png'); background-color: #f8f8f8; background-size: contain;"></div>
                    <div class="certification-content">
                        <h3>International Internship</h3>
                        <p>Advanced certification on Emerging Technologies with FH Aachen University, Germany</p>
                        <div class="certification-meta">
                            <span>Aug 29 - Oct 21, 2022</span>
                            <span>APSSDC & IES</span>
                        </div>
                        <a href="International Internship.pdf" class="btn" download>View Certificate</a>
                    </div>
                </div>
                
                <!-- Robotics Internship -->
                <div class="certification-card">
                    <div class="certification-img" style="background-image: url('https://srivinayagacnc.com/wp-content/uploads/2021/04/cropped-logo-1.png'); background-color: #f8f8f8; background-size: contain;"></div>
                    <div class="certification-content">
                        <h3>Industrial Training</h3>
                        <p>Production and Quality Control training at Somic ZF Components</p>
                        <div class="certification-meta">
                            <span>Nov 2019 - May 2020</span>
                            <span>Sri Vinayaga CNC</span>
                        </div>
                        <a href="Internship certificate.pdf" class="btn" download>View Certificate</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Masters Goals Section -->
    <section class="section goals" id="goals">
        <div class="container">
            <div class="section-title">
                <h2>Master's Degree Goals</h2>
            </div>
            <div class="goals-content">
                <p>I am seeking to pursue a Master's degree in Mechanical Engineering or related fields to further develop my expertise in robotics, automation, and mechanical systems design. My academic background, technical skills, and project experience have prepared me to contribute meaningfully to advanced research in these areas.</p>
                <p>My specific interests include mechatronics, control systems, and assistive technologies. The head gesture-controlled wheelchair project demonstrated my ability to develop innovative solutions, and I aim to expand this skillset through graduate studies.</p>
                <p>With my strong GRE scores (Verbal: 161, Quant: 169) and TOEFL score of 91, I am well-prepared for the academic rigor of graduate studies. I look forward to collaborating with faculty and peers to push the boundaries of mechanical engineering innovation.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <p><i class="fas fa-map-marker-alt"></i> 1-36A, Porumamilla palli village, Chinna cumbum post, 523333 cumbum, India</p>
                    <p><i class="fas fa-phone"></i> (+91) 7032495520</p>
                    <p><i class="fas fa-envelope"></i> naniyelem@gmail.com</p>
                    <p><i class="fab fa-whatsapp"></i> 7032495520</p>
                    
                    <div class="social-links">
                        <a href="https://www.linkedin.com/in/naveenyelem" target="_blank"><i class="fab fa-linkedin"></i></a>
                        <a href="https://www.instagram.com/ns_stunt_rider_/" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Venkata Naveen Kumar Yelem. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
