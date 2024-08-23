<template>
  <div class="container">
    <div class="cardWrapper">
      <div v-for="(product) in products" :key="product.id" class="productCard" :id="product.id">
        <div class="productDetails">
          <!-- icon -->
          <img src="../assets/icons/boxIcon.png" alt="Box icon">
          <!-- texts -->
          <div class="weightDetails">
            <p class="body3">{{ product.itemWeightLabel }}</p>
            <p class="body2">{{ product.weight }}</p>
          </div>
        </div>
        <h4>{{ product.cta }}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  data() {
    return {
      products: [ 
        {
          id: 'blackHeadset',
          itemWeightLabel: 'Item Weight',
          weight: '2.6 Pounds',
          description: 'This is a great product!',
          cta: 'Find the perfect gifts'
        },
        {
          id: 'pinkHeadset',
          itemWeightLabel: 'Item Weight',
          weight: '2.6 Pounds',
          description: 'This is a great product!',
          cta: 'Find the perfect gifts'
        }
      ]
    };
  }
};
</script>

<style scoped>
.productCard {
  display: flex;
  width: 36.5rem;
  height: fit-content;
  padding: 1.5rem;
  flex-direction: column;
  align-items: flex-start;
  gap: 20.625rem;
  flex-shrink: 0;
  border-radius: 1.25rem;
  transition: all 300ms ease-out;

}


#pinkHeadset:hover,
#blackHeadset:hover {
  background-size: 130%;
  transition: 300ms;
  background-color: black;
}


#blackHeadset {
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.20) 0%, rgba(0, 0, 0, 0.20) 100%), url(../assets/images/blackHeadset.png) lightgray 50% / cover no-repeat;
}

#pinkHeadset {
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.20) 0%, rgba(0, 0, 0, 0.20) 100%), url(../assets/images/pinkHeadset.png) lightgray 50% / cover no-repeat;
}


.productDetails {
  display: flex;
  width: 14.125rem;
  padding: 0.875rem 1rem;
  align-items: center;
  gap: 1rem;
  border-radius: 3.5rem;
  background: rgba(0, 0, 0, 0.10);
  backdrop-filter: blur(27px);
}

/* assets de texto abaixo! :) */

.body2 {
  color: var(--White-white-50, #FFF);
  text-align: center;
  font-family: Inter;
  font-size: 1.125rem;
  font-style: normal;
  font-weight: 700;
  letter-spacing: -0.01125rem;
  margin: 0;
}

.body3 {
  color: var(--White-white-50, #FFF);
  font-family: Inter;
  font-size: 1rem;
  font-style: normal;
  font-weight: 400;
  line-height: 1.5rem;
  letter-spacing: -0.01rem;
  margin: 0;
}
h4 {
  color: var(--White-white-50, #FFF);
  font-family: Inter;
  font-size: 3.75rem;
  font-style: normal;
  font-weight: 600;
  line-height: 4.25rem;
  letter-spacing: -0.15rem;
  width: 24.3125rem;
}

/* fim das assets de texto */

.weightDetails {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  flex: 1 0 0;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.cardWrapper {
  display: inline-flex;
  flex-direction: row;
  gap: 2rem;
  flex-shrink: 0;
  
}
</style>
