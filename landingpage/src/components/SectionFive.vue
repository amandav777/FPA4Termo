<template>
  <div class="container">
    <div class="product-main">
      <section class="product-img">
        <transition-group :name="animationDirection" tag="div" class="image-container">
          <img :src="currentImage" alt="Main Product image" class="product-image" :key="selectedColor">
        </transition-group>
      </section>
      <aside class="product-info">
        <h2>JBL Children's Bluetooth Headphones</h2>
        <div class="product-rating">
          <div class="rating-icons">
            <img src="../assets/icons/rating.png" alt="Star Rating 1">
            <img src="../assets/icons/rating.png" alt="Star Rating 2">
            <img src="../assets/icons/rating.png" alt="Star Rating 3">
            <img src="../assets/icons/rating.png" alt="Star Rating 4">
            <img src="../assets/icons/rating.png" alt="Star Rating 5">
          </div>
          <p>18,921 (reviews)</p>
        </div>
        <div class="color-info">
          <p>Color Options</p>
          <button 
            class="color-2-button" 
            :class="{ selected: selectedColor === 'color2' }" 
            @click="changeColor('color2')">
            <img src="../assets/icons/color2elipse.png" alt="Color option 2" class="color-circle">
            <img v-if="selectedColor === 'color2'" class="check-icon" src="../assets/icons/checkmark.png" alt="Selected">
          </button>
          <button 
            class="color-1-button" 
            :class="{ selected: selectedColor === 'color1' }" 
            @click="changeColor('color1')">
            <img src="../assets/icons/color1elipse.png" alt="Color option 1" class="color-circle">
            <img v-if="selectedColor === 'color1'" class="check-icon" src="../assets/icons/checkmark.png" alt="Selected">
          </button>
        </div>
        <div class="product-price">
          <div class="price-main">
            <span class="price-symbol">$</span>
            <span class="price-amount">28</span>
          </div>
          <div class="price-info">
            <span class="price-original">$35.99</span>
            <span class="discount-tag">22% off</span>
          </div>
        </div>
        <div class="moredetails-button">
          <button type="button">
            <label for="button">SEE MORE DETAILS</label>
            <img src="../assets/icons/arrowRight.png" alt="">
          </button>
        </div>
      </aside>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedColor: 'color2',  // Cor inicial
      images: {
        color1: require('../assets/images/product1.png'),
        color2: require('../assets/images/product2.png')
      },
      animationDirection: 'swap-down' // Define a animação inicial
    };
  },
  methods: {
    changeColor(color) {
      if (this.selectedColor !== color) {
        // Ajuste a animação com base na cor selecionada
        this.animationDirection = color === 'color1' ? 'swap-up' : 'swap-down';
        
        // Atualize a imagem correspondente
        this.currentImage = this.images[color];
        
        // Atualize a cor selecionada
        this.selectedColor = color;
      }
    }
  }
};
</script>

<style scoped>
:root {
  --Info-100: #17F;
  --Base-100: #1F2026;
}

.container {
  width: 1400px;
  height: 928px;
  border-radius: 30px;
  background: #F3F5F9;
}

.product-main {
  display: inline-flex;
  align-items: center;
  margin-left: 153px;
  gap: 80px;
}

.product-info {
  width: 450px;
  color: #000;
  font-family: Inter;
  font-size: 48px;
  font-style: normal;
  font-weight: 600;
  line-height: 56px;
  letter-spacing: -0.96px;
}
.product-info h2 {
  text-align: justify;
}
.product-img {
  position: relative;
  width: 300px;
  height: 300px;
}

.image-container {
  position: relative;
  height: 100%;
}

.product-image {
  position: absolute;
  max-width: 100%;
  height: auto;
  transition: transform 0.6s ;
}
/* Animação de subida (para Cor 1) */
.swap-up-enter-active, .swap-up-leave-active {
  transition: transform 0.6s ease-in-out;
}

.swap-up-enter-from {
  transform: translateY(100%); /* A nova imagem entra de baixo */
}

.swap-up-enter-to {
  transform: translateY(0); /* A nova imagem fica no centro */
}

.swap-up-leave-to {
  transform: translateY(-100%); /* A imagem atual sobe para fora da tela */
}

/* Animação de descida (para Cor 2) */
.swap-down-enter-active, .swap-down-leave-active {
  transition: transform 0.6s ease-in-out;
}

.swap-down-enter-from {
  transform: translateY(-100%); /* A nova imagem entra de cima */
}

.swap-down-enter-to {
  transform: translateY(0); /* A nova imagem fica no centro */
}

.swap-down-leave-to {
  transform: translateY(100%); /* A imagem atual desce para fora da tela */
}
.product-rating
{
  display: flex;
  align-items: center;
  gap: 6px;
}
.product-rating p {
  color: var(--Info-100, #17F);
  font-family: Inter;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
  letter-spacing: -0.16px;
}

.color-circle {
  border-radius: 50%;
  background-color: #E2E2E2;
}

.color-info {
  display: flex;
  align-items: center;
  gap: 24px;
  position: relative;
}

.color-info img {
  display: flex;
  align-items: flex-start;
  gap: 30px;
}

.color-info p {
  color: var(--Base-100, #1F2026);
  font-family: Inter;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 28px;
  letter-spacing: -0.2px;
}

.check-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 20px;
  height: 20px;
  background-color: transparent;
}

.color-1-button,.color-2-button {
  position: relative;
  border: none;
  padding: 0;
}

.product-price {
  display: flex;
  flex-direction: column;
  margin-top: 15px;
}

.price-main {
  display: flex;
  align-items: center;
  font-size: 60px;
  font-weight: 700;
}

.price-symbol {
  font-size: 24px;
  font-weight: 400;
  margin-right: 5px;
}

.price-amount {
  font-size: 90px;
}

.price-info {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 7px;
}

.price-original {
  font-size: 18px;
  text-decoration: line-through;
}

.discount-tag {
  display: flex;
  padding: 6px 14px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  position: relative;
  border-radius: 40px !important;
  border-image: linear-gradient(to right, #CD43FF, #FD65A6, #FC9651, #FFBD72, #CD43FF) 1 round;
  border-width: 2px;
  border-style: solid;
}

.moredetails-button button {
  display: flex;
  padding: 8px 8px 8px 24px;
  justify-content: center;
  align-items: center;
  gap: 30px;

  border-radius: 40px;
  border: 1px solid var(--White-white-700, #B5B5B5);
  background: var(--White-white-50, #FFF);
}

.moredetails-button label {
  color: var(--Black-black-500, #000);
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
  letter-spacing: -0.14px;
  text-transform: uppercase;
}
</style>
