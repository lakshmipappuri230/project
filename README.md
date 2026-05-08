# project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Green Valley International School - Excellence in Education</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #f5f7fb;
            color: #333;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: auto;
        }

        /* ================= HEADER ================= */

        header {
            background: linear-gradient(135deg, #0f172a, #2563eb);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 3px 10px rgba(0,0,0,0.15);
        }

        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: white;
            text-decoration: none;
            font-size: 1.8rem;
            font-weight: 700;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            color: white;
            font-weight: 500;
            padding: 8px 15px;
            border-radius: 6px;
            transition: 0.3s;
        }

        nav a:hover {
            background: rgba(255,255,255,0.2);
        }

        .menu-toggle {
            display: none;
            color: white;
            background: none;
            border: none;
            font-size: 1.7rem;
            cursor: pointer;
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 40px 20px;
            background:
                linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
                url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?q=80&w=1600&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            color: white;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 30px;
        }

        .hero-btn {
            background: #facc15;
            color: #111827;
            border: none;
            padding: 14px 35px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.3s;
        }

        .hero-btn:hover {
            transform: translateY(-3px);
            background: #fde047;
        }

        #special-message {
            margin-top: 25px;
            display: none;
            font-size: 1.2rem;
            font-weight: bold;
            color: #facc15;
        }

        /* ================= SECTIONS ================= */

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: #0f172a;
            margin-bottom: 10px;
        }

        .section-title p {
            color: #666;
        }

        /* ================= ABOUT ================= */

        .about {
            background: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px,1fr));
            gap: 40px;
            align-items: center;
        }

        .about-text p {
            margin-bottom: 20px;
            line-height: 1.8;
            color: #555;
        }

        .about-image img {
            width: 100%;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        /* ================= COURSES ================= */

        .courses {
            background: #eef2ff;
        }

        .courses-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
            gap: 25px;
        }

        .course-card {
            background: white;
            padding: 30px;
            border-radius: 18px;
            text-align: center;
            transition: 0.3s;
            box-shadow: 0 4px 10px rgba(0,0,0,0.08);
        }

        .course-card:hover {
            transform: translateY(-10px);
        }

        .course-card h3 {
            margin: 20px 0;
            color: #1d4ed8;
        }

        .course-card p {
            color: #666;
            margin-bottom: 20px;
        }

        .course-btn {
            background: #2563eb;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            cursor: pointer;
            transition: 0.3s;
        }

        .course-btn:hover {
            background: #1d4ed8;
        }

        /* ================= CONTACT ================= */

        .contact {
            background: white;
        }

        .contact-form {
            max-width: 700px;
            margin: auto;
            background: #f8fafc;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 14px;
            border-radius: 10px;
            border: 1px solid #ccc;
            outline: none;
            transition: 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            border-color: #2563eb;
        }

        .submit-btn {
            width: 100%;
            background: #2563eb;
            color: white;
            border: none;
            padding: 14px;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: 0.3s;
        }

        .submit-btn:hover {
            background: #1d4ed8;
        }

        /* ================= FOOTER ================= */

        footer {
            background: #0f172a;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        footer p {
            margin: 8px 0;
        }

        /* ================= RESPONSIVE ================= */

        @media(max-width: 768px){

            nav ul {
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: #0f172a;
                flex-direction: column;
                text-align: center;
                display: none;
                padding: 20px 0;
            }

            nav ul.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.2rem;
            }

            .hero-content p {
                font-size: 1rem;
            }
        }
    </style>
</head>

