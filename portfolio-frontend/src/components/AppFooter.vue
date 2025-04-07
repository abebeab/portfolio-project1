<template>
  <footer class="footer">
    <div class="footer-container">
      <!-- Centered Content -->
      <div class="center-content">
        <!-- Contact Info -->
        <div class="contact-info">
          <p class="contact-text">Email: <a href="mailto:abebetafere988@gmail.com">abebetafere988@gmail.com</a></p>
          <p class="contact-text">Location: Addis Ababa, Ethiopia</p>
        </div>

        <!-- Company Announcement -->
        <div class="company-announcement">
          <p class="company-name"><strong>Super Digital TECH</strong></p>
          <p class="coming-soon-text">🚀 Launching Soon! Stay tuned for the future !!</p>
        </div>
      </div>
       
      <!-- Social Links aligned top right -->
       
      <div class="footer-top-right">
        <p> Stay connected:</p> 
        <div class="social-links">
          <a href="https://www.linkedin.com/in/abebe-tafere-6176781a2/" target="_blank" class="social-icon">
            <img src="../assets/icons/linkedin-icon.jpg" alt="LinkedIn" />
          </a>
          <a href="https://t.me/ab_se7p" target="_blank" class="social-icon">
            <img src="../assets/icons/telegram-icon.jpg" alt="Telegram" />
          </a>
          <a href="https://github.com/abebeab" target="_blank" class="social-icon">
            <img src="../assets/icons/github-icon.jpg" alt="GitHub" />
          </a>
          <a href="https://www.upwork.com/freelancers/~01d347dbe89190526d?mp_source=share" target="_blank" class="social-icon">
            <img src="../assets/icons/upwork-icon.jpg" alt="Upwork" />
          </a>
        </div>
      </div>

      <!-- Footer Bottom Text -->
      <div class="footer-bottom">
        <p class="footer-text">
          &copy; 2025 All rights reserved. This portfolio is made with ❤️ by Abebe Tafere
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
}
</script>

<style scoped>
.footer {
  background: linear-gradient(135deg, #6a1b9a, #ff4081);
  color: #fff;
  text-align: center;
  width: 100%;
  padding-top: 20px;
  box-shadow: 0px -4px 10px rgba(0, 0, 0, 0.1);
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 10px 20px 20px;
  position: relative;
}

.center-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.contact-info {
  margin-bottom: 10px;
}

.contact-text {
  font-size: 1.1rem;
  margin: 5px 0;
}

.contact-text a {
  color: #fff;
  text-decoration: none;
}

.contact-text a:hover {
  text-decoration: underline;
}

.footer-top-right {
  display: flex;
  justify-content: flex-end;
  margin-top: 20px;
}

.social-links {
  display: flex;
  gap: 10px;
  align-items: center;
  margin-left: 20px;
}

.social-icon img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  transition: transform 0.3s ease;
}

.social-icon:hover img {
  transform: scale(1.2);
}

.footer-bottom {
  margin-top: 20px;
}

.footer-text {
  font-size: 1.1rem;
  font-weight: 600;
}

.company-announcement {
  margin-top: 20px;
  background-color: rgba(255, 255, 255, 0.2);
  padding: 20px;
  border-radius: 10px;
  text-align: center;
}

.company-name {
  font-size: 2rem;
  font-weight: bold;
  color: #007fff;
  text-transform: uppercase;
}

.coming-soon-text {
  font-size: 1.3rem;
  margin-top: 10px;
  color: #fff;
  font-style: italic;
  font-weight: 500;
  letter-spacing: 1px;
}

@media (max-width: 768px) {
  .footer-container {
    padding: 15px;
  }

  .footer-top-right {
    justify-content: center;
  }

  .social-links {
    flex-wrap: nowrap;
    flex-direction: row;
    flex-shrink: 1;
  }

  .social-icon img {
    width: 35px;
    height: 35px;
  }

  .company-name {
    font-size: 1.6rem;
  }

  .coming-soon-text {
    font-size: 1.1rem;
  }

  .footer-text {
    font-size: 1rem;
    padding-top: 10px;
  }
}
</style>
