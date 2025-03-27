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
          <button class="work-button">Work with Me</button>
        </p>

        <!-- Follow me on section -->
        <p class="follow-text">
          Follow me on
        </p>
        <div class="social-links">
          <!-- LinkedIn Link -->
          <a href="https://www.linkedin.com" target="_blank" class="social-icon">
            <img src="../assets/icons/linkedin-icon.jpg" alt="LinkedIn">
          </a>

          <!-- Telegram Link -->
          <a href="https://telegram.me" target="_blank" class="social-icon">
            <img src="../assets/icons/telegram-icon.jpg" alt="Telegram">
          </a>

          <!-- GitHub Link -->
          <a href="https://github.com" target="_blank" class="social-icon">
            <img src="../assets/icons/github-icon.jpg" alt="GitHub">
          </a>

          <!-- Upwork Link -->
          <a href="https://www.upwork.com" target="_blank" class="social-icon">
            <img src="../assets/icons/upwork-icon.jpg" alt="Upwork">
          </a>
        </div>
      </div>

      <!-- Right side: Image -->
      <div class="home-image">
        <img src="@/assets/apprnt.jpg" alt="About Me" />
        <!-- New Button: Get the Course -->
        <p class="course-button-paragraph">
          <button class="course-button">Get the Course</button>
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>
#home {
  display: flex;
  justify-content: center; /* Center the content horizontally */
  align-items: center; /* Center the content vertically */
  height: calc(100vh - 60px); /* Adjust the height to avoid space for the header */
  width: 100%;
  background-color: #f0f4f8; /* Set a different background color for the home section */
  margin-top: 0; /* Make sure no extra space exists between the header and this section */
  padding: 20px 0; /* Add padding for spacing */
}

.home-container {
  display: flex;
  justify-content: center; /* Center the content horizontally */
  align-items: center; /* Center the content vertically */
  width: 80%; /* Set the container width */
  max-width: 1200px; /* Optional: Limit maximum width */
}

.home-text {
  flex: 1; /* Allow the text to take up available space */
  padding-right: 20px;
  text-align: left; /* Align the text to the left */
}

.home-text p {
  margin-bottom: 20px;
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
}

.services {
  font-size: 16px;
}

.work-button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}

.work-button:hover {
  background-color: #45a049;
}

.follow-text {
  margin-top: 20px;
  font-size: 18px;
}

.social-links {
  display: flex;
  justify-content: center; /* Center social icons */
  gap: 20px; /* Increase space between icons */
  margin-top: 10px;
}

.social-icon img {
  width: 50px; /* Increase the width of the social icons */
  height: 50px; /* Increase the height of the social icons */
  object-fit: contain;
  transition: transform 0.3s ease; /* Smooth scaling on hover */
}

.social-icon img:hover {
  transform: scale(1.2); /* Scale up the icons on hover */
}

.home-image {
  flex: 1; /* Allow the image to take up remaining space */
  text-align: center; /* Center the image */
  position: relative; /* Make sure the button is positioned relative to the image container */
}

.home-image img {
  width: 500px; /* Increased width for the image */
  height: 300px; /* Set a fixed height for the image */
  object-fit: cover; /* Ensure the image covers the area without distorting */
  max-width: 100%; /* Ensure the image is responsive */
}

.course-button-paragraph {
  margin-top: 20px; /* Add space between the image and the button */
  text-align: center; /* Center the button */
}

.course-button {
  padding: 12px 25px;
  background-color: #007bff;
  color: white;
  border: none;
  font-size: 18px;
  cursor: pointer;
  border-radius: 5px;
  text-transform: uppercase;
}

.course-button:hover {
  background-color: #0056b3;
}
</style>
