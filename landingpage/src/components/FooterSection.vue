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
        </div>
    </div>
</template>
<script></script>
<style scoped>
.container {
    border-radius: 30px;
    background-color: black;
    width: 1400px;
    height: 734px;
    flex-shrink: 0;
}
.mainTitle {
    display: flex;
    color: white;
    margin-bottom: 500px;
    margin-left: 100px;
} 
.menuGrid{
    display: flex;
    gap: 50px;

}  
.menuGrid h2{
    color: white;
    font-family: Inter;
    
}
.menuGrid ul{
    list-style-type: none;
    padding: 0;
}
.menuGrid ul li{
    color: #B0B0B0;
    font-family: Inter;
    font-weight: 240;
}
</style>