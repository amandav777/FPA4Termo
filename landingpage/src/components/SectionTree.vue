<template>
  <div class="section-3">
    <div class="container-headsets">
      <div class="text-wrapper">
        <p class="subtitle-1">NEW PRODUCTS</p>
        <p class="body-2">Choose the headset that best suits your needs. We offer top-quality options with a variety of
          features to enhance your audio experience.</p>
      </div>

      <div class="card-wrapper">
        <div v-for="product in products" :key="product.id" class="product-card" :id="product.id">
          <div class="headset-details">
            <!-- image -->
            <div class="img">
              <img :src="hoveredProduct === product.id ? product.hoverImage : product.originalImage"
                @mouseover="hoveredProduct = product.id" @mouseleave="hoveredProduct = null" alt="Headset Image">
            </div>
            <!-- texts -->
            <p class="body-2">{{ product.title }}</p>
            <section class="price-detailer">
              <div class="pricing">
                <p class="body-1">$</p>
                <h6>{{ product.discountPrice }}</h6>
                <p class="body-3">{{ product.originalPrice }}</p>
              </div>
              <button class="btn-add-to-card">
                <p class="button-2">ADD TO CARD</p>
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

.subtitle-1 {
  color: #000;
  font-family: Inter;
  font-size: 2.25rem;
  font-style: normal;
  font-weight: 600;
  line-height: 2.75rem;
  letter-spacing: -0.09rem;
}

.body-1 {
  color: var(--Black-black-500, #000);
  font-family: Inter;
  font-size: 1.25rem;
  font-style: normal;
  font-weight: 400;
  line-height: 1.75rem;
  letter-spacing: -0.0125rem;
}

.body-2 {
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

.body-3 {
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

.button-2 {
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

.section-3 {
  border-radius: 30px;
  width: 1400px;
  height: 995px;
  max-width: 100%;
  margin: 0 auto;
  padding: 20px;
  position: relative;
}

.text-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  width: 42.25rem;
}

.container-headsets {
  background-color: #F3F5F9;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4rem;
  border-radius: 30px;
  padding: 10px 10px 20px;
  width: 1380px;
}


.card-wrapper {
  display: flex;
  align-items: center;
  gap: 3rem;
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

.headset-details {
  display: flex;
  width: fit-content;
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

.btn-add-to-card {
  display: flex;
  padding: 0.5rem 0.5rem 0.5rem 1.5rem;
  justify-content: center;
  align-items: center;
  gap: 1.875rem;
  border-radius: 2.5rem;
  border: 1px solid var(--White-white-700, #B5B5B5);
  background: var(--White-white-50, #FFF);
}

.btn-add-to-card:hover {
  border-color: 2px solid #000;
}

.price-detailer {
  display: flex;
  width: 16.8125rem;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
}


@media (max-width: 320px) {
  .section-3 {
    border-radius: 15px;
    width: 100%;
    height: auto;
    margin: 0;
    padding: 10px;
    position: relative;
  }

  .container-headsets {
    max-width: 100%;
    width: 100%;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
  }

  .card-wrapper {
    flex-direction: column;
    align-items: center;
    gap: 5rem;
    width: 100%;
    padding-bottom: 5px;
  }

  .img img {
    max-width: 70%;
    height: auto;
  }

  .img {
    display: flex;
    justify-content: center;
  }

  .headset-details {
    width: 300px;
    align-items: center;
    display: flex;
    justify-content: center;
    gap: 0.5rem;
    flex-wrap: wrap;
  }

  .pricing {
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .body-2 {
    display: flex;
    justify-content: center;
    padding: 5px;
  }

  .text-wrapper {
    max-width: 280px;
    align-items: center;
    gap: 0.5rem;
    text-align: center;
  }

  .btn-add-to-card:active {
    border: 2px solid #000;
  }
}


@media (max-width: 480px) {
  .section-3 {
    border-radius: 15px;
    width: 100%;
    height: auto;
    margin: 0;
    padding: 10px;
    position: relative;
  }

  .container-headsets {
    max-width: 100%;
    width: 100%;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
  }

  .card-wrapper {
    flex-direction: column;
    align-items: center;
    gap: 5rem;
    width: 100%;
    padding-bottom: 5px;
  }

  .img img {
    max-width: 90%;
    height: auto;
  }

  .img {
    display: flex;
    justify-content: center;
  }

  .headset-details {
    width: 70%;
    align-items: center;
    display: flex;
    justify-content: center;
    gap: 0.5rem;
    flex-wrap: wrap;
  }

  .pricing {
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .body-2 {
    display: flex;
    justify-content: center;
    padding: 5px;
  }

  .text-wrapper {
    max-width: 280px;
    align-items: center;
    gap: 0.5rem;
    text-align: center;
  }

}

@media (max-width: 1024px) {


  .section-3{
    display: flex;
    justify-content: center;
  }

  .container-headsets {
    width: 800px;
    padding: 40px;
    height: fit-content;
  }

  .card-wrapper {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    height: fit-content;
  }

  .headset-details {
    width: fit-content;
  }



}
</style>
