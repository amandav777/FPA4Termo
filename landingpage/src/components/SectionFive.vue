<template>
    <div class="container">
      <div class="product-main">
        <section class="product-img">
          <img src="../assets/images/product.png" alt="Main Product image" class="product-image">
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
            <button class="color-1-button" @click="toggleCheckIcon">
              <img src="../assets/icons/color1elipse.png" alt="Color option 1" class="color-circle">
              <img src="../assets/icons/checkmark.png" alt="Check icon" class="check-icon" style="display: none;">
            </button>
            <button class="color-2-button" @click="toggleCheckIcon">
              <img src="../assets/icons/color2elipse.png" alt="Color option 2" class="color-circle">
              <img src="../assets/icons/checkmark.png" alt="Check icon" class="check-icon" style="display: none;">
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
            <button type="button"><label for="button">SEE MORE DETAILS</label><img src="../assets/icons/arrowRight.png" alt=""></button>
          </div>
        </aside>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      toggleCheckIcon(event) {
        const clickedButton = event.currentTarget; 
        const buttons = document.querySelectorAll('.color-info button');
  
        buttons.forEach(button => {
          const checkIcon = button.querySelector('.check-icon');
          checkIcon.style.display = 'none'; 
        });
  
        const checkIcon = clickedButton.querySelector('.check-icon');
        checkIcon.style.display = 'block'; 
  
        const productImage = document.querySelector('.product-image');
        if (clickedButton.classList.contains('color-1-button')) {
            productImage.src = require('../assets/images/product.png');

        } else if (clickedButton.classList.contains('color-2-button')) {
            productImage.src = require('../assets/images/product2.png');
        }
      }
    }
  }
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
        gap: 80px;
        object-fit: cover;
    }

    .product-img{
        display: flex;
        padding-right: 153px;
        flex-direction: column;
        justify-content: flex-end;
        align-items: flex-start;
        gap: 113px;
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
    .product-rating {
        display: flex;
        gap: 24px;
    }
    .product-rating p{
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
        line-height: 28px; /* 140% */
        letter-spacing: -0.2px;
    }

    .check-icon {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 20px;
        height: 20px;
        display: none;
        background-color: transparent;
    }
    .color-1-button,.color-2-button{
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
        border-radius: 40px;
        border: 1px solid linear-gradient(to right, #CD43FF, #FD65A6,#FC9651,#FFBD72, #CD43FF);
    }
    .moredetails-button button{
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