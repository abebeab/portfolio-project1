<template>
  <section id="services">
    <!-- Top Text Section -->
    <h2 class="section-title">Services</h2>
    <p class="section-description">Here are the services I offer.</p>

    <!-- Centered Texts -->
    <div class="services-intro">
      <h3 class="services-heading">What I Do for Clients</h3>
      <p class="services-subheading">I give many services for clients.</p>
    </div>

    <!-- Service Boxes Section -->
    <div class="service-boxes">
      <!-- Web Design -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/web-design-icon.jpg" alt="Web Design" class="service-icon" />
          <h4 class="service-title">Web Design</h4>
          <p class="service-description">Creating visually appealing and user-friendly designs that engage users and enhance their browsing experience.</p>
        </div>
      </div>

      <!-- Web Development -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/web-development-icon.jpg" alt="Web Development" class="service-icon" />
          <h4 class="service-title">Web Development</h4>
          <p class="service-description">Developing fully functional websites and web applications tailored to your business needs.</p>
        </div>
      </div>
      
      <!-- Networking -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/networking-icon.jpg" alt="Networking" class="service-icon" />
          <h4 class="service-title">Networking</h4>
          <p class="service-description">Providing network solutions and ensuring robust and secure connectivity for businesses and clients.</p>
        </div>
      </div>

      <!-- SEO Optimization -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/seo-icon.jpg" alt="SEO" class="service-icon" />
          <h4 class="service-title">SEO Optimization</h4>
          <p class="service-description">Optimizing websites to rank higher on search engines and improve your online visibility.</p>
        </div>
      </div>

      <!-- Mobile App Development -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/mobile-app-icon.jpg" alt="Mobile App Development" class="service-icon" />
          <h4 class="service-title">Mobile App Development</h4>
          <p class="service-description">Building custom mobile applications for iOS and Android platforms to enhance user experience.</p>
        </div>
      </div>

      <!-- Graphic Design -->
      <div class="service-box">
        <div class="service-content">
          <img src="../assets/icons/graphic-design-icon.jpg" alt="Graphic Design" class="service-icon" />
          <h4 class="service-title">Graphic Design</h4>
          <p class="service-description">Creating visually appealing graphics and logos for branding, print media, and digital platforms.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ServicesSection',
}
</script>

<style scoped>
/* Section Styling */
section#services {
  padding: 40px 10px;
  min-height: 500px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #f4f7fb;
  margin-top: 20px; /* Increased gap between the top of the services section and header */
  scroll-margin-top: 40px; /* Ensures proper scroll behavior when jumping to this section */
}

/* Top Section Styling */
.section-title {
  font-size: 3rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
}

.section-description {
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 30px;
}

/* Centered Texts */
.services-intro {
  text-align: center;
  margin-bottom: 40px;
}

.services-heading {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.services-subheading {
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.services-description {
  font-size: 1.2rem;
  color: #555;
}

/* Service Boxes Section */
.service-boxes {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); /* Responsive grid */
  gap: 30px; /* Increased gap between boxes */
  max-width: 1000px;
  width: 100%;
  justify-items: center;
}

.service-box {
  background-color: #e9967a;
  padding: 20px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.service-box:hover {
  transform: scale(1.05); /* Slightly enlarge the box on hover */
}

/* Align Image Above Title with Gap */
.service-content {
  display: flex;
  flex-direction: column;
  align-items: center; /* Center align everything */
  gap: 15px; /* Gap between icon, title, and description */
}

.service-icon {
  width: 60px;
  height: 60px;
  margin-bottom: 10px; /* Space between icon and title */
  object-fit: contain;
}

.service-title {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 10px; /* Space between title and description */
}

.service-description {
  font-size: 1rem;
  color: #333;
}

/* Responsive Design */
@media (max-width: 768px) {
  .services-heading {
    font-size: 2rem;
  }

  .service-boxes {
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); /* Adjust grid for smaller screens */
  }

  .service-box {
    padding: 15px;
  }

  .service-icon {
    width: 50px;
    height: 50px;
  }

  .service-title {
    font-size: 1.3rem;
  }

  .service-description {
    font-size: 0.9rem;
  }
}
</style>
