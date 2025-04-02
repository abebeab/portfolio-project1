  <template>
  <section id="contact">
    <!-- Top Section -->
    <h2 class="contact-title">Contact Me</h2>
    <p class="contact-description">Hey, you can contact me in any choice social media link or email me.</p>

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
        <form>
          <div class="form-inputs">
            <input type="text" placeholder="Your Name" required class="input-field" />
            <input type="email" placeholder="Your Email" required class="input-field" />
          </div>
          <textarea placeholder="Your Message" required></textarea>
          <button type="submit">Send Message</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
}
</script>
<style scoped>
/* Section Styling */
section#contact {
  margin-top: 10px; /* Reduced space between the top of the contact section and header */
  padding: 40px 10px;
  padding-top: 30px; /* Further reduced top padding for more compact space */
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 30px;
  position: relative;
  background-color: #f4f7fb; /* Light background color */
  border-radius: 10px; /* Rounded corners */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Optional: Light shadow */
}

/* Adjusting Scroll Behavior */
html {
  scroll-padding-top: 60px; /* Reduced padding to make the section appear closer to the header */
}

/* Ensure there's always space when navigating to the section */
section#contact {
  scroll-margin-top: 60px; /* Adjusted space when scrolling to the section */
}

/* Styling for the Title */
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

/* Bottom Section: Flex container for the info and form */
.contact-content {
  display: flex;
  justify-content: space-between;
  gap: 50px; /* Increased gap between the left and right sections */
  width: 100%;
  max-width: 960px;
  flex-wrap: wrap;
}

/* Bottom Left Section (Contact Info) */
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

/* Add Gap Between the Two Blocks */
.info-gap {
  margin-bottom: 30px; /* This adds the gap between the first and second block */
}

/* Bottom Right Section (Contact Form) */
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

/* Form Inputs and Textarea */
.form-inputs {
  display: flex;
  gap: 15px; /* Horizontal gap between the input fields */
}

.contact-form-right input,
.contact-form-right textarea,
.contact-form-right button {
  padding: 10px;
  border-radius: 5px;
  border: 2px solid #ddd; /* Increased border width */
  font-size: 1rem;
  width: 100%; /* Set width to 100% for all elements */
  box-sizing: border-box;
}

/* Textarea */
.contact-form-right textarea {
  height: 150px; /* Increased height for better proportion */
}

/* Button Styling */
.contact-form-right button {
  padding: 10px 20px;
  background-color: #e9967a;
  color: white;
  border: none;
  border-radius: 5px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  width: auto; /* Set button width to auto, matching the name input */
  max-width: 100%;
  margin-top: 10px;
  align-self: flex-start; /* Align button to match input fields */
}

.contact-form-right button:hover {
  background-color: #c67c56;
}

/* Responsive Design for Smaller Screens */
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
    width: 90%; /* Ensure form elements are wider on smaller screens */
  }
}

</style>
