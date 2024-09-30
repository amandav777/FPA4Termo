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
    selectedColor: 'color1', 
    currentImage: require('../assets/images/product.png'), 
    images: {
      color1: require('../assets/images/product.png'),
      color2: require('../assets/images/product2.png')
    },
    animationDirection: 'swap-down' 
  };
},
  methods: {
    changeColor(color) {
      if (this.selectedColor !== color) {
        this.animationDirection = color === 'color1' ? 'swap-up' : 'swap-down';
        
        this.currentImage = this.images[color];
        
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
  max-width: 87.5rem; 
  width: 100%;
  height: auto;
  border-radius: 1.875rem; 
  background: #F3F5F9;
  padding: 1.25rem; 
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
  height: auto;
  width: 100%;
  max-width: 1000px; 
  min-height: 646px; 
  padding-top: 141px; 
  padding-bottom: 141px; 

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
  color: #000;
  font-family: Inter;
  font-size: 3rem; 
  font-weight: 600;
  text-align: left; ;
}

/* Imagem do produto */
.product-img {
  width: 37.563rem;
  height: 40.375rem;
  overflow: hidden;
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
  transition: transform 0.4s ease-in-out;
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
  transition: transform 0.4s ease-in-out;
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
  gap: 0.375rem;
}
.product-rating p {
  color: var(--Info-100, #17F);
  font-family: Inter;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.5rem;
}

/* Opções de cores */
.color-circle {
  border-radius: 50%;
}
.color-info {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  position: relative;
}
.color-info img {
  display: flex;
  align-items: flex-start;
  gap: 1.875rem;
}
.color-info p {
  color: var(--Base-100, #1F2026);
  font-family: Inter;
  font-size: 1.25rem;
  font-weight: 400;
  line-height: 1.75rem;
}
.color-info button {
  background-color: #F3F5F9;
}
.check-icon {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 1.25rem;
  height: 1.25rem;
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
  flex-direction: row;
  align-items: center;
  margin-top: 0.938rem;
  gap: 0.625rem;
  position: relative;
}
.price-main {
  display: flex;
  align-items: center;
  font-size: 3.75rem;
  font-weight: 700;
}
.price-symbol {
  font-size: 1.5rem;
  font-weight: 700;
  margin-right: 0.313rem;
  align-self: start;
  top: 0;
  left: 0;
}
.price-amount {
  font-size: 5.625rem;
}
.price-info {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.438rem;
}
.price-original {
  font-size: 1.5rem;
  text-decoration: line-through;
  font-weight: 700;
}

.discount-tag {
  position: relative;
  display: flex;
  justify-content: center;
  border-radius: 2.5rem;
  border: 2px solid transparent;
  background-image: linear-gradient(#fff, #fff), linear-gradient(to right, #CD43FF, #FD65A6, #FC9651, #FFBD72, #CD43FF);
  background-origin: border-box;
  background-clip: content-box, border-box;
}
.discount-tag label {
  gap: 0.625rem;
  padding: 0.5rem 1.5rem; 
  font-size: 1.25rem; 
  font-weight: 700;
}

.moredetails-button {
  margin-top: 2rem;
}

/* Botão de mais detalhes */
.moredetails-button button {
  display: flex;
  padding: 0.75rem 1.5rem; 
  justify-content: space-between; 
  align-items: center;
  gap:1.875rem;
  border-radius: 40px;
  border: 1px solid #B5B5B5;
  background-color: #FFF;
  cursor: pointer;
}
.moredetails-button label {
  color: var(--Black-black-500, #000);
  font-size: 0.875rem;
  font-weight: 600;
  line-height: 1.5rem;
  text-transform: uppercase;
}
/* Responsavidade */
@media (max-width: 768px) {
  .product-main {
    padding-top: 80px; 
    padding-bottom: 80px; 
  }
}

</style>
