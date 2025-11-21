# Personal Portfolio Website 🌐

A modern, responsive personal portfolio website showcasing projects, skills, and experience. Built with **HTML5**, **CSS3**, and **vanilla JavaScript**. Features a clean design, dark/light theme toggle, and mobile-responsive layout.

---

## ✨ Features

### 🎨 Design
- ✅ Modern, clean UI/UX design
- ✅ Responsive on all devices (mobile, tablet, desktop)
- ✅ Smooth animations & transitions
- ✅ Dark/Light theme toggle
- ✅ Professional color scheme

### 📱 Responsiveness
- ✅ Mobile-first approach
- ✅ Media queries for all breakpoints
- ✅ Touch-friendly navigation
- ✅ Flexible grid layouts

### 🧩 Sections
- ✅ Hero section with CTA
- ✅ About me with biography
- ✅ Skills showcase with icons
- ✅ Projects portfolio with descriptions
- ✅ Contact form with validation
- ✅ Social links & footer

### ⚡ Functionality
- ✅ Smooth scrolling
- ✅ Form validation
- ✅ Theme persistence
- ✅ Modal windows for project details
- ✅ Newsletter subscription

---

## 📁 Project Structure

```
portfolio-website/
├── index.html              # Main HTML file
├── styles/
│   ├── main.css           # Main stylesheet
│   ├── responsive.css     # Media queries
│   └── themes.css         # Dark/Light themes
├── scripts/
│   ├── main.js            # Main JavaScript
│   ├── theme.js           # Theme switcher
│   ├── scroll.js          # Smooth scrolling
│   └── form.js            # Form handling
├── assets/
│   ├── images/
│   │   ├── hero.jpg
│   │   ├── about.jpg
│   │   ├── projects/
│   │   └── skills/
│   ├── icons/
│   │   ├── github.svg
│   │   ├── linkedin.svg
│   │   └── ...
│   └── fonts/
└── README.md
```

---

## 🎯 Sections Breakdown

### 1. Header & Navigation
```html
<header class="header">
    <nav class="navbar">
        <div class="logo">Jalel Masmoudi</div>
        <ul class="nav-links">
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button class="theme-toggle">🌙</button>
    </nav>
</header>
```

### 2. Hero Section
```html
<section class="hero">
    <div class="hero-content">
        <h1>Hi! I'm Jalel Masmoudi</h1>
        <p>Computer Science Student | Problem Solver | Algorithms Enthusiast</p>
        <a href="#projects" class="cta-button">View My Work</a>
    </div>
    <img src="assets/images/hero.jpg" alt="Hero Image">
</section>
```

### 3. About Section
```html
<section id="about" class="about">
    <div class="about-content">
        <img src="assets/images/about.jpg" alt="Profile">
        <div class="about-text">
            <h2>About Me</h2>
            <p>I'm a 19-year-old CS student from Tunisia...</p>
            <p>My passion lies in solving complex problems...</p>
            <div class="stats">
                <div class="stat">
                    <h3>50+</h3>
                    <p>Problems Solved</p>
                </div>
                <div class="stat">
                    <h3>5</h3>
                    <p>Projects Completed</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

### 4. Skills Section
```html
<section id="skills" class="skills">
    <h2>Skills & Technologies</h2>
    <div class="skills-grid">
        <div class="skill-card">
            <img src="assets/icons/python.svg" alt="Python">
            <h3>Python</h3>
            <p>Data structures, algorithms, scripting</p>
        </div>
        <div class="skill-card">
            <img src="assets/icons/cpp.svg" alt="C++">
            <h3>C++</h3>
            <p>Competitive programming, system code</p>
        </div>
        <!-- More skills... -->
    </div>
</section>
```

### 5. Projects Section
```html
<section id="projects" class="projects">
    <h2>Featured Projects</h2>
    <div class="projects-grid">
        <article class="project-card">
            <img src="assets/images/project1.jpg" alt="Algorithm Library">
            <h3>Algorithm Library</h3>
            <p>Comprehensive collection of algorithms and data structures</p>
            <div class="project-tags">
                <span>Python</span>
                <span>C++</span>
                <span>Algorithms</span>
            </div>
            <a href="https://github.com/..." class="project-link">View Project</a>
        </article>
        <!-- More projects... -->
    </div>
</section>
```

### 6. Contact Section
```html
<section id="contact" class="contact">
    <h2>Get In Touch</h2>
    <form class="contact-form" id="contactForm">
        <input type="text" placeholder="Your Name" required>
        <input type="email" placeholder="Your Email" required>
        <textarea placeholder="Your Message" rows="5" required></textarea>
        <button type="submit" class="submit-btn">Send Message</button>
    </form>
</section>
```

---

## 🎨 Styling Highlights

### Color Scheme

**Light Mode:**
```css
--primary-color: #2180f3;      /* Blue */
--secondary-color: #f59e0b;    /* Amber */
--background: #f9fafb;         /* Light gray */
--text-primary: #1f2937;       /* Dark gray */
--text-secondary: #6b7280;     /* Medium gray */
```

**Dark Mode:**
```css
--primary-color: #60a5fa;      /* Light blue */
--secondary-color: #fbbf24;    /* Light amber */
--background: #1f2937;         /* Dark gray */
--text-primary: #f3f4f6;       /* Light gray */
--text-secondary: #d1d5db;     /* Medium light gray */
```

### Responsive Breakpoints

```css
/* Mobile: < 768px */
@media (max-width: 768px) {
    .nav-links { flex-direction: column; }
    .hero { flex-direction: column; }
    .projects-grid { grid-template-columns: 1fr; }
}

