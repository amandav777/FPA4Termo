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
            <img src="../assets/icons/color1elipse.png" alt="Color option 2" class="color-circle">
            <img v-if="selectedColor === 'color2'" class="check-icon" src="../assets/icons/checkmark.png" alt="Selected">
          </button>
          <button 
            class="color-1-button" 
            :class="{ selected: selectedColor === 'color1' }" 
            @click="changeColor('color1')">
            <img src="../assets/icons/color2elipse.png" alt="Color option 1" class="color-circle">
            <img v-if="selectedColor === 'color1'" class="check-icon" src="../assets/icons/checkmark.png" alt="Selected">
          </button>
        </div>
        <div class="product-price">
          <div class="price-main">
            <div class="price-symbol">$</div>
            <span class="price-amount">28</span>
          </div>
          <div class="price-info">
            <span class="price-original">$35.99</span>
            <div class="discount-tag"><label for=""> 22% off</label></div>
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
    selectedColor: 'color1', // Cor inicial
    currentImage: require('../assets/images/product.png'), // Imagem inicial
    images: {
      color1: require('../assets/images/product.png'),
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

/* Container principal */
.container {
  max-width: 1400px;
  width: 100%;
  height: auto;
  border-radius: 30px;
  background: #F3F5F9;
  padding: 20px;
  display: flex; 
  justify-content: center; 
  align-items: center; 

}


/* Estrutura do produto */
.product-main {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  width: 100%;
  max-width: 1000px; 
}


/* Informações do produto */
.product-info {
  width: 100%;
  max-width: 450px;
  color: #000;
  font-family: Inter;
  font-size: 3rem; 
  font-weight: 600;
  text-align: left; 
}


.product-info h2 {
  text-align: justify;
}

/* Imagem do produto */
.product-img {
  width: 601px;
  height: 646px;
  overflow: hidden; /* Evita que a imagem saia do contêiner */
  position: relative;
}
.product-image {
  position: absolute;
  max-width: 100%; 
  max-height: 100%;
}
.image-container {
  position: relative;
  height: 100%;
  width: 100%;
  z-index: 5; 
}

/* Animações */
.swap-up-enter-active, .swap-up-leave-active {
  transition: transform 0.8s ease-in-out;
}
.swap-up-enter-from {
  transform: translateY(100%);
}
.swap-up-enter-to {
  transform: translateY(0);
}
.swap-up-leave-to {
  transform: translateY(-100%);
}

.swap-down-enter-active, .swap-down-leave-active {
  transition: transform 0.6s ease-in-out;
}
.swap-down-enter-from {
  transform: translateY(-100%);
}
.swap-down-enter-to {
  transform: translateY(0);
}
.swap-down-leave-to {
  transform: translateY(100%);
}

/* Avaliação do produto */
.product-rating {
  display: flex;
  align-items: center;
  gap: 6px;
}
.product-rating p {
  color: var(--Info-100, #17F);
  font-family: Inter;
  font-size: 16px;
  font-weight: 600;
  line-height: 24px;
  letter-spacing: -0.16px;
}

/* Opções de cores */
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
.color-1-button, .color-2-button {
  position: relative;
  border: none;
  padding: 0;
}

/* Preço do produto */
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
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 40px;
  border: 2px solid transparent;
  background-image: linear-gradient(#fff, #fff), linear-gradient(to right, #CD43FF, #FD65A6, #FC9651, #FFBD72, #CD43FF);
  background-origin: border-box;
  background-clip: content-box, border-box;
}
.discount-tag label {
  padding: 8px 24px; 
  font-size: 20px; 
  font-weight: 400;
}

/* Botão de mais detalhes */
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
  font-weight: 600;
  line-height: 24px;
  letter-spacing: -0.14px;
  text-transform: uppercase;
}
</style>
