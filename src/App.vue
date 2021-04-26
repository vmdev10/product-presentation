<template>
  <div class="container">
    <div class="card">
      <img class="shoes" src="./assets/TENIS.svg" alt="Tênis" />
      <div class="shadow"></div>
    </div>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  width: 100%;
  height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;
}

.card {
  position: relative;

  width: 263px;
  height: 386px;

  background: #ffffff;
  box-shadow: 0px 4px 42px rgba(0, 0, 0, 0.25);
  border-radius: 16px 50px 16px 16px;
}

.shoes {
  position: absolute;
  top: -200px;
  right: -120px;

  z-index: 99;
}

.shadow {
  position: relative;
  width: 100%;
  height: 100%;

  border-radius: 16px 50px 16px 16px;
  overflow: hidden;
}

.shadow:after {
  content: "";

  position: absolute;
  top: -160px;
  left: -20px;
  width: 400px;
  height: 300px;

  background: linear-gradient(
    114.61deg,
    rgba(196, 196, 196, 0.3) -19.56%,
    rgba(196, 196, 196, 0) 120%
  );
  border-radius: 50%;
  transform: rotate(20deg);
}
</style>
