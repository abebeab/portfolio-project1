<template>
  <section id="portfolio">
    <h2 class="section-title">My Portfolio</h2>
    <p class="section-description">Here are some of the projects I have worked on.</p>

    <!-- Colored buttons for filtering projects -->
    <div class="portfolio-buttons">
      <button class="portfolio-btn">All</button>
      <button class="portfolio-btn">CSS</button>
      <button class="portfolio-btn">HTML</button>
      <button class="portfolio-btn">JavaScript</button>
      <button class="portfolio-btn">Python</button>
      <button class="portfolio-btn">Java</button>
      <button class="portfolio-btn">Networking</button>
      <button class="portfolio-btn">Data Management</button>
      <button class="portfolio-btn">Kotlin</button>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PortfolioSection',
}
</script>

<style scoped>
/* Section Styling */
section#portfolio {
  margin-bottom: 40px;
  padding: 40px 20px;  /* Increase padding for more breathing room */
  min-height: 300px;
  background-color:#faf3db; /* Dark background for contrast */
  color: #fff; /* White text color */
  border-radius: 10px; /* Rounded corners */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Light shadow for depth */
}

h2.section-title {
  font-size: 3rem;
  font-weight: bold;
  text-align: center;
  color: #FF6347; /* A distinct color for the title */
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2); /* Subtle text shadow */
}

p.section-description {
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 20px;
  font-style: italic;
  color: #FF6347;
}

/* Buttons Styling */
.portfolio-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-top: 20px;
}

.portfolio-btn {
  padding: 12px 24px;
  font-size: 1.1rem;
  font-weight: bold;
  text-transform: uppercase; /* Make button text uppercase */
  border-radius: 8px;
  border: none;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add subtle shadow */
}

.portfolio-btn:hover {
  transform: scale(1.05); /* Slightly enlarge button on hover */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15); /* More prominent shadow on hover */
}

/* Colorful Buttons */
.portfolio-btn:nth-child(1) {
  background-color: #FF6347; /* Red */
}

.portfolio-btn:nth-child(2) {
  background-color: #FF9800; /* Orange */
}

.portfolio-btn:nth-child(3) {
  background-color: #FFD700; /* Yellow */
}

.portfolio-btn:nth-child(4) {
  background-color: #4CAF50; /* Green */
}

.portfolio-btn:nth-child(5) {
  background-color: #2196F3; /* Blue */
}

.portfolio-btn:nth-child(6) {
  background-color: #9C27B0; /* Purple */
}

.portfolio-btn:nth-child(7) {
  background-color: #3F51B5; /* Indigo */
}

.portfolio-btn:nth-child(8) {
  background-color: #009688; /* Teal */
}

.portfolio-btn:nth-child(9) {
  background-color: #607D8B; /* Blue-grey */
}

/* Responsive Design */
@media (max-width: 768px) {
  .portfolio-btn {
    padding: 10px 20px;
    font-size: 1rem;
  }
}
</style>
