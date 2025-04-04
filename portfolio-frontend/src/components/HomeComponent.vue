<template>
  <section id="home">
    <div class="home-container">
      <!-- Left side: Text content -->
      <div class="home-text">
        <p class="intro-text">
          Hey, I'm Abebe 👋
        </p>
        <p class="description">
          I build and design web interfaces
        </p>
        <p class="services">
          Work with me about website development, mobile application development, networking, and IT support services. I'm open to new projects!
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
    }
  }
};
</script>

<style scoped>
/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Home section styling */
#home {
  display: flex;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 0px); /* Adjust the height to avoid space for the header */
  width: 100%;
  background-color: #f0f4f8;
  margin-top: 150px; /* Increased space between the header and home section */
  padding: 20px 0;
}

/* Container to hold content inside the home section */
.home-container {
  display: flex;
  justify-content: center; /* Center the content horizontally */
  align-items: center; /* Center the content vertically */
  width: 80%; /* Set the container width */
  max-width: 1200px; /* Optional: Limit maximum width */
}

/* Styling for the text content */
.home-text {
  flex: 1; /* Allow the text to take up available space */
  padding-right: 20px;
  text-align: left; /* Align the text to the left */
}

.home-text p {
  margin-bottom: 20px;
  margin-left: 10px;
}

.intro-text {
  font-size: 24px;
}

.description {
  font-size: 50px;
  font-weight: bold;
  font-family: 'Roboto', sans-serif;
  line-height: 1.2;
  margin-bottom: 20px;
  margin-left: 20px;
}

.services {
  font-size: 16px;
}

/* Work with Me button styling */
.work-button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
  margin-left: 20px;
}

.work-button:hover {
  background-color: #45a049;
}

/* Follow me on section */
.follow-text {
  margin-top: 20px;
  font-size: 18px;
  margin-bottom: 20px; /* Add space after the text */
}

/* Social links and icons styling */
.social-links {
  display: flex;
  justify-content: flex-start; /* Align items to the left */
  gap: 20px; /* Space between the icons */
  margin-top: 10px;
}

.social-icon img {
  width: 70px; /* Increased size for the social icons */
  height: 70px; /* Increased height for the social icons */
  object-fit: cover;
  border-radius: 50%; /* Make the icons circular */
  transition: transform 0.3s ease; /* Smooth scaling on hover */
}

.social-icon img:hover {
  transform: scale(1.3); /* Scale up the icons on hover */
}

/* Image section styling */
.home-image {
  flex: 1; /* Allow the image to take up remaining space */
  text-align: left; /* Center the image */
  position: relative; /* Make sure the button is positioned relative to the image container */
  margin-right:10px;
}

/* Image Styling */
.home-image img {
  width: 500px; /* Increased width for the image */
  height: 300px; /* Set a fixed height for the image */
  object-fit: cover; /* Ensure the image covers the area without distorting */
  max-width: 100%; /* Ensure the image is responsive */
}

/* Download Resume button styling */
.download-button {
  position: absolute; /* Position the button absolutely relative to the image container */
  bottom: -50px; /* Position the button 20px from the bottom of the image */
  right: 20px; /* Position the button 20px from the right of the image */
  padding: 5px 5px; /* Adjusted padding for button height */
  font-size: 15px; /* Adjust text size */
  background-color: #007bff;
  color: white;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background-color 0.3s ease; /* Smooth transition */
}

/* Hover state for the button */
.download-button:hover {
  background-color: #0056b3; /* Darken the button on hover */
}

/* Text styling inside the button */
.download-button span {
  display: inline-block;
  line-height: 1.2;
}
</style>
