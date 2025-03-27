<template>
  <div id="app">
    <!-- Header Section -->
    <header class="header">
      <div class="logo">
        <i class="fas fa-laravel"></i>
        <span>My Portfolio here!!</span>
      </div>

      <nav class="navbar">
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact" class="contact-link">Contact</a></li>
        </ul>
      </nav>
    </header>

    <!-- Main Content Sections -->
    <main>
      <section id="home">
        <h2>Home</h2>
        <p>Welcome to my portfolio website.</p>
      </section>

      <section id="about">
        <h2>About Me</h2>
        <p>This is a brief introduction about myself.</p>
      </section>

      <section id="portfolio">
        <h2>My Portfolio</h2>
        <p>Here are some of the projects I have worked on.</p>
      </section>

      <section id="services">
        <h2>Services</h2>
        <p>Here are the services I offer.</p>
      </section>

      <section id="contact">
        <h2>Contact</h2>
        <p>Get in touch with me!</p>
      </section>
    </main>

    <!-- Footer Section -->
    <footer class="footer">
      <p>&copy; 2025 <a href="https://www.laravel.com" target="_blank">laravel.com</a> All Rights Reserved.</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style scoped>
/* Global Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #f9f9f9;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  scroll-behavior: smooth; /* Enable smooth scrolling */
}

/* Header Section */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color: #efdecd;
  color: #333;
  width: 100%;
  box-sizing: border-box;
  min-height: 80px;
  position: sticky;  /* Sticky positioning */
  top: 0;  /* Stick to the top of the page */
  z-index: 1000;  /* Ensure it's above other content */
}

.logo {
  display: flex;
  align-items: center;
}

.logo i {
  font-size: 36px;
  margin-right: 50px;
}

.logo span {
  font-size: 24px;
  font-weight: bold;
}

.navbar ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  gap: 20px;
}

.navbar li {
  padding: 10px;
}

.navbar a {
  text-decoration: none;
  color: #333;
  font-size: 18px;
  display: block;
}

.navbar a:hover {
  color: #f2f3f4;
}

.contact-link {
  margin-right: 0px;
}

/* Main Section Styles */
main {
  padding: 20px;
  width: 100%;
  text-align: center;
  background-color: #fff;
}

section {
  margin-bottom: 40px;
  padding:20px;
  min-height: 300px;
}

/* Footer Styling */
.footer {
  background-color: #f2f3f4;
  padding: 20px;
  text-align: center;
  font-size: 14px;
  color: #333;
  width: 100%;
  position: relative;
}

.footer p {
  margin: 0;
}

.footer a {
  color: #007bff;
  text-decoration: none;
}

.footer a:hover {
  text-decoration: underline;
}
</style>
