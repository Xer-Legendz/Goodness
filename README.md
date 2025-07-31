# Goodness
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <style>
        * {
            margin: 0; padding: 0; box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        body { color: #333; line-height: 1.6; }
        header {
            background: #222; position: fixed; width: 100%; top: 0; z-index: 100;
        }
        .navbar {
            display: flex; justify-content: space-between; align-items: center;
            padding: 1rem 2rem; color: #fff;
        }
        .logo { font-weight: bold; font-size: 1.3rem; }
        .nav-links { list-style: none; display: flex; }
        .nav-links li { margin-left: 20px; }
        .nav-links a {
            text-decoration: none; color: #fff; transition: 0.3s;
        }
        .nav-links a:hover { color: #00bcd4; }
        .hero {
            height: 100vh;
            background: url('https://source.unsplash.com/1600x900/?technology,coding') center/cover no-repeat;
            display: flex; justify-content: center; align-items: center; text-align: center;
            color: white; padding: 0 20px;
        }
        .hero h1 { font-size: 3rem; }
        .hero span { color: #00bcd4; }
        .hero .btn {
            display: inline-block; padding: 10px 20px; margin-top: 20px;
            background: #00bcd4; color: white; text-decoration: none;
            border-radius: 5px; transition: 0.3s;
        }
        .hero .btn:hover { background: #0097a7; }
        section { padding: 80px 20px; text-align: center; }
        .projects-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;
        }
        .project-card {
            padding: 20px; background: #f4f4f4; border-radius: 10px; transition: 0.3s;
        }
        .project-card:hover { transform: translateY(-5px); background: #e0f7fa; }
        form {
            max-width: 500px; margin: auto; display: flex; flex-direction: column;
        }
        form input, form textarea {
            margin: 10px 0; padding: 10px; border: 1px solid #ccc; border-radius: 5px;
        }
        form button {
            background: #00bcd4; color: white; border: none; padding: 10px;
            border-radius: 5px; cursor: pointer; transition: 0.3s;
        }
        form button:hover { background: #0097a7; }
        footer {
            background: #222; color: #fff; text-align: center; padding: 1rem; margin-top: 20px;
        }
        /* Mobile responsive */
        @media (max-width: 768px) {
            .nav-links { flex-direction: column; display: none; background: #222; width: 100%; text-align: center; }
            .nav-links.active { display: flex; }
            .navbar { flex-direction: column; }
        }
        .menu-toggle {
            display: none; font-size: 1.8rem; cursor: pointer; color: #fff;
        }
        @media (max-width: 768px) {
            .menu-toggle { display: block; }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <header>
        <nav class="navbar">
            <div class="logo">MyPortfolio</div>
            <div class="menu-toggle">&#9776;</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm <span>Your Name</span></h1>
            <p>A Passionate Web Developer</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Me</h2>
        <p>Hello! I'm a web developer passionate about creating beautiful and functional websites. 
           I love coding, solving problems, and bringing ideas to life on the web.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <h2>My Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Project 1</h3>
                <p>Description of your project.</p>
            </div>
            <div class="project-card">
                <h3>Project 2</h3>
                <p>Description of your project.</p>
            </div>
            <div class="project-card">
                <h3>Project 3</h3>
                <p>Description of your project.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit" class="btn">Send Message</button>
        </form>
    </section>

    <footer>
        <p>© 2025 Your Name. All rights reserved.</p>
    </footer>

    <script>
        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener("click", function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute("href")).scrollIntoView({
                    behavior: "smooth"
                });
            });
        });

        // Simple contact form validation
        document.getElementById("contactForm").addEventListener("submit", function(e) {
            e.preventDefault();
            alert("Thank you for your message! I'll get back to you soon.");
            this.reset();
        });

        // Mobile menu toggle
        const menuToggle = document.querySelector(".menu-toggle");
        const navLinks = document.querySelector(".nav-links");
        menuToggle.addEventListener("click", () => {
            navLinks.classList.toggle("active");
        });
    </script>
</body>
</html>
