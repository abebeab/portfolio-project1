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

        <!-- Button -->
        <p class="button-paragraph">
          <button class="contact-button">Contact Me</button>
        </p>
      </div>
    </div>

    <!-- Technologies Section within the About Section -->
    <div class="technologies-wrapper">
      <h2 class="tech-title">Technologies I Work With</h2>
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
}
</script>

<style scoped>
/* Section Styling for About *//* Section Styling for About */
section#about {
  margin-top: 100px; /* Increased the top margin to create a larger gap */
  margin-bottom: 40px;
  padding: 40px 10px; /* Reduced padding for narrowness */
  min-height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column; /* Stack image and text vertically */
  position: relative; /* Ensure the background works as expected */
  padding-top: 80px;
}


/* Container for flex layout in About Section */
.about-container {
  display: flex;
  align-items: center; /* Center the image vertically */
  justify-content: center;
  width: 100%;
  max-width: 960px; /* Reduced max-width to make it narrower */
  gap: 20px; /* Reduced gap between image and text */
}

/* Styling for the image */
.about-image {
  flex: 1;
  padding: 20px;
  text-align: center;
  display: flex;
  justify-content: center; /* Center the image horizontally */
}

.about-image img {
  max-width: 100%;
  height: auto; /* Adjust height to make the image shorter */
  object-fit: cover; /* Ensures image doesn't stretch, keeps aspect ratio */
  border-radius: 10px; /* Optional: adds rounded corners */
  width: 100%; /* Makes image fill the container */
  max-height: 300px; /* Constrains height */
}

/* Styling for the text and button in About */
.about-text {
  flex: 2;
  padding: 20px;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: flex-start; /* Align text to the top */
}

.about-title {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 10px;
  line-height: 1.5; /* Line height for better spacing between lines */
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

/* Technologies Section (inside About Section) */
.technologies-wrapper {
  background-color: #f0f8ff; /* Distinct background color for the technologies part */
  padding: 40px 20px;
  text-align: center;
  border-radius: 10px; /* Optional: rounded corners for tech section */
  margin-top: 40px; /* Adds space between About and Technologies */
  width: 100%;
  max-width: 960px; /* Keeps it narrow like the About Section */
}

.tech-title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 20px;
}

.tech-icons {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(100px, 1fr)); /* Responsive grid for icons */
  gap: 20px;
  justify-items: center; /* Centers icons */
}

.tech-item {
  text-align: center;
}

.tech-item img {
  width: 60px; /* Icon size */
  height: 60px; /* Icon size */
  object-fit: contain;
  margin-bottom: 10px;
}

.tech-item span {
  display: block;
  font-size: 1rem;
  font-weight: bold;
  color: #333;
}

/* Responsive Design for smaller screens */
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
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr)); /* Adjusted grid for small screens */
  }
}
</style>
