# MY-portfolio
html code 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <!-- Importing Google Font (Poppins) -->
    <link rel="preconnect" href="https://googleapis.com">
    <link rel="preconnect" href="https://gstatic.com" crossorigin>
    <link href="https://googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- External CSS Link -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Header -->
    <header>
        <nav class="navbar">
            <h1>My Portfolio</h1>
            <div class="nav-links">
                <a href="#about">About</a>
                <a href="#skills">Skills</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Main Content Wrapper -->
    <main class="container">

        <!-- About Me Section -->
        <section id="about" class="portfolio-section text-center">
            <h2>About Me</h2>
            <div class="avatar-container">
                <!-- Placeholder SVG for the male professional avatar from the image -->
                <svg viewBox="0 0 100 100" class="avatar-img">
                    <circle cx="50" cy="50" r="50" fill="#E0F2FE"/>
                    <path d="M50,40 C58,40 62,32 62,24 C62,14 58,10 50,10 C42,10 38,14 38,24 C38,32 42,40 50,40 Z" fill="#2D3748"/>
                    <path d="M50,42 C54,42 55,47 55,52 L45,52 C45,47 46,42 50,42 Z" fill="#ED8936"/>
                    <path d="M25,85 C25,65 35,55 50,55 C65,55 75,65 75,85 Z" fill="#4A5568"/>
                    <path d="M42,55 L50,70 L58,55 L54,55 L50,62 L46,55 Z" fill="#FFF"/>
                    <path d="M48,60 L52,60 L50,75 Z" fill="#E53E3E"/>
                </svg>
            </div>
            <p class="about-text">Hello! My name is John Doe. I am learning web development and this is my first portfolio website.</p>
        </section>

        <hr class="section-divider">

        <!-- My Skills Section -->
        <section id="skills" class="portfolio-section text-center">
            <h2>My Skills</h2>
            <div class="table-container">
                <table class="skills-table">
                    <thead>
                        <tr>
                            <th>Skill</th>
                            <th>Level</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>HTML</td>
                            <td>Beginner</td>
                        </tr>
                        <tr>
                            <td>CSS</td>
                            <td>Beginner</td>
                        </tr>
                        <tr>
                            <td>JavaScript</td>
                            <td>Learning</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <hr class="section-divider">

        <!-- My Projects Section -->
        <section id="projects" class="portfolio-section text-center">
            <h2>My Projects</h2>
            <div class="projects-container">
                <div class="project-card">
                    <h3>Project 1</h3>
                    <p>A simple HTML & CSS webpage.</p>
                </div>
                <div class="project-card">
                    <h3>Project 2</h3>
                    <p>Another awesome mini project.</p>
                </div>
            </div>
        </section>

        <hr class="section-divider">

        <!-- Contact Me Section -->
        <section id="contact" class="portfolio-section text-center">
            <h2>Contact Me</h2>
            <form class="contact-form" action="#" method="POST" onsubmit="event.preventDefault();">
                <div class="form-group">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" placeholder="Enter your name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message:</label>
                    <textarea id="message" name="message" rows="4" placeholder="Write your message" required></textarea>
                </div>
                <button type="submit" class="btn-submit">Send</button>
            </form>
        </section>

    </main>

    <!-- Fixed Back to Top Button -->
    <a href="#" class="back-to-top">↑ Back to Top</a>

</body>
</html>


style css code 
/* ==========================================
   1. GLOBAL STYLES & VARIABLE DEFINITIONS
   ========================================== */
:root {
    --primary-color: #0056b3;     /* Main Dark Blue Theme Color */
    --secondary-color: #f4f7f9;   /* Soft Light Gray for Background */
    --text-color: #333333;        /* Dark Slate for text readability */
    --white: #ffffff;
    --border-color: #b0c4de;      /* Light steel blue for neat borders */
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
    background-color: var(--secondary-color);
    color: var(--text-color);
    line-height: 1.6;
}

.container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
}

.text-center {
    text-align: center;
}

/* ==========================================
   2. NAVIGATION BAR STYLING
   ========================================== */
header {
    background-color: var(--primary-color);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.navbar {
    max-width: 900px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 15px 20px;
}

.navbar h1 {
    color: var(--white);
    font-size: 1.8rem;
    margin-bottom: 10px;
}

.nav-links a {
    color: var(--white);
    text-decoration: none;
    padding: 8px 16px;
    font-weight: 400;
    transition: background-color 0.3s ease, border-radius 0.3s ease;
}

.nav-links a:hover {
    background-color: rgba(255, 255, 255, 0.2);
    border-radius: 4px;
}

/* ==========================================
   3. BOX MODEL & SECTION SPACING
   ========================================== */
.portfolio-section {
    padding: 50px 20px;
    margin: 20px 0;
}

.portfolio-section h2 {
    font-size: 2rem;
    color: var(--primary-color);
    margin-bottom: 30px;
    font-weight: 600;
}

/* Styled Section Divider (<hr>) */
.section-divider {
    border: 0;
    height: 1px;
    background: var(--border-color);
    margin: 10px auto;
    width: 95%;
}

/* ==========================================
   4. ABOUT ME SPECIFIC STYLING
   ========================================== */
.avatar-container {
    margin-bottom: 20px;
}

.avatar-img {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15); /* Soft shadows requested in guide */
}

.about-text {
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto;
    color: #555;
}

/* ==========================================
   5. SKILLS TABLE STYLING
   ========================================== */
.table-container {
    display: flex;
    justify-content: center;
}

.skills-table {
    width: 100%;
    max-width: 500px;
    border-collapse: collapse;
    background-color: var(--white);
    border: 2px solid var(--primary-color);
}

.skills-table th {
    background-color: var(--primary-color);
    color: var(--white);
    padding: 12px;
    font-weight: 600;
}

.skills-table td {
    padding: 12px;
    border: 1px solid var(--border-color);
}

/* Alternating Row Colors */
.skills-table tbody tr:nth-child(even) {
    background-color: #e6f0fa;
}

.skills-table tbody tr:nth-child(odd) {
    background-color: var(--white);
}

/* ==========================================
   6. PROJECTS CARDS STYLING
   ========================================== */
.projects-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    align-items: center;
}

.project-card {
    background-color: var(--white);
    width: 100%;
    max-width: 500px;
    padding: 25px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
}

.project-card h3 {
    margin-bottom: 10px;
    color: #111;
}

.project-card p {
    color: #666;
}

/* ==========================================
   7. CONTACT FORM & BUTTON STYLING
   ========================================== */
.contact-form {
    max-width: 500px;
    margin: 0 auto;
    background-color: var(--white);
    padding: 30px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    text-align: left;
}

.form-group {
    margin-bottom: 20px;
    display: flex;
    align-items: center;
}

.form-group label {
    width: 90px;
    font-weight: 600;
    color: #444;
}

.form-group input,
.form-group textarea {
    flex: 1;
    padding: 10px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    font-family: inherit;
    font-size: 0.95rem;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--primary-color);
}

/* Button Customization */
.btn-submit {
    display: block;
    width: 100%;
    background-color: var(--primary-color);
    color: var(--white);
    padding: 12px;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.btn-submit:hover {
    background-color: #004085;
}

/* ==========================================
   8. FIXED POSITION ELEMENTS
   ========================================== */
.back-to-top {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: var(--primary-color);
    color: var(--white);
    text-decoration: none;
    padding: 10px 15px;
    border-radius: 4px;
    font-size: 0.9rem;
    font-weight: 600;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: background-color 0.2s ease;
}

.back-to-top:hover {
    background-color: #004085;
}

