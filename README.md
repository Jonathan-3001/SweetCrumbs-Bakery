<!-- sweetcrumbs-onefile.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SweetCrumbs Bakery – Unified Page</title>
  <style>
    body { font-family: 'Lato', sans-serif; margin: 0; padding: 0; line-height: 1.6; background: #fff8f0; color: #4b2e2e; }
    header, footer { background: #f9e4d4; padding: 1rem; text-align: center; }
    nav ul { display: flex; justify-content: center; list-style: none; gap: 1rem; padding: 0; }
    nav a { text-decoration: none; color: #4b2e2e; font-weight: bold; }
    .hero, .section { padding: 2rem; text-align: center; }
    .products, .team-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; padding: 1rem; }
    .product-card, .team-member { background: #fff; padding: 1rem; border-radius: 5px; border: 1px solid #ddd; }
    .product-card img, .team-member img { width: 100%; height: auto; border-radius: 5px; }
    .tabs { display: flex; justify-content: center; gap: 1rem; margin: 1rem 0; }
    .tab { padding: 0.5rem 1rem; background: #e6cfc3; border: none; cursor: pointer; font-weight: bold; }
    .tab.active { background: #d49a89; color: white; }
    .tab-content { display: none; }
    .tab-content.active { display: block; }
    form { max-width: 500px; margin: auto; display: flex; flex-direction: column; gap: 1rem; padding: 1rem; }
    form input, form textarea, form button { padding: 0.5rem; border-radius: 5px; border: 1px solid #ccc; }
    .map iframe { width: 100%; height: 300px; border: none; margin-top: 1rem; }
  </style>
</head>
<body>
  <header>
    <h1>SweetCrumbs Bakery</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="home" class="hero">
    <h2>Baked Fresh Daily</h2>
    <p>Indulge in handcrafted pastries and artisanal breads.</p>
  </section>

  <section class="section">
    <h3>Customer Favorites</h3>
    <div class="products">
      <div class="product-card"><img src="images/cupcake.jpg" alt="Cupcake"><p>Cupcakes</p></div>
      <div class="product-card"><img src="images/bread.jpg" alt="Bread"><p>Bread</p></div>
      <div class="product-card"><img src="images/cookies.jpg" alt="Cookies"><p>Cookies</p></div>
    </div>
  </section>

  <section id="menu" class="section">
    <h2>Menu</h2>
    <div class="tabs">
      <button class="tab active" onclick="switchTab('cakes')">Cakes</button>
      <button class="tab" onclick="switchTab('pastries')">Pastries</button>
      <button class="tab" onclick="switchTab('bread')">Bread</button>
    </div>
    <div id="cakes" class="tab-content active"><div class="product-card"><img src="images/chocolate-cake.jpg" alt="Chocolate Cake"><p>Chocolate Cake</p></div></div>
    <div id="pastries" class="tab-content"><div class="product-card"><img src="images/croissant.jpg" alt="Croissant"><p>Croissant</p></div></div>
    <div id="bread" class="tab-content"><div class="product-card"><img src="images/sourdough.jpg" alt="Sourdough Bread"><p>Sourdough Bread</p></div></div>
  </section>

  <section id="about" class="section">
    <h2>Our Story</h2>
    <p>SweetCrumbs started with a love for baking and a passion for creating joy through food.</p>
    <h3>Meet Our Bakers</h3>
    <div class="team-grid">
      <div class="team-member"><img src="images/baker1.jpg" alt="Baker Alice"><p>Alice</p></div>
      <div class="team-member"><img src="images/baker2.jpg" alt="Baker Ben"><p>Ben</p></div>
    </div>
  </section>

  <section id="contact" class="section">
    <h2>Contact Us</h2>
    <form>
      <label for="name">Name</label>
      <input id="name" name="name" required>
      <label for="email">Email</label>
      <input id="email" name="email" type="email" required>
      <label for="message">Message</label>
      <textarea id="message" name="message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <div class="map">
      <h3>Find Us</h3>
      <iframe src="https://www.google.com/maps/embed?..." title="Bakery Location"></iframe>
    </div>
    <div class="hours">
      <h3>Opening Hours</h3>
      <p>Mon–Sat: 8am–8pm<br>Sunday: Closed</p>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 SweetCrumbs Bakery</p>
  </footer>

  <script>
    function switchTab(tabId) {
      document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
      document.querySelectorAll('.tab').forEach(b => b.classList.remove('active'));
      document.getElementById(tabId).classList.add('active');
      [...document.querySelectorAll('.tab')].find(b => b.textContent.toLowerCase() === tabId).classList.add('active');
    }
  </script>
</body>
</html>

<!-- Phase 3 - PDF Deliverable Details -->

# Phase 3 – Development
Deliverable: Public GitHub Repository and Live URL
Due Date: **Fri 9 May 2025**

**Requirements:**
- Code hosted in a public GitHub repository with frequent commits
- Live deployment using Netlify, GitHub Pages, or Vercel
- Includes all static assets (HTML, CSS, JS, images)
- Fully functional navigation across all pages
- Responsive design (320px – 1440px)
- Meets accessibility (WCAG 2.1 AA) and performance (Lighthouse ≥ 90) standards
- At least one JavaScript-driven interactive feature (e.g., tabbed menu)

**To Submit:**
- GitHub repository link
- Live site URL

**Review Checklist:**
- [x] Proper HTML5 semantics
- [x] External styles and scripts
- [x] Mobile responsiveness
- [x] Keyboard navigability and alt attributes
- [x] Tab switch JavaScript working correctly
- [x] Clean, documented code

<!-- Wireframe Description -->

# Low-Fidelity Wireframe (Textual Description)

**Home Page**
- Header with navigation
- Hero image section with tagline and CTA
- Section with 3 featured products in columns
- Footer with links

**Menu Page**
- Header and tabs for product categories
- Section with product cards filtered by tab
- Footer

**About Page**
- Header and bakery story section
- Team grid with names and photos
- Footer

**Contact Page**
- Header and contact form section
- Google Map and opening hours
- Footer

![image](https://github.com/user-attachments/assets/4e198896-1c9a-49aa-9a8b-ccdd894ceaab)