<body>

    <!-- HEADER -->

    <header>
        <div class="container">
            <a href="#" class="logo">🏫 Green Valley International School</a>

            <nav>
                <ul id="navMenu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#courses">Programs</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>

            <button class="menu-toggle" id="menuToggle">☰</button>
        </div>
    </header>

    <!-- HERO -->

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Empowering Students for a Bright Future</h1>
            <p>Modern Education • Smart Learning • Global Excellence</p>

            <button class="hero-btn" id="heroBtn">
                Explore Our School
            </button>

            <div id="special-message">
                🌟 Welcome to Green Valley International School 🌟
            </div>
        </div>
    </section>

    <!-- ABOUT -->

    <section class="about" id="about">
        <div class="container">

            <div class="section-title">
                <h2>About Our School</h2>
                <p>Creating leaders of tomorrow through quality education</p>
            </div>

            <div class="about-content">

                <div class="about-text">
                    <p>
                        Green Valley International School is dedicated to academic
                        excellence, innovation, and holistic student development.
                        We provide a supportive environment where students can
                        grow intellectually, socially, and creatively.
                    </p>

                    <p>
                        Our highly qualified faculty members use modern teaching
                        methods and advanced technology to inspire students to
                        achieve their dreams and become confident future leaders.
                    </p>

                    <p>
                        With world-class facilities, extracurricular activities,
                        and student-focused learning, we ensure every child
                        receives the best educational experience.
                    </p>
                </div>

                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1509062522246-3755977927d7?q=80&w=1200&auto=format&fit=crop" alt="School">
                </div>

            </div>
        </div>
    </section>

    <!-- COURSES -->

    <section class="courses" id="courses">

        <div class="container">

            <div class="section-title">
                <h2>Academic Programs</h2>
                <p>Explore our modern and interactive learning programs</p>
            </div>

            <div class="courses-grid">

                <div class="course-card">
                    <h3>🔬 Science & Innovation</h3>
                    <p>
                        Interactive labs and hands-on experiments for future scientists.
                    </p>
                    <button class="course-btn">Read More</button>
                </div>

                <div class="course-card">
                    <h3>💻 Computer Education</h3>
                    <p>
                        Learn coding, digital literacy, and future technologies.
                    </p>
                    <button class="course-btn">Read More</button>
                </div>

                <div class="course-card">
                    <h3>📘 Mathematics</h3>
                    <p>
                        Build strong analytical and problem-solving skills.
                    </p>
                    <button class="course-btn">Read More</button>
                </div>

                <div class="course-card">
                    <h3>🎨 Arts & Creativity</h3>
                    <p>
                        Encourage imagination through music, dance, and art.
                    </p>
                    <button class="course-btn">Read More</button>
                </div>

            </div>
        </div>
    </section>

    <!-- CONTACT -->

    <section class="contact" id="contact">

        <div class="container">

            <div class="section-title">
                <h2>Contact Us</h2>
                <p>We would love to hear from you</p>
            </div>

            <form class="contact-form" id="contactForm">

                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" id="name" placeholder="Enter your name">
                </div>

                <div class="form-group">
                    <label>Email Address</label>
                    <input type="email" id="email" placeholder="Enter your email">
                </div>

                <div class="form-group">
                    <label>Your Message</label>
                    <textarea rows="5" id="message" placeholder="Write your message"></textarea>
                </div>

                <button type="submit" class="submit-btn">
                    Send Message
                </button>

            </form>

        </div>
    </section>

    <!-- FOOTER -->

    <footer>
        <p>© 2026 Green Valley International School</p>
        <p>📍 Punjab, India | 📞 +91 98765 43210</p>
        <p>📧 info@greenvalleyschool.edu</p>
    </footer>

    <!-- JAVASCRIPT -->

    <script>

        // MOBILE MENU

        const menuToggle = document.getElementById("menuToggle");
        const navMenu = document.getElementById("navMenu");

        menuToggle.addEventListener("click", () => {
            navMenu.classList.toggle("active");
        });

        // HERO MESSAGE

        const heroBtn = document.getElementById("heroBtn");
        const specialMessage = document.getElementById("special-message");

        heroBtn.addEventListener("click", () => {

            if (specialMessage.style.display === "block") {
                specialMessage.style.display = "none";
                heroBtn.innerText = "Explore Our School";
            } else {
                specialMessage.style.display = "block";
                heroBtn.innerText = "Hide Message";
            }
        });

        // CONTACT FORM

        const contactForm = document.getElementById("contactForm");

        contactForm.addEventListener("submit", function(e){

            e.preventDefault();

            const name = document.getElementById("name").value;
            const email = document.getElementById("email").value;
            const message = document.getElementById("message").value;

            if(name === "" || email === "" || message === ""){
                alert("Please fill all fields.");
            } else {
                alert("Message sent successfully!");
                contactForm.reset();
            }

        });

    </script>

</body>
</html>
