<template>
  <div class="container">
    <div class="loader">
      <div class="circle" style="--crl: #04fc43"></div>
      <div class="circle circle2" style="--crl: #fee800"></div>
      <div class="circle circle3" style="--crl: #ff00be"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loader {
  position: relative;
  width: 400px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;

  border-radius: 50%;
}

.circle {
  position: absolute;
  width: 300px;
  height: 300px;
  border: 2px solid #191919;
  border-radius: 50%;
  animation: animateCircle 3s linear infinite;
}

.circle2 {
  width: 200px;
  height: 200px;
  animation: animateCircle 6s linear infinite;
}

.circle3 {
  width: 100px;
  height: 100px;
  animation: animateCircle 2s linear infinite;
}

@keyframes animateCircle {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.circle::before {
  content: "";
  position: absolute;
  top: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: var(--crl);
  box-shadow: 0 0 20px var(--crl), 0 0 60px var(--crl);
}
</style>