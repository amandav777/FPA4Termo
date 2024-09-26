<template>
    <div class="navbar">
        <div class="navbar__logo">
            <img src="../assets/images/logo_g.png " alt="Logo">
        </div>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">Sale</a>
            <a href="#">Bundle & Save</a>

            <div class="dropdown" @click="toggleDropdown">
                <a href="#" class="dropbtn">
                    Shop By Category
                    <img :src="arrowImg" alt="Dropdown arrow" class="arrow" />
                </a>
                <div v-if="isDropdownOpen" class="dropdown-content">
                    <a href="#">Category 1</a>
                    <a href="#">Category 2</a>
                    <a href="#">Category 3</a>
                </div>
            </div>

            <a href="#">Support</a>
        </div>

        <div class="nav-actions">
            <a href="#">Sign In</a>
            <a href="#">Sign Up For Free</a>
        </div>


    </div>
</template>

<script>

export default{
    data() {
        return {
            isDropdownOpen: false,
            arrowImg: require('@/assets/icons/seta.png'),
        };
    },
    methods: {
        toggleDropdown() {
            this.isDropdownOpen = !this.isDropdownOpen;
        },
    },
};
</script>

<style scoped>
     body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            background-color: #fff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        /* Logo */
        .navbar img {
        width: 135px;
        height: 26px;
        flex-shrink: 0;
        margin-left: 20px;
        }

        .navbar .nav-links {
        color: var(--Black-black-500, #000);
        text-align: center;
        font-family: Inter;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 24px; 
        letter-spacing: -0.14px;
        text-transform: uppercase;
        }

        .navbar .nav-links a {
            text-decoration: none;
            color: #000;
            font-weight: bold;
            padding: 10px;
        }

        .navbar .nav-actions {
        color: var(--Black-black-500, #000);
        text-align: center;
        font-family: Inter;
        font-size: 14px;
        font-style: normal;
        font-weight: 600;
        line-height: 24px; 
        letter-spacing: -0.14px;
        display: flex;
        text-transform: uppercase;
        text-align: none;
        }

        .navbar .nav-actions a {
        color: var(--Black-black-500, #000);
        padding: 10px 20px;
        }

</style>