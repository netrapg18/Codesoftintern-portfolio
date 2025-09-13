<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>P.G NETRA | CSE Student & Developer</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

    <style>
        
        :root {
            --primary-color: #00aaff; /* A vibrant blue */
            --secondary-color: #0077b6; /* A darker blue for hover */
            --bg-color: #1a1a1a; /* Dark background */
            --surface-color: #2c2c2c; /* Slightly lighter for cards */
            --text-color: #f0f0f0; /* Off-white text */
            --heading-color: #ffffff;
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
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* --- Typography & Links --- */
        h1, h2, h3 {
            color: var(--heading-color);
            font-weight: 600;
        }

        h1 { font-size: 3rem; }
        h2 { font-size: 2.5rem; }
        h3 { font-size: 1.5rem; }

        a {
            color: var(--primary-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--secondary-color);
        }

        section {
            padding: 6rem 5%;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--primary-color);
            margin: 0.5rem auto 0;
            border-radius: 2px;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: #fff;
            padding: 12px 28px;
            border-radius: 5px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            border: 2px solid transparent;
        }

        .btn:hover {
            background-color: var(--secondary-color);
            color: #fff;
            transform: translateY(-3px);
        }

        
        header {
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            background-color: rgba(26, 26, 26, 0.8);
            backdrop-filter: blur(10px);
            padding: 1rem 5%;
            border-bottom: 1px solid var(--surface-color);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--heading-color);
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav ul li a {
            font-weight: 600;
        }

        
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1555066931-4365d1469c5b') no-repeat center center/cover;
        }

        .hero-text h1 {
            margin-bottom: 1rem;
        }

        .hero-text p {
            font-size: 1.8rem;
            font-weight: 300;
            margin-bottom: 2rem;
        }

        .highlight {
            color: var(--primary-color);
        }

       
        .about-container {
            display: flex;
            align-items: center;
            gap: 3rem;
        }

        .about-image img {
            width: 300px;
            height: 300px;
            object-fit: cover;
            border-radius: 50%;
            border: 5px solid var(--surface-color);
        }

        .about-bio {
            flex: 1;
        }

        .about-bio h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .about-bio p {
            margin-bottom: 1rem;
        }

      
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1.5rem;
            text-align: center;
        }

        .skill-card {
            background: var(--surface-color);
            padding: 2rem 1rem;
            border-radius: 10px;
            font-size: 1.2rem;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0, 170, 255, 0.2);
        }

        .skill-card i {
            font-size: 2.5rem;
            display: block;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

       
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--surface-color);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
        }

        .project-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            display: block;
        }

        .project-info {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .project-info h3 {
            margin-bottom: 0.5rem;
        }
        
        .project-info p {
            flex-grow: 1;
            margin-bottom: 1rem;
        }

        .project-links {
            margin-top: auto; /* Pushes links to the bottom */
            display: flex;
            gap: 1rem;
        }

        .project-links a {
            font-weight: 600;
            background-color: var(--bg-color);
            padding: 8px 16px;
            border-radius: 5px;
        }
        .project-links a:hover {
            background-color: var(--primary-color);
            color: white;
        }
        .project-links i {
            margin-right: 0.5rem;
        }


        
        #contact {
            text-align: center;
        }

        .contact-subtitle {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 2.5rem;
            flex-wrap: wrap;
        }

        .contact-link {
            font-size: 1.2rem;
        }
        .contact-link i {
            margin-right: 0.5rem;
        }

        
        footer {
            text-align: center;
            padding: 2rem 5%;
            background: var(--surface-color);
            margin-top: 2rem;
        }

       
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }

            nav ul {
                display: none; /* Simple hiding for mobile, can be replaced with a hamburger menu */
            }

            .about-container {
                flex-direction: column;
                text-align: center;
            }

            .about-image img {
                width: 200px;
                height: 200px;
            }
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <a href="#home" class="logo">Portfolio</a>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="hero-text">
                <h1>Hi, I'm <span class="highlight">P.G NETRA</span></h1>
                <p>I am a <span class="typing"></span></p>
                <a href="#projects" class="btn">View My Work</a>
            </div>
        </section>

        <section id="about">
            <h2 class="section-title">About Me</h2>
            <div class="about-container">
                <div class="about-image">
                    <img src="https://via.placeholder.com/300" alt="A photo of you">
                </div>
                <div class="about-bio">
                    <h3>Aspiring Software Developer</h3>
                    <p>
                        I am a passionate and driven Computer Science and Engineering student with a strong interest in building beautiful, functional websites and robust backend systems. 
                    </p>
                    <p>
                        My coursework in Java has provided me with a solid foundation in object-oriented programming, while my personal projects in web development have allowed me to bring my creative ideas to life. I thrive in collaborative environments and possess strong communication skills, enabling me to effectively articulate technical concepts and work within a team.
                    </p>
                </div>
            </div>
        </section>

        <section id="skills">
            <h2 class="section-title">My Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-card"><i class="fa-brands fa-java"></i> Java</div>
                <div class="skill-card"><i class="fa-brands fa-html5"></i> HTML</div>
                <div class="skill-card"><i class="fa-brands fa-css3-alt"></i> CSS</div>
                <div class="skill-card"><i class="fa-brands fa-js"></i> JavaScript</div>
                <div class="skill-card"><i class="fa-solid fa-database"></i> SQL</div>
                <div class="skill-card"><i class="fa-brands fa-git-alt"></i> GitHub</div>
                <div class="skill-card"><i class="fa-solid fa-laptop-code"></i> Data Structures</div>
                <div class="skill-card"><i class="fa-solid fa-users"></i> Teamwork</div>
                <div class="skill-card"><i class="fa-solid fa-comments"></i> Communication</div>
            </div>
        </section>

        <section id="projects">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <img src="https://via.placeholder.com/400x220/2c2c2c/ffffff?text=Project+1" alt="Project 1 Screenshot">
                    <div class="project-info">
                        <h3>Hostel Complaint Management System</h3>
                        <p>A digital platform that automates and streamlines the process of submitting, tracking, and resolving student issues. Built using HTML, CSS, and JavaScript.</p>
                        <div class="project-links">
                            <a href="https://github.com/netrapg18/Hostel-complaint-management-system-" target="_blank"><i class="fa-brands fa-github"></i> Code</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <img src="https://via.placeholder.com/400x220/2c2c2c/ffffff?text=Project+2" alt="Project 2 Screenshot">
                    <div class="project-info">
                        <h3>Text to Speech Converter</h3>
                        <p>A fully responsive text-to-speech converter using HTML, CSS, and JavaScript that allows users to input text and hear it read aloud.</p>
                        <div class="project-links">
                            <a href="https://github.com/netrapg18/Text-to-speak" target="_blank"><i class="fa-brands fa-github"></i> Code</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <img src="https://via.placeholder.com/400x220/2c2c2c/ffffff?text=Project+3" alt="Project 3 Screenshot">
                    <div class="project-info">
                        <h3>Student Feedback Form</h3>
                        <p>A structured student feedback form built with HTML for structure, CSS for modern styling, and JavaScript for client-side validation logic.</p>
                        <div class="project-links">
                             <a href="https://github.com/netrapg18/Student-feed-back-form-" target="_blank"><i class="fa-brands fa-github"></i> Code</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <img src="https://via.placeholder.com/400x220/2c2c2c/ffffff?text=Project+4" alt="Netflix Clone Screenshot">
                    <div class="project-info">
                        <h3>Netflix Frontend Clone</h3>
                        <p>A responsive Netflix clone built using HTML, CSS, and JavaScript. It replicates the Netflix homepage UI with dynamic sections and modern styling.</p>
                        <div class="project-links">
                            <a href="https://github.com/netrapg18/Netflix-front-end-clone-" target="_blank">
                                <i class="fa-brands fa-github"></i> Code
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact">
            <h2 class="section-title">Get In Touch</h2>
            <p class="contact-subtitle">I'm currently seeking internship opportunities. My inbox is always open!</p>
            <div class="contact-info">
                <a href="mailto:netrageethamani2006@gmail.com" class="contact-link"><i class="fa-solid fa-envelope"></i> netrageethamani2006@gmail.com</a>
                <a href="https://linkedin.com/in/yourprofile" target="_blank" class="contact-link"><i class="fa-brands fa-linkedin"></i> LinkedIn Profile</a>
            </div>
            <a href="resume.pdf" download class="btn">Download My Resume</a>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 P.G NETRA. All Rights Reserved.</p>
    </footer>

    <script src="https://unpkg.com/typed.js@2.1.0/dist/typed.umd.js"></script>
    <script>
        var typed = new Typed('.typing', {
            strings: ["CSE Student.", "Web Developer.", "Java Enthusiast."],
            typeSpeed: 70,
            backSpeed: 60,
            loop: true
        });
    </script>

</body>
</html>
