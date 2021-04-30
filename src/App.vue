<template>
  <div class="container">
    <div class="card">
      <img class="burguer" src="./assets/burguer.png" alt="Hamburguer" />
      <div class="shadow"></div>
      <div class="card-content">
        <p class="subtitle">SPACE</p>
        <h3 class="title">BURGUER</h3>
        <span
          v-for="(composition, index) in checkedNames"
          :key="composition"
          class="description"
        >
          <span v-if="checkedNames.length - 1 == index">
            {{ composition }}
          </span>
          <span v-else> {{ composition + ", " }} </span>
        </span>
        <h4 class="price">R$16,00</h4>

        <div class="actions-container mt-4">
          <div class="accordion accordion-flush" id="accordionFlushExample">
            <div
              v-for="option in options"
              :key="option.label"
              class="accordion-item"
            >
              <h2 class="accordion-header" v-bind:id="'heading' + option.label">
                <button
                  class="accordion-button collapsed"
                  type="button"
                  data-bs-toggle="collapse"
                  v-bind:data-bs-target="'#' + option.label"
                  aria-expanded="false"
                  v-bind:aria-controls="'heading' + option.label"
                >
                  {{ option.label }}
                </button>
              </h2>
              <div
                v-bind:id="option.label"
                class="accordion-collapse collapse"
                v-bind:aria-labelledby="option.label"
                data-bs-parent="#accordionFlushExample"
              >
                <div class="accordion-body">
                  <div class="form-check">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      v-model="checkedNames"
                      :value="option.data"
                      v-bind:id="option.data"
                      checked
                    />
                    <label class="form-check-label" v-bind:for="option.data">
                      {{ option.data }}
                    </label>
                  </div>
                  <div class="form-check">
                    <input
                      class="form-check-input"
                      type="checkbox"
                      v-model="checkedNames"
                      :value="option.data2"
                      v-bind:id="option.data2"
                    />
                    <label class="form-check-label" v-bind:for="option.data2">
                      {{ option.data2 }}
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
      checkedNames: [],
      options: [
        { label: "Pães", data: "Pão Americano", data2: "Pão Integral" },
        { label: "Queijos", data: "Queijo Cheddar", data2: "Queijo Mussarela" },
        {
          label: "Carnes",
          data: "Dupla Carne Bovina",
          data2: "Pedações de Peito de Frango Empanado",
        },
        {
          label: "Molhos",
          data: "Molho Barbecue",
          data2: "Maionese Temperada",
        },
        { label: "Acompanhamentos", data: "Bacon", data2: "Calabresa" },
      ],
    };
  },
};
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

  font-size: 3rem;
  line-height: 17px;
}

.title {
  font-family: "Bebas Neue", cursive;
  color: rgb(255, 17, 0);

  margin: 1rem 0 1rem 0;

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
  background-image: url("./assets/plus-icon.svg");
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
