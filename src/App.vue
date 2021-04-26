<template>
  <div class="container">
    <div class="card">
      <img class="burguer" src="./assets/burguer.png" alt="Hamburguer" />
      <div class="shadow"></div>
      <div class="card-content">
        <p class="subtitle">RETRO</p>
        <h3 class="title">BURGUER</h3>
      </div>
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

.burguer {
  width: 200px;
  height: 100px;
  position: absolute;
  top: 10px;
  right: -10px;

  z-index: 99;
}

.shadow {
  position: absolute;
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

.card-content {
  width: 100%;
  height: 100%;

  padding: 120px 20px 0;
}

.subtitle {
  font-family: 'Bebas Neue', cursive;
  font-size: 2rem;
  line-height: 17px;

}

.title {
  margin: 0.5rem 0;
  font-family: 'Bebas Neue', cursive;
  font-size: 2.5rem;
  line-height: 32px;
}
</style>
