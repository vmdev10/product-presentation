<template>
  <div class="container">
    <div class="card">
      <img class="burguer" src="./assets/burguer.png" alt="Hamburguer" />
      <div class="shadow"></div>
      <div class="card-content">
        <p class="subtitle">SPACE</p>
        <h3 class="title">BURGUER</h3>
        <h4 class="description">
          {{ checkedNames }}
        </h4>
        <h4 class="price">R$16,00</h4>

        <div class="actions-container mt-4">
          <div class="accordion accordion-flush" id="accordionFlushExample">
            <div class="accordion-item">
              <h2 class="accordion-header" id="flush-headingOne">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#flush-collapseOne"
                  aria-expanded="false"
                  aria-controls="flush-collapseOne"
                >
                  Pães
                </button>
              </h2>
              <div
                id="flush-collapseOne"
                class="accordion-collapse collapse"
                aria-labelledby="flush-headingOne"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" value="Pão Americano" id="american" checked>
                    <label class="form-check-label" for="american">
                      Pão Americano
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" value="Pão Integral" id="integral">
                    <label class="form-check-label" for="integral">
                      Pão Integral
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="accordion-item">
              <h2 class="accordion-header" id="flush-headingTwo">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#flush-collapseTwo"
                  aria-expanded="false"
                  aria-controls="flush-collapseTwo"
                >
                  Queijos
                </button>
              </h2>
              <div
                id="flush-collapseTwo"
                class="accordion-collapse collapse"
                aria-labelledby="flush-headingTwo"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                    <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="cheddar" value="Queijo Cheddar" checked>
                    <label class="form-check-label" for="cheddar">
                      Queijo Cheddar
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="mussarela" value="Queijo Mussarela">
                    <label class="form-check-label" for="mussarela">
                      Queijo Mussarela
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="accordion-item">
              <h2 class="accordion-header" id="flush-headingThree">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#flush-collapseThree"
                  aria-expanded="false"
                  aria-controls="flush-collapseThree"
                >
                  Carnes
                </button>
              </h2>
              <div
                id="flush-collapseThree"
                class="accordion-collapse collapse"
                aria-labelledby="flush-headingThree"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="beef" value="Carne Bovina" checked>
                    <label class="form-check-label" for="beef">
                      Carne Bovina
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="chicken" value="Peito De Frango Empanado">
                    <label class="form-check-label" for="chicken">
                      Peito De Frango Empanado
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="accordion-item">
              <h2 class="accordion-header" id="flush-headingFour">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#flush-collapseFour"
                  aria-expanded="false"
                  aria-controls="flush-collapseFour"
                >
                  Molhos
                </button>
              </h2>
              <div
                id="flush-collapseFour"
                class="accordion-collapse collapse"
                aria-labelledby="flush-headingFour"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="barbecue" value="Molho Barbecue" checked>
                    <label class="form-check-label" for="barbecue">
                      Molho Barbecue
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="mayonnaise" value="Maionese Temperada">
                    <label class="form-check-label" for="mayonnaise">
                      Maionese Temperada
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="accordion-item">
              <h2 class="accordion-header" id="flush-headingFive">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  data-bs-target="#flush-collapseFive"
                  aria-expanded="false"
                  aria-controls="flush-collapseFive"
                >
                  Adicionais
                </button>
              </h2>
              <div
                id="flush-collapseFive"
                class="accordion-collapse collapse"
                aria-labelledby="flush-headingFive"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="sausage" value="Calabresa" checked>
                    <label class="form-check-label" for="sausage">
                      Calabresa
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="bacon" value="Bacon">
                    <label class="form-check-label" for="bacon">
                      Bacon
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="onion" value="Cebola Caramelizada">
                    <label class="form-check-label" for="onion">
                      Cebola Caramelizada
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="lettuce" value="Alface">
                    <label class="form-check-label" for="lettuce">
                      Alface
                    </label>
                  </div>
                  <div class="form-check">
                    <input class="form-check-input" type="checkbox" v-model="checkedNames" id="tomato" value="Tomate">
                    <label class="form-check-label" for="tomato">
                      Tomate
                    </label>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checkedNames: []
    }
  },
  methods: {
    isChecked() {

    }
  }
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

@keyframes float {
  0%,
  100% {
    transform: translatey(0);
  }
  50% {
    transform: translatey(-20px);
  }
}
.burguer {
  animation: float 6s ease-in-out infinite;
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

  width: 19rem;
  height: auto;

  padding: 2rem 0 3.5rem 0;

  background: #ffffff;
  box-shadow: 0px 4px 42px rgba(0, 0, 0, 0.25);
  border-radius: 16px 50px 16px 16px;
}

.burguer {
  width: 220px;
  height: 120px;
  position: absolute;
  top: 12px;
  right: -10px;

  transform: rotate(20deg);
  z-index: 99;
}

.shadow {
  position: absolute;
  width: 100%;

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
  font-family: "Bebas Neue", cursive;
  color: rgb(255, 17, 0);

  font-size: 2.5rem;
  line-height: 17px;
}

.title {
  font-family: "Bebas Neue", cursive;
  color: rgb(255, 17, 0);

  margin: 0.5rem 0 1rem 0;

  font-size: 3rem;
  line-height: 32px;
}

.description {
  font-family: "Bebas Neue", cursive;
  font-size: 0.8rem;
  font-weight: 400;
  color: rgb(255, 174, 0);
}

.price {
  font-family: "Bebas Neue", cursive;
  font-size: 1.5rem;
  margin-top: 0.5rem;
  text-align: right;
  color: rgb(255, 17, 0);
}

.accordion-button {
  font-size: 0.8rem;
}

.accordion-button::after {
  background-image: url('./assets/plus-icon.svg');
  background-size: 0.8rem;
  background-repeat: no-repeat;
}

.accordion-item {
  padding: 0.5rem 0;
}

.accordion-collapse {
  margin-left: 1rem;
}

.accordion-body {
  font-size: 0.8rem;
  padding: 0.5rem 0;
}
</style>
