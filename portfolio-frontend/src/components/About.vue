<template>
  <section id="about">
    <div class="about-container">
      <!-- Left side: Image -->
      <div class="about-image">
        <img src="@/assets/apprnt.jpg" alt="About Me" />
      </div>

      <!-- Right side: Text and Button -->
      <div class="about-text">
        <!-- Combined About Me and Subtitle in One Paragraph (2 lines) -->
        <p class="about-title">
          About Me: <br /> I am a Website Developer
        </p>

        <!-- Combined Text into One Paragraph -->
        <p class="about-paragraph">
          I'm a passionate web developer, dedicated to building high-quality websites. I specialize in frontend and backend technologies, creating responsive and interactive web applications. My focus is always on delivering the best user experience while ensuring optimal performance. Let's collaborate to create something amazing and bring your ideas to life!
        </p>

         <!-- Contact Me -->
         <p class="button-paragraph">
          <button @click="scrollToContact" class="contact-button">Contact Me</button>
        </p>
      </div>
    </div>

    <!-- Technologies Section within the About Section -->
    <div class="technologies-wrapper">
      <h2 class="tech-title">Technologies I Work With</h2>

      <!-- MENU: Technologies Section with icons -->
      <div class="tech-icons">
        <div class="tech-item">
          <img src="../assets/icons/laravel-icon.jpg" alt="Laravel" />
          <span>Laravel</span>
        </div>
        
        <div class="tech-item">
          <img src="../assets/icons/vue-icon.jpg" alt="Vue.js" />
          <span>Vue.js</span>
        </div>
        <div class="tech-item">
          <img src="../assets/icons/java-icon.png" alt="Java" />
          <span>Java</span>
        </div>
        
        <div class="tech-item">
          <img src="../assets/icons/python-icon.jpg" alt="Python" />
          <span>Python</span>
        </div>
        
        <div class="tech-item">
          <img src="../assets/icons/networking-icon.jpg" alt="Networking" />
          <span>Networking</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section (Example) -->
  <section id="portfolio">
    <!-- Portfolio content goes here -->
  </section>
</template>

<script>
export default {
  name: 'AboutSection',  // Multi-word component name
  methods: {
    scrollToContact() {
      const contactSection = document.getElementById("contact");
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: "smooth" });
      }
    },
  },

}
</script>

<style scoped>
/* Section Styling for About */
section#about {
  margin-top: 100px;
  margin-bottom: 40px;
  padding: 40px 10px;
  min-height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  position: relative;
  padding-top: 80px;
}

.about-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  max-width: 960px;
  gap: 20px;
}

.about-image {
  flex: 1;
  padding: 20px;
  text-align: center;
  display: flex;
  justify-content: center;
}

.about-image img {
  max-width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 10px;
  width: 100%;
  max-height: 300px;
}

.about-text {
  flex: 2;
  padding: 20px;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.about-title {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 10px;
  line-height: 1.5;
}

.about-paragraph {
  font-size: 1.1rem;
  line-height: 1.6;
  margin-bottom: 20px;
  color: #333;
}

.button-paragraph {
  margin-top: 20px;
}

.contact-button {
  background-color: #e9967a;
  color: white;
  font-size: 1.2rem;
  padding: 12px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: fit-content;
  transition: background-color 0.3s ease;
}

.contact-button:hover {
  background-color: #c67c56;
}

.technologies-wrapper {
  background-color: #f0f8ff;
  padding: 40px 20px;
  text-align: center;
  border-radius: 10px;
  margin-top: 40px;
  width: 100%;
  max-width: 960px;
}

.tech-title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 20px;
}

.tech-icons {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
  gap: 20px;
  justify-items: center;
}

.tech-item {
  text-align: center;
}

.tech-item img {
  width: 60px;
  height: 60px;
  object-fit: contain;
  margin-bottom: 10px;
}

.tech-item span {
  display: block;
  font-size: 1rem;
  font-weight: bold;
  color: #333;
}

@media (max-width: 768px) {
  .about-container {
    flex-direction: column;
    align-items: center;
  }

  .about-image, .about-text {
    flex: none;
    width: 100%;
    padding: 10px;
  }

  .about-text {
    text-align: center;
  }

  .about-paragraph {
    text-align: justify;
  }

  .tech-icons {
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
  }
}
</style>
