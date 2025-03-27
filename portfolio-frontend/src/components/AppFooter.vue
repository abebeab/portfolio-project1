<template>
  <footer class="footer">
    <p>&copy; 2025 My Portfolio. All rights reserved.</p>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',  // Multi-word component name
}
</script>

<style scoped>
.footer {
  background-color:#9f8170;
  color: white;
  text-align: center;
  padding: 10px 0;
  position: relative; /* Ensures footer stays at the bottom without overlap */
  width: 100%;
}
</style>
