<template>
    <div class="container">
        <div class="mainTitle">
            <img src="../assets/images/logo_gabini.png" alt="Footer Logo">
        </div>
        <div class="menuGrid">
            <div class="menuColumn">
                <h2>Menu</h2>
                <ul>
                    <li>Home</li>
                    <li>About us</li>
                    <li>Product</li>
                    <li>Pricing</li>
                </ul>
            </div>
            <div class="resourcesColumn">
                <h2>Resources</h2>
                <ul>
                    <li>Forum</li>
                    <li>Support</li>
                    <li>Partners</li>
                    <li>Events</li>
                </ul>
            </div>
            <div class="myAcountColumn">
                <h2>My Acount</h2>
                <ul>
                    <li>My Orders</li>
                    <li>Faq</li>
                    <li>Sales conditions</li>
                    <li>Legal Mentions</li>
                </ul>
            </div>
            <div class="emailInput">
                <h2>Subscribe to newsletter</h2>
                <p>Sign up for exclusive offers, original
                    stories, events and more</p>
                <button>Subscribe</button>
            </div>
        </div>
        <footer>
            <div class="rectangleBar">
                <ul>
                    <li><p>© 2024 Gabini Headset Store. - All Rights Reserved</p></li>
                    <li>PRODUCTS</li>
                    <li>PRIVACY POLICY</li>
                    <li>CUSTOMER SERVICES</li>
                </ul>
            </div>
            <div class="secondLogo">
                <img src="../assets/images/Logo_gabini_cinza.png" alt="Second Footer Logo">
            </div>
        </footer>
    </div>
</template>
<script></script>
<style scoped>

/* Fundo */
.container {
    border-radius: 30px;
    background-color: black;
    width: 1400px;
    height: 734px;
}

/* Logo 1 */
.mainTitle {
    position: relative;
    width: 204px;
    height: 39px;
    left: 80px;
    top:-50px;
} 

/* Seção de Menus */
.menuGrid{
    display: flex;
    position: relative;
    gap: 50px;
    top: 18px;
    left: 80px;

}  
.menuGrid h2{
    color: white;
    font-family: Inter;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: 28px;
    
    
}
.menuGrid p{
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 21px;
    text-align: justify;

}
.menuGrid ul{
    list-style-type: none;
    padding: 0;
}
.menuGrid ul li{
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 21px;
    text-align: justify;
}

/* Logo Maior / Segunda Logo */
.secondLogo {
    width: 1233px;
    height: 247px;
    top: 414px;
    left: 89px;
    opacity: 0.2;
}

/* Aquele reangulo em cima da segunda logo */
.rectangleBar {
    width: 1392px;
    height: 108px;
    flex-shrink: 0;
    color: #B0B0B0;
    font-family: Inter;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 22px; 
    letter-spacing: -0.14px;
}

.rectangleBar ul {
    display: flex;
    gap: 20px;
    align-items: center;
    list-style-type: none;
}
.rectangleBar ul li:nth-child(2),
.rectangleBar ul li:nth-child(3),
.rectangleBar ul li:nth-child(4) {
    text-decoration: underline;
    font-weight: bold;
}
</style>