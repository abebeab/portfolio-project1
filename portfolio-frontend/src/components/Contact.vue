<template>
  <section id="contact">
    <!-- Top Section -->
    <h2 class="contact-title">Contact Me</h2>
    <p class="contact-description">Hey, you can contact me in any choice social media link or email me.</p>

    <!-- Success Message -->
    <div v-if="formSubmitted" class="success-message">
      Thank You, The Message Submitted Successfully!
    </div>

    <!-- Bottom Section with Left Info and Right Form -->
    <div class="contact-content">
      <!-- Left Section: Contact Information -->
      <div class="contact-info-left">
        <!-- First Block: Message Info -->
        <div class="info-item">
          <img src="../assets/icons/message-icon.jpg" alt="Message Icon" class="icon" />
          <span>Have a question?</span>
        </div>
        <div class="info-item">
          <span>I am here to help you</span>
        </div>
        <div class="info-item">
          <span>Email me at <a href="mailto:abebetafere988@gmail.com">abebetafere988@gmail.com</a></span>
        </div>

        <!-- Add Gap Between Two Blocks -->
        <div class="info-gap"></div>

        <!-- Second Block: Location Info -->
        <div class="info-item">
          <img src="../assets/icons/location-icon.jpg" alt="Location Icon" class="icon" />
          <span>Current Location: Addis Ababa, Ethiopia</span>
        </div>
        <div class="info-item">
          <span>Serving Clients Worldwide!</span>
        </div>
      </div>

      <!-- Right Section: Contact Form -->
      <div class="contact-form-right">
        <form @submit.prevent="handleSubmit">
          <div class="form-inputs">
            <input type="text" v-model="name" placeholder="Your Name" required class="input-field" />
            <input type="email" v-model="email" placeholder="Your Email" required class="input-field" />
          </div>
          <textarea v-model="message" placeholder="Your Message" required></textarea>
          <button type="submit">Send Message</button>
        </form>
      </div>
    </div>

    <!-- Home Page Button (Right Corner) -->
    <div class="scroll-to-home" @click="goToHome">
      <i class="fa fa-home"></i> <!-- FontAwesome Home Icon -->
      <!-- Bullet Indicator -->
      <div class="bullet"></div>
    </div>
    
    <!-- MENU Text for Developer Tools (Invisible on the Page) -->
    <!-- MENU: This section contains the icons for "Contact" and Home page navigation -->
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      name: '',
      email: '',
      message: '',
      formSubmitted: false, // To track if form is submitted
    };
  },
  methods: {
    goToHome() {
      window.location.href = '/'; // This will redirect to the home page
    },
    handleSubmit() {
      // Here, you would typically send the form data to your server or API.
      // For this example, we just simulate a successful submission.

      // Reset the form values
      this.name = '';
      this.email = '';
      this.message = '';

      // Set formSubmitted to true to show the success message
      this.formSubmitted = true;

      // Hide the success message after 3 seconds
      setTimeout(() => {
        this.formSubmitted = false;
      }, 3000); // 3 seconds
    },
  },
};
</script>

<style scoped>
/* Section Styling */
section#contact {
  margin-top: 10px;
  padding: 40px 10px;
  padding-top: 30px;
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 30px;
  position: relative;
  background-color: #f4f7fb;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

/* Success Message Styling */
.success-message {
  font-size: 1.5rem;
  color: green;
  background-color: #d4edda;
  border: 1px solid #c3e6cb;
  padding: 10px;
  border-radius: 5px;
  margin-bottom: 20px;
  text-align: center;
  animation: showMessage 0.5s ease-in-out; /* Animation for a smooth appearance */
}

/* Show Message Animation */
@keyframes showMessage {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

/* Adjusting Scroll Behavior */
html {
  scroll-padding-top: 60px;
}

section#contact {
  scroll-margin-top: 60px;
}

.contact-title {
  font-size: 3rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
}

.contact-description {
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.contact-content {
  display: flex;
  justify-content: space-between;
  gap: 50px;
  width: 100%;
  max-width: 960px;
  flex-wrap: wrap;
}

.contact-info-left {
  flex: 1;
  padding: 20px;
}

.info-item {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.info-item span {
  font-size: 1.2rem;
  color: #333;
  margin-left: 10px;
}

.info-item a {
  color: #e9967a;
  text-decoration: none;
}

.info-item .icon {
  width: 20px;
  height: 20px;
  margin-right: 10px;
}

.info-gap {
  margin-bottom: 30px;
}

.contact-form-right {
  flex: 1;
  padding: 20px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.contact-form-right form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form-inputs {
  display: flex;
  gap: 15px;
}

.contact-form-right input,
.contact-form-right textarea,
.contact-form-right button {
  padding: 10px;
  border-radius: 5px;
  border: 2px solid #ddd;
  font-size: 1rem;
  width: 100%;
  box-sizing: border-box;
}

.contact-form-right textarea {
  height: 150px;
}

.contact-form-right button {
  padding: 10px 20px;
  background-color: #e9967a;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  width: auto;
  max-width: 100%;
  margin-top: 10px;
  align-self: flex-start;
}

.contact-form-right button:hover {
  background-color: #c67c56;
}

/* Home Page Button Styling */
.scroll-to-home {
  position: fixed; /* Fixed position in the right corner */
  bottom: 30px;
  right: 30px;
  background-color: #e9967a;
  color: white;
  border: none;
  border-radius: 50%;
  padding: 15px;
  font-size: 2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  z-index: 10; /* Ensure it's above all content */
}

.scroll-to-home:hover {
  background-color: #c67c56;
}

.scroll-to-home i {
  font-size: 2rem; /* FontAwesome Home Icon Size */
}

/* Bullet Indicator */
.scroll-to-home .bullet {
  position: absolute;
  top: -5px;
  right: -5px;
  width: 10px;
  height: 10px;
  background-color: #ff4500; /* Red color for bullet */
  border-radius: 50%;
  transition: transform 0.2s ease-in-out;
}

/* Bullet Animation on Hover */
.scroll-to-home:hover .bullet {
  transform: scale(1.2);
}

/* Responsive Design */
@media (max-width: 768px) {
  section#contact {
    flex-direction: column;
    align-items: center;
  }

  .contact-content {
    flex-direction: column;
    align-items: center;
  }

  .contact-info-left {
    margin-bottom: 30px;
  }

  .contact-form-right {
    width: 100%;
  }

  .contact-form-right input,
  .contact-form-right textarea,
  .contact-form-right button {
    width: 90%;
  }
}
</style>
