<template>
  <div class="spinner">
    <div class="bar1"></div>
    <div class="bar2"></div>
    <div class="bar3"></div>
    <div class="bar4"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.spinner {
  display: inline-block;
  width: 80px;
  height: 80px;
}

.spinner .bar1,
.spinner .bar2,
.spinner .bar3,
.spinner .bar4 {
  width: 15px;
  height: 15px;
  background-color: #333;
  border-radius: 50%;
  display: inline-block;
  animation: spin 1.2s ease-in-out infinite;
}

.spinner .bar2 {
  animation-delay: 0.3s;
}

.spinner .bar3 {
  animation-delay: 0.6s;
}

.spinner .bar4 {
  animation-delay: 0.9s;
}

@keyframes spin {
  0%,
  100% {
    transform: translateY(0);
  }
  25% {
    transform: translateY(-20px);
  }
  50% {
    transform: translateY(0);
  }
  75% {
    transform: translateY(20px);
  }
}
</style>
