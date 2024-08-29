<template>
    <div class="container">
        <div class="content">
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
                   <br> stories, events and more</p>
                <div class="inputWrapper">
                    <input type="email" placeholder="Email Address">
                    <img src="..\assets\icons\enterButton.png" alt="Submit Button">
                </div>
            </div>
        </div>
        <footer>
            <div class="rectangleBar">
                <ul>
                    <li><p>© 2024 Gabini Headset Store. - All Rights Reserved</p></li>
                    <li>PRODUCTS</li>
                    <li>PRIVACY POLICY</li>
                    <li>CUSTOMER SERVICES</li>
                    <li class="socialMedia"><img src="..\assets\icons\socialmedia.png" alt=""></li>
                </ul>
            </div>
            <div class="secondLogo">
                <img src="../assets/images/Logo_gabini_cinza.png" alt="Second Footer Logo">
            </div>
        </footer>
        </div>
       
    </div>
</template>

<script></script>

<style scoped>
.container {
    border-radius: 30px;
    background-color: black;
    max-width: 100%;
    margin: 0 auto;
    padding: 20px;
    position: relative;
}

.content {
    padding: 50px;
}

.mainTitle {
    padding: 10px;
    position: relative;
    width: 204px;
    height: 39px;
    margin-bottom: 20px;
}

.menuGrid {
    line-height: 24px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.menuGrid h2 {
    color: white;
    font-family: Inter, sans-serif;
    font-size: 20px;
    font-weight: 700;
}

.menuGrid p {
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 21px;
    text-align: justify;
    margin: 0;
}

.menuGrid ul {
    list-style-type: none;
    padding: 0;
}

.menuGrid ul li {
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 24px;
    text-align: justify;
}

.emailInput {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.emailInput p {
    text-align: justify;
}

.emailInput input[type="email"] {
    width: 100%;
    height: 40px;
    border-radius: 20px;
    border: 1px solid #767A85;
    background: #4B4B4B;
    color: white;
    padding: 0 50px 0 20px;
    box-sizing: border-box;
}

.inputWrapper {
    position: relative;
    width: 100%;
}

.inputWrapper input[type="email"] {
    width: 100%;
    height: 40px;
    border-radius: 20px;
    border: 1px solid #767A85;
    background: #4B4B4B;
    color: white;
    padding: 0 50px 0 20px;
    box-sizing: border-box;
}

.submitIcon {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%);
    width: 30px;
    height: 30px;
}

.secondLogo {
    width: 100%;
    max-width: 1233px;
    height: auto;
    z-index: 1;
    margin: 0 auto;
}

footer {
    position: relative;
}

.rectangleBar {
    background-color: black;
    color: #B0B0B0;
    font-family: Inter, sans-serif;
    font-size: 14px;
    text-align: center;
    width: 100%;
    z-index: 2;
    padding: 10px 0;
    box-sizing: border-box;
    position: absolute;
    bottom: 0;
}

.rectangleBar ul {
    display: flex;
    justify-content: center;
    gap: 20px;
    align-items: center;
    list-style-type: none;
    padding: 0;
    margin: 0;
}

.rectangleBar ul li:nth-child(2),
.rectangleBar ul li:nth-child(3),
.rectangleBar ul li:nth-child(4) {
    text-decoration: underline;
    font-weight: bold;
}

.socialMedia {
    display: inline-flex;
    padding: 10px;
    flex-direction: column;
    align-items: end;
    gap: 10px;
}
</style>
