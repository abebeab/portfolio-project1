<template>
  <div id="app">
    <!-- Header Section -->
    <header class="header">
      <div class="logo">
        <img src="@/assets/icons/logo.png" alt="Super Digital HiTECHh Logo" class="logo-img" />
        <span class="logo-text">Super Digital TECHh</span>
      </div>

      <!-- Menu Container: "MENU" label and hamburger icon -->
      <nav class="navbar">
        <div class="menu-container">
          <!-- MENU Label (shown on mobile) -->
          <span class="menu-label">MENU</span>

          <!-- Hamburger Icon for mobile view -->
          <div class="hamburger" @click="toggleMenu">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
          </div>
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
      <HomeComponent />  
      <About />  
      <Portfolio />  
      <Services />  
      <Contact />  
    </main>

    <!-- Footer Section -->
    <AppFooter /> 
  </div>
</template>

<script>
// Import components
import HomeComponent from './components/HomeComponent.vue';
import About from './components/About.vue';
import Services from './components/Services.vue';
import Portfolio from './components/Portfolio.vue';  
import Contact from './components/Contact.vue';  
import AppFooter from './components/AppFooter.vue';  

export default {
  name: 'App',
  components: {
    HomeComponent,
    About,
    Services,
    Portfolio,  
    Contact,  
    AppFooter,  
  },
  data() {
    return {
      menuActive: false,  
    };
  },
  methods: {
    toggleMenu() {
      this.menuActive = !this.menuActive;  
    },
    scrollToSection(id) {
      const section = document.querySelector(id);
      if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
        this.menuActive = false;  
      }
    },
  },
};
</script>

<style scoped>
/* Global Styles */
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow-x: hidden;
}

#app {
  max-width: 100%;
  height: 100%;
}

/* Header Styles */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color: #2c3e50; /* Dark, professional background */
  color: #fff;
  width: 100%;
  box-sizing: border-box;
  min-height: 100px; /* Increased height for a larger header */
  position: sticky;
  top: 0;
  z-index: 1000;
  flex-wrap: nowrap;
}

.logo {
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: center;
  text-align: center;
}

.logo-img {
  width: 180px; /* Set logo size to 180px for larger desktop view */
  height: 180px; /* Set logo height to 180px for larger desktop view */
  border-radius: 50%;
  margin-right: 20px; /* Space between logo and text */
  transition: transform 0.3s ease-in-out; /* Smooth scaling */
}

.logo-img:hover {
  transform: scale(1.15); /* Slightly enlarge logo on hover */
}

.logo-text {
  font-size: 2rem; /* Increased font size */
  font-weight: bold;
  color: #f39c12; /* Bright color to match the TECHh vibe */
  text-transform: uppercase; /* Make text stand out */
  letter-spacing: 3px; /* Spacing for a more stylish effect */
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
  justify-content: space-between;
}

.navbar li {
  margin-left: 30px; /* More space between items */
}

.navbar a {
  text-decoration: none;
  font-size: 1.2rem;
  padding: 8px 20px;
  border-radius: 5px;
  color: #fff;
  transition: background-color 0.3s;
}

.navbar a:hover {
  background-color: #f39c12;
  color: #333; /* Hover effect for better visibility */
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
  background-color: #fff;
  border-radius: 2px;
}

/* MENU Text positioned on the right side (for mobile view and inspection) */
.menu-label {
  display: none;
  font-size: 1.2rem;
  font-weight: bold;
  margin-right: 20px;
  color: #fff;
}

.menu-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

@media (max-width: 768px) {
  .header {
    padding: 20px 15px;
  }

  .navbar ul {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 60px;
    right: 0;
    background-color: #34495e;
    box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
    width: 100%;
    padding: 20px 0;
    margin: 0;
  }

  .navbar ul.active {
    display: flex;
  }

  .hamburger {
    display: flex;
  }

  .navbar li {
    margin: 10px 0;
    text-align: center;
  }

  .navbar a {
    width: 100%;
    text-align: left;
    padding: 15px 20px;
  }

  .menu-label {
    display: block;
    margin-right: 20px;
    font-size: 1.2rem;
    font-weight: bold;
    color: #fff;
    margin-top: 5px;
  }

  .logo {
    flex-direction: column;
    text-align: center;
  }

  .logo-img {
    width: 150px; /* Increase size for mobile */
    height: 150px; /* Increase size for mobile */
    margin-bottom: 10px; /* Space between logo and text on mobile */
    transition: transform 0.3s ease; /* Smooth scaling for mobile */
  }

  .logo-img:hover {
    transform: scale(1.2); /* Slightly enlarge logo on hover for mobile */
  }

  .menu-container {
    flex-direction: column;
    align-items: center;
  }
}
</style>
