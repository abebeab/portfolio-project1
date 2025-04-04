<template>
  <!-- Brand Name Animation (Placed Above Home Section) -->
  <section id="brand-animation">
    <div class="brand-animation">
      <p class="brand-text" id="brand-text">
        🚀 Super Digital Tec
      </p>
    </div>
  </section>

  <section id="home">
    <div class="home-container">
      <!-- Left side: Text content -->
      <div class="home-text">
        <p class="intro-text">
          Hey, I'm Abebe 👋
        </p>
        <p class="description">
          I build and design <br /> web interfaces
        </p>
        <p class="services">
          Work with me about website development, mobile application  <br />development,networking, and IT support services. I'm open to new projects!
        </p>

        <!-- Work with me button -->
        <p class="button-paragraph">
          <button @click="scrollToContact" class="work-button" aria-label="Scroll to contact section">Work with Me</button>
        </p>

        <!-- Follow me on section -->
        <p class="follow-text">
          Follow me on
        </p>

        <!-- Social links horizontally under Follow me on -->
        <div class="social-links">
          <a href="https://www.linkedin.com/in/abebe-tafere-6176781a2/" target="_blank" class="social-icon" aria-label="LinkedIn">
            <img src="../assets/icons/linkedin-icon.jpg" alt="LinkedIn">
          </a>
          <a href="https://t.me/ab_se7p" target="_blank" class="social-icon" aria-label="Telegram">
            <img src="../assets/icons/telegram-icon.jpg" alt="Telegram">
          </a>
          <a href="https://github.com/abebeab" target="_blank" class="social-icon" aria-label="GitHub">
            <img src="../assets/icons/github-icon.jpg" alt="GitHub">
          </a>
          <a href="https://www.upwork.com/freelancers/~01d347dbe89190526d?mp_source=share" target="_blank" class="social-icon" aria-label="Upwork">
            <img src="../assets/icons/upwork-icon.jpg" alt="Upwork">
          </a>
        </div>
      </div>

      <!-- Right side: Image -->
      <div class="home-image">
        <img src="@/assets/apprnt.jpg" alt="About Me" />

        <!-- Download Resume Button at the bottom-right corner -->
        <button @click="downloadResume" class="download-button" aria-label="Download Resume">
          <span>Download Resume</span>
        </button>
      </div>
    </div>
  </section>

  <!-- About Section (just an example for where to place your content) -->
  <section id="about">
    <!-- About content goes here -->
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
      // Trigger the download of the resume file
      const link = document.createElement('a');
      link.href = "https://drive.google.com/uc?export=download&id=1Nrh0r1eJ7HHIbhiZVSGA1Gtfxp7zcnfc";  // Correct Google Drive download link
      link.download = 'Abebe_Resume.pdf';  // Filename to be saved as
      link.click(); // Programmatically click to trigger the download
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
/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Brand Name Animation (Fixed in center with Blue-Green Gradient) */
#brand-animation {
  position: fixed;
  top: 15%;
  left: 0%;
  transform: translateX(5%);
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

/* Home section styling */
#home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 0px);
  width: 100%;
  background-color: #f0f4f8;
  margin-top: 30px;
  padding: 20px 0;
}

/* Container to hold content inside the home section */
.home-container {
  display: flex;
  justify-content: space-between; /* Space between the text and image */
  align-items: center;
  width: 80%;
  max-width: 1200px;
}

.home-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center; /* Center-align the text */
  gap: 10px; /* Reduced gap between the lines of text */
  margin-bottom: 10; /* Reduced margin to bring it closer */
}

.intro-text {
  font-size: 24px;
  margin-top: 150px; /* Adjusted margin for better spacing */
}

.description {
  font-size: 50px; /* Reduced size for a more compact look */
  font-weight: bold;
  font-family: 'Roboto', sans-serif;
  line-height: 1.2;
}

.services {
  font-size: 1.1rem;
  line-height: 1.6;
  margin-bottom: 20px;
  color: #333;
}

.work-button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
  margin-top: 10px; /* Reduced margin for less space */
}

.work-button:hover {
  background-color: #45a049;
}

/* Follow me on section */
.follow-text {
  margin-top: 10px; /* Reduced margin */
  font-size: 16px;
  margin-bottom: 10px; /* Reduced bottom margin */
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 10px; /* Reduced space between icons */
  margin-bottom: 100px;
}

.social-icon img {
  width: 60px; /* Reduced size for compactness */
  height: 60px; /* Reduced size for compactness */
  object-fit: cover;
  border-radius: 50%;
  transition: transform 0.3s ease;
}

.social-icon img:hover {
  transform: scale(1.2); /* Slightly smaller hover effect */
}

/* Image section styling */
.home-image {
  flex: 1;
  text-align: left;
  position: relative;
  
}

.home-image img {
  width: 60px; /* Reduced width */
  height: 400px; /* Reduced height */
  object-fit: cover;
  max-width: 0%;
  margin-left: 0px; /* Reduced margin for better balance */
  margin-top: 40px;
}

.download-button {
  position: absolute;
  bottom: -80px;
  right: -20px;
  padding: 5px 10px; /* Adjusted padding for compactness */
  font-size: 14px;
  background-color: #007bff;
  color: white;
  border: none;
  cursor: pointer;
}

.download-button:hover {
  background-color: #0056b3;
}

.download-button span {
  display: inline-block;
  line-height: 1.2;
}
</style>
