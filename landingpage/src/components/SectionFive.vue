<template>
 <div class="container">
    <div class="product-main">
        <section class="product-img">
            <img src="..\assets\images\product.png" alt="Main Product image" class="product-image">
        </section>
        <aside class="product-info">
            <h2>JBL Children's Bluetooth Headphones</h2>
            <div class="product-rating">
                <div class="rating-icons">
                    <img src="../assets/icons/rating.png" alt="Star Raing 1">
                    <img src="../assets/icons/rating.png" alt="Star Raing 2">
                    <img src="../assets/icons/rating.png" alt="Star Raing 3">
                    <img src="../assets/icons/rating.png" alt="Star Raing 4">
                    <img src="../assets/icons/rating.png" alt="Star Raing 5">
                </div>
                <p>18,921 (reviews)</p>
            </div>
            <div class="color-info">
                <p>Color options</p>
                <img src="../assets/icons/color2elipse.png" alt=""><img src="../assets/icons/color1elipse.png" alt="">
            </div>
            <div class="product-price">
                <p></p>
            </div>
        </aside>
    </div>
 </div>
</template>
<style scoped>

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
    .color-info {
        display: flex;
        align-items: center;
        gap: 24px;
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
    .product-price {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 7px;
    }
</style>