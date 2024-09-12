<template>
    <!-- <div class="navbarMockada">
        trocar dps
    </div> -->

    <div class="heroSection">
        <div class="heroSectionContainer">
            <div class="alignHorizontal" style="gap: 80px;">
                <div class="leftContainer">
                    <h1>GABINI HEADSET STORE</h1>

                    <div class="ctaHeroSection">
                        <p class="subtitle1">Welcome to Gabini quality, at our most welcoming price.</p>
                        <button class="btnCta">
                            <p class="button1">SEE MORE DETAILS</p>
                            <img src="../assets/icons/arrowRight.png" alt="A right-oriented arrow">
                        </button>
                    </div>

                    <div class="alignHorizontal" style="gap: 3rem;">
                        <div class="rating">
                            <div class="alignHorizontal" style="gap: 0.75rem;">
                                <p class="subtitle3">4.8</p>
                                <img src="../assets/icons/star.png" alt="A star icon" id="star">
                            </div>
                            <p class="body3">2,290 ratings</p>
                        </div>

                        <div class="alignVertical">
                            <p class="subtitle2">10K+</p>
                            <p class="caption">Bought in past month</p>
                        </div>
                    </div>
                </div>

                <div class="rightContainer">
                    <div class="cardHeroSection">
                        <img src="../assets/images/headsetHero.png"
                            alt="A card with a beautiful headset and some information about it. It says: 2 years of warranty and 78 hours of battery.">

                        <div class="bubbleInfo" id="battery">
                            <img src="../assets/icons/battery.png" alt="A battery that lasts 78 hours!">
                            <section class="batteryInfo">
                                <p>Battery</p>
                                <h2>78 hours</h2>
                            </section>
                        </div>

                        <div class="bubbleInfo" id="warranty">
                            <img src="../assets/icons/medal.png" alt="2 years of warranty!">
                            <section class="warrantyInfo">
                                <p>Warranty</p>
                                <h2>2 years</h2>
                            </section>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style scoped>
/* assets de texto abaixo! :) */
h1 {
    color: var(--Black-black-500, #000);
    font-family: Inter;
    font-size: 6.25rem;
    font-style: normal;
    font-weight: 700;
    line-height: 5.625rem;
    letter-spacing: -0.25rem;
    text-transform: uppercase;
    width: 34rem;
    margin: 0;
}

.subtitle1 {
    color: var(--Base-100, #1F2026);
    font-family: Inter;
    font-size: 2.25rem;
    font-style: normal;
    font-weight: 600;
    line-height: 2.75rem;
    letter-spacing: -0.09rem;
    width: 29.0625rem;
}

.subtitle2 {
    color: var(--Black-black-500, #000);
    font-family: Inter;
    font-size: 1.875rem;
    font-style: normal;
    font-weight: 600;
    line-height: 2.375rem;
    letter-spacing: -0.01875rem;
    margin: 0;
}

.caption {
    color: var(--Black-black-500, #000);
    font-family: Inter;
    font-size: 0.875rem;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
}

.subtitle3 {
    color: var(--Black-black-500, #000);
    font-family: Inter;
    font-size: 1.5rem;
    font-style: normal;
    font-weight: 600;
    line-height: 1.875rem;
    letter-spacing: -0.03rem;
    margin: 0;
}

.body3 {
    color: var(--Black-black-200, #8A8A8A);
    font-family: Inter;
    font-size: 1rem;
    font-style: normal;
    font-weight: 400;
    line-height: 1.5rem;
    letter-spacing: -0.01rem;
}


.bubbleInfo {
    p {
        color: var(--Black-black-200, #8A8A8A);
        text-align: center;
        font-family: Inter;
        font-size: 1.125rem;
        font-style: normal;
        font-weight: 400;
        line-height: 1.75rem;
        letter-spacing: -0.01125rem;
        margin: 0;
    }

    h2 {
        color: var(--Black-black-500, #000);
        text-align: center;
        font-family: Inter;
        font-size: 1.25rem;
        font-style: normal;
        font-weight: 600;
        line-height: 1.625rem;
        letter-spacing: -0.0125rem;
        margin: 0;
    }
}


/* fim das assets de texto */
.heroSection {
    width: 100vw;
    height: 51.4375rem;
    flex-shrink: 0;
}

.ctaHeroSection {
    border-left: 1px solid #BFC0C2;
    width: fit-content;
    padding: 25px;
}

.btnCta {
    display: inline-flex;
    padding: 0.5rem 0.5rem 0.5rem 1.5rem;
    justify-content: center;
    align-items: center;
    gap: 1.875rem;
    border-radius: 2.5rem;
    border: 1px solid var(--White-white-700, #B5B5B5);
    background: var(--White-white-50, #FFF);
    color: var(--Black-black-500, #000);
}

.button1 {
    font-family: Inter;
    font-size: 0.875rem;
    font-style: normal;
    font-weight: 600;
    line-height: 1.5rem;
    letter-spacing: -0.00875rem;
    text-transform: uppercase;
}

.btnCta:hover {
    border: 1.5px solid #000;
}

.navbarMockada {
    width: 100vw;
    height: 5.9375rem;
    flex-shrink: 0;
    background-color: black;
}

.alignHorizontal {
    display: flex;
    flex-direction: row;
    width: fit-content;
}

.alignVertical {
    display: flex;
    justify-content: center;
    flex-direction: column;
}

#star {
    height: 28px;
}

.rating {
    width: fit-content;
}

.leftContainer {
    width: 34rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 700px;
}

.cardHeroSection {
    position: relative;
    width: 33.3125rem;
    height: 36.1875rem;
    flex-shrink: 0;
    border-radius: 1.875rem;
}

.heroSectionContainer {
    display: flex;
    justify-content: center;
    padding: 60px;
}

.bubbleInfo {
    position: absolute;
    display: flex;
    width: 16.25rem;
    padding: 1rem 1.25rem;
    align-items: center;
    gap: 1rem;
    border-radius: 3.75rem;
    background: var(--White-white-50, #FFF);
    box-shadow: 0px 24px 44px 0px rgba(226, 216, 239, 0.3);
}

#battery {
    bottom: 20px;
    left: 20px;
}

#warranty {
    top: 20px;
    right: 20px;
}

.batteryInfo {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 0.25rem;
}

.warrantyInfo {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 0.25rem;
}
</style>
