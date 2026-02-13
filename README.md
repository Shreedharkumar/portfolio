# Ex01 Portfolio
## Date: 13.03.2026

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SHREEDHAR | Portfolio</title>
  
  <!-- CSS & JS -->
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>

  <!-- Icons & Fonts -->
  <link href="https://cdn.jsdelivr.net/npm/remixicon@4.2.0/fonts/remixicon.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
</head>
<body>
  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">SHREEDHAR</div>
      <ul class="nav-links">
        <li><a href="#home" class="active">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Hi, It's <span>SHREE</span></h1>
      <h2>I'm a <span class="highlight">Software Developer</span></h2>
      <p>
        Passionate developer with skills in building modern, responsive, 
        and user-friendly web applications. I enjoy solving problems and 
        creating clean, efficient code.
      </p>
      
      <!-- Social Icons -->
      <div class="social-icons">
        <a href="https://www.linkedin.com/in/shreedhar-kumar-29795332a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"><i class="ri-linkedin-fill"></i></a>
        <a href="https://github.com/Shreedharkumar"><i class="ri-github-fill"></i></a>
        <a href=""><i class="ri-twitter-x-fill"></i></a>
        <a href="https://www.instagram.com/p/DMhc56pxoAn/?utm_source=ig_web_button_share_sheet&igsh=MTFjcTA3cGxzbTAzYg=="><i class="ri-instagram-line"></i></a>
      </div>

      <!-- Call-to-action -->
      <a href="#contact" class="btn">Hire Me</a>
    </div>

    <!-- Profile Image -->
    <div class="hero-img">
      <!-- 👇 make sure this image is inside assets/images/ -->
      <img src="pic.png" alt="My Profile Picture">
    </div>
  </section>
</body>
</html>

```

CSS
```
/* Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  background: #0d0d0d;
  color: #fff;
  line-height: 1.6;
}

/* Navbar */
header {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  background: #0d0d0d;
  padding: 20px 50px;
  z-index: 1000;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 22px;
  font-weight: 700;
  color: #ff4d6d;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 25px;
}

.nav-links li a {
  text-decoration: none;
  color: #fff;
  transition: 0.3s;
}

.nav-links li a.active,
.nav-links li a:hover {
  color: #ff4d6d;
}

/* Hero Section */
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-height: 100vh;
  padding: 0 80px;
}

.hero-content {
  max-width: 50%;
}

.hero-content h1 {
  font-size: 48px;
  margin-bottom: 15px;
}

.hero-content h1 span {
  color: #ff4d6d;
}

.hero-content h2 {
  font-size: 30px;
  margin-bottom: 20px;
}

.highlight {
  color: #ff4d6d;
}

.hero-content p {
  margin-bottom: 25px;
  color: #aaa;
}

/* Social Icons */
.social-icons {
  display: flex;
  gap: 20px;
  margin-bottom: 30px;
}

.social-icons a {
  font-size: 22px;
  color: #fff;
  transition: 0.3s;
}

.social-icons a:hover {
  color: #ff4d6d;
}

/* Button */
.btn {
  display: inline-block;
  padding: 12px 28px;
  background: transparent;
  border: 2px solid #ff4d6d;
  color: #ff4d6d;
  font-size: 16px;
  border-radius: 30px;
  transition: 0.3s;
}

.btn:hover {
  background: #ff4d6d;
  color: #fff;
}

/* Hero Image */
.hero-img img {
  width: 350px;
  border-radius: 50%;
  box-shadow: 0 0 40px rgba(255, 77, 109, 0.6);
}

/* Responsive */
@media (max-width: 900px) {
  .hero {
    flex-direction: column-reverse;
    text-align: center;
    padding: 100px 30px;
  }

  .hero-content {
    max-width: 100%;
  }

  .hero-img img {
    width: 250px;
    margin-bottom: 30px;
  }
}

```
SCRIPT.JS
```
// Navbar active link effect
const navLinks = document.querySelectorAll('.nav-links a');

navLinks.forEach(link => {
  link.addEventListener('click', () => {
    navLinks.forEach(nav => nav.classList.remove('active'));
    link.classList.add('active');
  });
});

// Optional: Smooth scroll effect
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener("click", function(e) {
    e.preventDefault();
    document.querySelector(this.getAttribute("href")).scrollIntoView({
      behavior: "smooth"
    });
  });
});

```
## OUTPUT
<img width="1919" height="1040" alt="image" src="https://github.com/user-attachments/assets/d1d2b7b0-2f30-40b8-abd8-8ed24f22459f" />

## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
