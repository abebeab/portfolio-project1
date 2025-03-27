<template>
  <footer class="footer">
    <p class="footer-text">&copy; 2025 My Portfolio. All rights reserved.</p>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',  // Multi-word component name
}
</script>

<style scoped>
.footer {
  background-color: #c4bfbf; /* Light gray background color */
  text-align: center;
  padding: 20px 0;
  position: relative; /* Ensures footer stays at the bottom without overlap */
  width: 100%;
}

/* Styling the text to be bold and dark */
.footer-text {
  font-size: 1.2rem; /* Optional: Adjust the font size for better visibility */
  font-weight: bold; /* Makes the text bold */
  color: #222; /* Dark color for the text */
  margin: 0;
  padding: 0;
}
</style>
