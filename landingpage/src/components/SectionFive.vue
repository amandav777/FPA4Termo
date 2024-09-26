<template>
 <div class="container">
    <div class="product-main">
        <section class="product-img">
            <img src="..\assets\images\product.png" alt="Main Product image" class="product-image">
        </section>
        <aside class="product-info">
            <h2>JBL Children's Bluetooth Headphones</h2>
            <div class="rating-icons">
                <img src="../assets/icons/rating.png" alt="">
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
        display: flex;
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
        line-height: 56px; /* 116.667% */
        letter-spacing: -0.96px;
    }
</style>