/* Tablet: 768px - 1024px */
@media (min-width: 768px) and (max-width: 1024px) {
    .projects-grid { grid-template-columns: repeat(2, 1fr); }
}

/* Desktop: > 1024px */
@media (min-width: 1024px) {
    .projects-grid { grid-template-columns: repeat(3, 1fr); }
}
```

---

## 📜 Key JavaScript Functions

### Theme Switcher
```javascript
// Toggle between dark and light theme
function toggleTheme() {
    const html = document.documentElement;
    const currentTheme = html.getAttribute('data-theme') || 'light';
    const newTheme = currentTheme === 'light' ? 'dark' : 'light';
    
    html.setAttribute('data-theme', newTheme);
    localStorage.setItem('theme', newTheme);
    updateThemeIcon(newTheme);
}

// Persist theme preference
window.addEventListener('DOMContentLoaded', () => {
    const saved = localStorage.getItem('theme') || 'light';
    document.documentElement.setAttribute('data-theme', saved);
});
```

### Smooth Scrolling
```javascript
// Smooth scroll to sections
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        target.scrollIntoView({ behavior: 'smooth' });
    });
});
```

### Form Validation
```javascript
// Validate contact form
const form = document.getElementById('contactForm');
form.addEventListener('submit', (e) => {
    e.preventDefault();
    
    const name = form.name.value.trim();
    const email = form.email.value.trim();
    const message = form.message.value.trim();
    
    // Validate email format
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    
    if (!name || !email || !message) {
        alert('Please fill all fields');
        return;
    }
    
    if (!emailRegex.test(email)) {
        alert('Please enter valid email');
        return;
    }
    
    // Send form data
    submitForm(name, email, message);
});
```

### Scroll Animation
```javascript
// Animate elements on scroll
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -100px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('fade-in');
            observer.unobserve(entry.target);
        }
    });
}, observerOptions);

document.querySelectorAll('.fade-on-scroll').forEach(el => {
    observer.observe(el);
});
```

---

## 🚀 Getting Started

### Clone & Open
```bash
# Clone repository
git clone https://github.com/jalel-masmoudi/portfolio-website.git
cd portfolio-website

# Open in browser
open index.html  # macOS
# or
start index.html # Windows
# or
xdg-open index.html # Linux
```

### Customize

1. **Update Personal Info**
   - Edit name in header
   - Update hero text
   - Add your bio in About section

2. **Add Projects**
   - Edit projects in HTML
   - Add project images
   - Update GitHub links

3. **Modify Colors**
   - Edit CSS variables in `main.css`
   - Update theme colors for brand

4. **Contact Form**
   - Set up form backend (FormSpree, Netlify)
   - Update form submission handler

---

## 📱 Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers

---

## 🎯 Optimization

### Performance Tips
- ✅ Optimize images (use WebP format)
- ✅ Minify CSS & JS
- ✅ Lazy load images
- ✅ Enable caching
- ✅ Use CDN for assets

### SEO Optimization
- ✅ Proper meta tags
- ✅ Semantic HTML
- ✅ Alt text for images
- ✅ Structured data (Schema.org)
- ✅ Mobile-friendly design

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfolio of Jalel Masmoudi...">
    <meta name="keywords" content="CS Student, Algorithms, Programming">
    <title>Jalel Masmoudi - CS Student & Problem Solver</title>
</head>
```

---

## 🔧 Advanced Features

### Add Blog Section
```html
<section id="blog" class="blog">
    <h2>Latest Blog Posts</h2>
    <!-- Blog cards -->
</section>
```

### Add Testimonials
```html
<section class="testimonials">
    <h2>What People Say</h2>
    <!-- Testimonial cards -->
</section>
```

### Add Newsletter
```html
<section class="newsletter">
    <h2>Subscribe for Updates</h2>
    <form class="newsletter-form">
        <input type="email" placeholder="Enter email">
        <button type="submit">Subscribe</button>
    </form>
</section>
```

---

## 🚢 Deployment

### Deploy to GitHub Pages
```bash
# Push to GitHub
git add .
git commit -m "Deploy portfolio"
git push origin main

# In repository settings, enable GitHub Pages
```

### Deploy to Netlify
```bash
# Connect GitHub repository
# Automatic deployments on push
```

### Deploy to Vercel
```bash
# Import project from GitHub
# Automatic deployments
```

---

## 📊 Page Speed Insights

Target Metrics:
- ✅ Lighthouse score: 90+
- ✅ First Contentful Paint: < 1.5s
- ✅ Cumulative Layout Shift: < 0.1

---

## 🤝 Customization Tips

✅ **Use your actual projects**
✅ **Add real images**
✅ **Update all links**
✅ **Set up contact form**
✅ **Add social links**
✅ **Maintain consistency**
✅ **Test on multiple devices**

---

## 📄 License

MIT License - Feel free to use as template!

---

## 👤 Author

**Jalel Masmoudi**  
Computer Science Student | Portfolio Website  
📧 jalel.masmoudi@example.com

---

*Last Updated: November 2025*  
*Your portfolio is your digital first impression!* ✨
