<template>
    <div class="section3">
      <div class="container">
        <div class="textWrapper">
          <p class="subtitle1">NEW PRODUCTS</p>
          <p class="body2">Choose the headset that best suits your needs. We offer top-quality options with a variety of features to enhance your audio experience.</p>
        </div>
        
        <div class="cardWrapper">
          <div v-for="product in products" :key="product.id" class="productCard" :id="product.id">
            <div class="headsetDetails">
              <!-- image -->
              <div class="img">
                <img :src="hoveredProduct === product.id ? product.hoverImage : product.originalImage"
                     @mouseover="hoveredProduct = product.id"
                     @mouseleave="hoveredProduct = null"
                     alt="Headset Image">
              </div>
              <!-- texts -->
              <p class="body2">{{ product.title }}</p>
              <section class="priceDetailer">
                <div class="pricing">
                  <p class="body1">$</p>
                  <h6>{{ product.discountPrice }}</h6>
                  <p class="body3">{{ product.originalPrice }}</p>
                </div>
                <button class="btnAddToCard">
                  <p class="button2">ADD TO CARDT</p>
                  <img src="../assets/icons/shopCart.png" alt="A shopping cart icon">
                </button>
              </section>
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
        hoveredProduct: null, 
        products: [
          {
            id: '1',
            title: 'Gabini® K-29 Premium Headset with Multi-Device Connectivity and Noise-Canceling Technology, Black.',
            discountPrice: '94.99',
            originalPrice: '$139.99',
            originalImage: require('@/assets/images/headset-section3-neutral.png'),
            hoverImage: require('@/assets/images/hoveredheadset-section3-neutral.png')
          },
          {
            id: '2',
            title: 'Gabini® K-29 Premium Headset with Multi-Device Connectivity and Noise-Canceling Technology, Black.',
            discountPrice: '94.99',
            originalPrice: '$139.99',
            originalImage: require('@/assets/images/headset-section3-neutral.png'),
            hoverImage: require('@/assets/images/hoveredheadset-section3-neutral.png')
          },
          {
            id: '3',
            title: 'Gabini® K-29 Premium Headset with Multi-Device Connectivity and Noise-Canceling Technology, Black.',
            discountPrice: '94.99',
            originalPrice: '$139.99',
            originalImage: require('@/assets/images/headset-section3-neutral.png'),
            hoverImage: require('@/assets/images/hoveredheadset-section3-neutral.png')
          }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* assets de texto abaixo! :) */
  
  .subtitle1 {
      color: #000;
      font-family: Inter;
      font-size: 2.25rem;
      font-style: normal;
      font-weight: 600;
      line-height: 2.75rem;
      letter-spacing: -0.09rem;
  }
  
  .body1 {
      color: var(--Black-black-500, #000);
      font-family: Inter;
      font-size: 1.25rem;
      font-style: normal;
      font-weight: 400;
      line-height: 1.75rem;
      letter-spacing: -0.0125rem;
  }
  
  .body2 {
      color: var(--Black-black-400, #333);
      text-align: center;
      font-family: Inter;
      font-size: 1.125rem;
      font-style: normal;
      font-weight: 400;
      line-height: 1.75rem;
      letter-spacing: -0.01125rem;
      align-self: stretch;
  }
  
  .body3 {
      color: var(--Alert-Colors-red, #E12237);
      font-family: Inter;
      font-size: 1rem;
      font-style: normal;
      font-weight: 400;
      line-height: 1.5rem;
      letter-spacing: -0.01rem;
      text-decoration: line-through;
  }
  
  h6 {
      color: var(--Black-black-500, #000);
      font-family: Inter;
      font-size: 2.5rem;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      letter-spacing: -0.1rem;
  }
  
  .button2 {
      color: var(--Black-black-500, #000);
      font-feature-settings: 'ss02' on;
      font-family: Inter;
      font-size: 0.75rem;
      font-style: normal;
      font-weight: 600;
      line-height: 1.5rem;
      letter-spacing: -0.0075rem;
      text-transform: uppercase;
  }
  
  /* fim das assets de texto */
  
  /* assets de alinhamento */
  
  .section3 {
      width: 87.5rem;
      height: 62.1875rem;
      flex-shrink: 0;
      border-radius: 1.875rem;
      background: #F3F5F9;
      justify-content: center;
      display: flex;
  }
  
  .textWrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      width: 42.25rem;
  }
  
  .container {
      display: flex;
      width: 75rem;
      flex-direction: column;
      align-items: center;
      gap: 5rem;
  }
  
  .cardWrapper {
      display: flex;
      align-items: center;
      gap: 9rem;
      align-self: stretch;
      flex-direction: row;
  }
  
  /* fim das assets de alinhamento */
  
  /* assets dos headsets */
  
  .img img {
      height: 20.4375rem;
      width: auto;
      transition: opacity 0.3s ease;
  }
  
  .headsetDetails {
      display: flex;
      width: 16.8125rem;
      flex-direction: column;
      align-items: center;
      gap: 1.5rem;
  }
  
  .pricing {
      display: flex;
      width: 12.125rem;
      height: 3rem;
      justify-content: center;
      align-items: center;
      gap: 4px;
  }
  
  .btnAddToCard {
      display: flex;
      padding: 0.5rem 0.5rem 0.5rem 1.5rem;
      justify-content: center;
      align-items: center;
      gap: 1.875rem;
      border-radius: 2.5rem;
      border: 1px solid var(--White-white-700, #B5B5B5);
      background: var(--White-white-50, #FFF);
  }

  .btnAddToCard:hover{
    border-color: #000;

  }
  
  .priceDetailer {
      display: flex;
      width: 16.8125rem;
      flex-direction: column;
      align-items: center;
      gap: 1.5rem;
  }
  
  </style>
  