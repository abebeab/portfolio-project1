<template>
  <div id="app">
    <!-- Header Section -->
    <header class="header">
      <div class="logo">
        <img src="@/assets/icons/logo.png" alt="Logo" class="logo-img" />
        <span class="logo-text">My Portfolio here!!</span>
      </div>
      <nav class="navbar">
        <!-- MENU Text and Hamburger Icon in One Line -->
        <span class="menu-label">MENU</span>

        <!-- Hamburger Icon for mobile view -->
        <div class="hamburger" @click="toggleMenu">
          <span class="bar"></span>
          <span class="bar"></span>
          <span class="bar"></span>
        </div>

        <!-- Navigation Links -->
        <ul :class="{ 'active': menuActive }">
          <li><a href="#home" @click="scrollToSection('#home')" aria-label="Go to Home section">Home</a></li>
          <li><a href="#about" @click="scrollToSection('#about')" aria-label="Go to About section">About</a></li>
          <li><a href="#portfolio" @click="scrollToSection('#portfolio')" aria-label="Go to Portfolio section">Portfolio</a></li>
          <li><a href="#services" @click="scrollToSection('#services')" aria-label="Go to Services section">Services</a></li>
          <li><a href="#contact" @click="scrollToSection('#contact')" aria-label="Go to Contact section">Contact</a></li>
        </ul>
      </nav>
    </header>

    <!-- Main Content Sections -->
    <main>
      <HomeComponent />  <!-- Include HomeComponent instead of Home.vue -->
      <About />  <!-- Include About component here -->
      <Portfolio />  <!-- Include Portfolio component here -->
      <Services />  <!-- Include Services component here -->
      <Contact />  <!-- Include Contact component here -->
    </main>

    <!-- Footer Section -->
    <AppFooter /> <!-- Integrate the Footer Component here -->
  </div>
</template>

<script>
// Import components
import HomeComponent from './components/HomeComponent.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';
import Portfolio from './components/Portfolio.vue';  
import Contact from './components/Contact.vue';  
import AppFooter from './components/AppFooter.vue';  // Import the AppFooter component

export default {
  name: 'App',
  components: {
    HomeComponent,
    About,
    Services,
    Portfolio,  
    Contact,  
    AppFooter,  // Register the AppFooter component
  },
  data() {
    return {
      menuActive: false,  // To toggle the menu on mobile
    };
  },
  methods: {
    toggleMenu() {
      this.menuActive = !this.menuActive;  // Toggle the menu visibility
    },
    scrollToSection(id) {
      const section = document.querySelector(id);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
        this.menuActive = false;  // Close the mobile menu after clicking a link
      }
    },
  },
};
</script>

<style scoped>
/* Header Styles */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color:#d99058;
  color: #333;
  width: 100%;
  box-sizing: border-box;
  min-height: 80px;
  position: sticky;
  top: 0;
  z-index: 1000;
  flex-wrap: nowrap;  /* Prevent wrapping of elements */
}

.logo {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
}

.logo-img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-right: 15px;
}

.logo-text {
  font-size: 1.5rem;
  font-weight: bold;
  white-space: nowrap;
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  position: relative;
  width: 100%;
}

.navbar ul {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}

.navbar li {
  margin-left: 20px;
}

.navbar a {
  text-decoration: none;
  font-size: 1.2rem;
  padding: 8px 20px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.navbar a:hover {
  background-color:#f0f8ff;
}

/* Hamburger for mobile */
.hamburger {
  display: none;
  flex-direction: column;
  justify-content: space-around;
  height: 24px;
  width: 30px;
  cursor: pointer;
}

.hamburger .bar {
  height: 4px;
  width: 100%;
  background-color: #333;
  border-radius: 2px;
}

/* MENU Text positioned on the right side (for mobile view and inspection) */
.menu-label {
  display: none;
  font-size: 1.2rem;
  font-weight: bold;
  margin-right: 20px;
  color: #333;
}

@media (max-width: 768px) {
  .navbar ul {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 60px;
    right: 0;
    background-color: #efdecd;
    box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
  }

  .navbar ul.active {
    display: flex;
  }

  .hamburger {
    display: flex;
  }

  .navbar li {
    margin: 10px 0;
  }

  .navbar a {
    width: 100%;
    text-align: left;
  }

  /* Show the MENU text on smaller screens (inspection) and position it in line with hamburger */
  .menu-label {
    display: block;
    margin-right: 20px;
    font-size: 1.2rem;
    font-weight: bold;
    color: #333;
    margin-top: 5px;
  }
}
</style>
