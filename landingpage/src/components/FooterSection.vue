<template>
    <div class="container">
        <div class="content">
            <div class="mainTitle">
                <img src="../assets/images/logo_gabini.png" alt="Footer Logo">
            </div>
            <div class="menuGrid">
                <section class="footerItemsGrid">
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
                        <li>Contact</li>
                        <li>Legal Mentions</li>
                    </ul>
                </div>
     
            </section>
            <aside class="emailInput">
                    <h2>Subscribe to newsletter</h2>
                    <p>Sign up for exclusive offers, original
                        <br> stories, events and more
                    </p>
                    <div class="inputWrapper">
                        <input type="email" placeholder="Email Address">
                        <img src="..\assets\icons\enterButton.png" alt="Submit Button" class="submitIcon">
                    </div>
                </aside>
            </div>
           
            <section class="footer">
                <div class="rectangleBar">
                    <ul>
                        <li>
                            <p>© 2024 Gabini Headset Store. - All Rights Reserved</p>
                        </li>
                        <li>PRODUCTS</li>
                        <li>PRIVACY POLICY</li>
                        <li>CUSTOMER SERVICES</li>
                        <li class="socialMedia"><img src="..\assets\icons\socialmedia.png" alt=""></li>
                    </ul>
                </div>
                <div class="secondLogo">
                    <img src="../assets/images/Logo_gabini_cinza.png" alt="Second Footer Logo">
                </div>
            </section>
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
    display: inline-flex;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 56px;  
}
.footerItemsGrid {
    display: inline-flex;
    align-items: flex-start;
    gap: 56px;
    
}   

.footerItemsGrid h2 {
    line-height: 24px;
    color: white;
    font-family: Inter, sans-serif;
    font-size: 20px;
    font-weight: 700;
}

.footerItemsGrid p {
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 21px;
    text-align: justify;
    margin: 0;
    gap: 24px;
    
}

.footerItemsGrid ul {
    list-style-type: none;
    padding: 0;
}

.footerItemsGrid ul li {
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 400;
    font-size: 14px;
    font-style: normal;
    line-height: 24px;
    text-align: justify;
}

.emailInput {
    display: inline-flex;
    flex-direction: column;
    align-items: flex-start;
    /* gap: 32px; */
}

.emailInput h2 {
    color: white;
    font-family: Inter, sans-serif;
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 10px;
}

.emailInput p {
    color: #B0B0B0;
    font-family: Inter;
    font-size: 14px;
    font-weight: 400;
    margin-bottom: 20px;
}

.inputWrapper {
    position: relative;
    width: 100%;
}

.emailInput input[type="email"] {
    width: 100%;
    height: 50px;
    border-radius: 25px;
    border: none;
    background: #4B4B4B;
    color: white;
    padding: 0 50px 0 20px;
    box-sizing: border-box;
    font-family: Inter, sans-serif;
    font-size: 16px;
}

.emailInput input[type="email"]::placeholder {
    color: #E0E0E0;
    opacity: 1;
}

.submitIcon {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%);
    width: 30px;
    height: 30px;
    cursor: pointer;
}

.secondLogo {
    width: 100%;
    max-width: 1233px;
    height: auto;
    z-index: 1;
    margin: 0 auto;
}

.footer {
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
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.rectangleBar ul {
    display: flex;
    justify-content: center;
    gap: 30px;
    align-items: center;
    list-style-type: none;
    padding: 0;
    margin: 0;
}

.rectangleBar ul li {
    text-align: center;
    margin-left: 20px;
}

.rectangleBar ul li:nth-child(2),
.rectangleBar ul li:nth-child(3),
.rectangleBar ul li:nth-child(4) {
    text-decoration: underline;
    font-weight: bold;
    margin-left: 10px;
    margin-right: 10px;
}

.rectangleBar ul li:first-child {
    margin-right: auto;
    margin-left: 0;
}

.rectangleBar ul li:last-child {
    margin-left: auto;
    margin-right: 0;
}

.socialMedia {
    display: inline-flex;
    padding: 10px;
    flex-direction: column;
    align-items: end;
    gap: 10px;
}

</style>
