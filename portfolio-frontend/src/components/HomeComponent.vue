<template>
  <!-- Brand Name Animation Section -->
  <section id="brand-animation">
    <div class="brand-animation">
      <p class="brand-text" id="brand-text">
        🚀 Super Digital Tec
      </p>
    </div>
  </section>

  <!-- Home Section -->
  <section id="home">
    <div class="home-container">
      <!-- Left side: Text content -->
      <div class="home-text">
        <p class="intro-text">
          Hey, I'm Abebe 👋
        </p>
        <p class="description">
          I build and design web interfaces.
        </p>
        <p class="services">
          I offer services in website development, mobile application development, networking, and IT support.
        </p>

        <!-- Work with me button -->
        <button @click="scrollToContact" class="work-button">Work with Me</button>

        <!-- Follow me on section -->
        <div class="follow-text">
          <p>Follow me on</p>
          <div class="social-links">
            <a href="https://www.linkedin.com/in/abebe-tafere-6176781a2/" target="_blank" class="social-icon">
              <img src="../assets/icons/linkedin-icon.jpg" alt="LinkedIn">
            </a>
            <a href="https://t.me/ab_se7p" target="_blank" class="social-icon">
              <img src="../assets/icons/telegram-icon.jpg" alt="Telegram">
            </a>
            <a href="https://github.com/abebeab" target="_blank" class="social-icon">
              <img src="../assets/icons/github-icon.jpg" alt="GitHub">
            </a>
            <a href="https://www.upwork.com/freelancers/~01d347dbe89190526d?mp_source=share" target="_blank" class="social-icon">
              <img src="../assets/icons/upwork-icon.jpg" alt="Upwork">
            </a>
          </div>
        </div>
      </div>

      <!-- Right side: Image -->
      <div class="home-image">
        <img src="@/assets/apprnt.jpg" alt="About Me" />
        
        <!-- Download Resume Button -->
        <button @click="downloadResume" class="download-button">
          <span>Download Resume</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    scrollToContact() {
      const contactSection = document.getElementById("contact");
      if (contactSection) {
        contactSection.scrollIntoView({ behavior: "smooth" });
      }
    },
    downloadResume() {
      const link = document.createElement('a');
      link.href = "https://drive.google.com/uc?export=download&id=1CdnQ_zm-tOCBuZ8cZbcikFKHjcFEZq1Z"; 
      link.download = 'Abebe_Resume.pdf'; 
      link.click(); 
    },
    startTypingEffect() {
      const brandTextElement = document.getElementById('brand-text');
      const text = "🚀 Super Digital Tec"; // Fixed text to type
      let i = 0;
      brandTextElement.textContent = ''; // Clear text initially

      // Function for typing effect with looping
      const typingInterval = () => {
        if (i < text.length) {
          brandTextElement.textContent += text[i];
          i++;
          setTimeout(typingInterval, 100); // Continue typing
        } else {
          setTimeout(() => {
            brandTextElement.textContent = ''; // Reset the text to empty
            i = 0; // Reset the index
            typingInterval(); // Restart typing after a delay
          }, 1000); // Adjust the delay before restarting (1 second)
        }
      };

      typingInterval(); // Start typing effect
    }
  },
  mounted() {
    this.startTypingEffect(); // Start the typing effect when the page is loaded
  }
};
</script>

<style scoped>
/* Base layout settings */
html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: 'Roboto', sans-serif;
}

#brand-animation {
  position: fixed;
  top: 15%;
  left: 50%;
  transform: translateX(-50%);
  z-index: 9990;
  text-align: center;
}

.brand-animation .brand-text {
  font-size: 2.5rem;
  font-weight: bold;
  text-transform: uppercase;
  white-space: normal;
  background: linear-gradient(90deg, #007bff, #00d2b7);
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
  display: inline-block;
  letter-spacing: 2px;
  overflow: hidden;
}

/* Home Section */
#home {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #f7f9fc;
  padding: 40px;
}

.home-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 1200px;
  gap: 30px;
  flex-wrap: wrap;
}

.home-text {
  flex: 1;
  text-align: left;
  padding: 20px;
}

.intro-text {
  font-size: 28px;
  color: #333;
  margin-bottom: 10px;
}

.description {
  font-size: 42px;
  font-weight: bold;
  color: #333;
  margin-bottom: 15px;
  line-height: 1.3;
}

.services {
  font-size: 18px;
  margin-bottom: 20px;
  color: #777;
}

.work-button {
  padding: 12px 20px;
  background-color: #4CAF50;
  color: white;
  font-size: 16px;
  border: none;
  cursor: pointer;
  border-radius: 4px;
  transition: background-color 0.3s ease;
}

.work-button:hover {
  background-color: #45a049;
}

.follow-text p {
  font-size: 18px;
  color: #333;
  margin-bottom: 10px;
}

.social-links {
  display: flex;
  gap: 15px;
}

.social-icon img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  transition: transform 0.3s ease;
}

.social-icon img:hover {
  transform: scale(1.2);
}

/* Image section */
.home-image {
  flex: 1;
  text-align: center;
  position: relative;
}

.home-image img {
  width: 100%;
  max-width: 400px;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.download-button {
  position: relative;
  bottom: -30px;
  right: 0;
  padding: 12px 20px;
  background-color: #007bff;
  color: white;
  border: none;
  font-size: 16px;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.download-button:hover {
  background-color: #0056b3;
}

/* Media Queries */
@media (max-width: 768px) {
  .home-container {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .home-text {
    text-align: center;
  }

  .intro-text {
    font-size: 22px;
  }

  .description {
    font-size: 32px;
  }

  .services {
    font-size: 16px;
  }

  .social-icon img {
    width: 40px;
    height: 40px;
  }

  .home-image img {
    width: 100%;
    max-width: 100%;
  }
}
</style>
