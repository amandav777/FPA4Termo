<template>
    <div class="navbar-mockada">
        trocar dps
    </div>

    <div class="hero-section">
        <div class="hero-section-container">
            <div class="align-horizontal" style="gap: 80px;">
                <div class="left-container">
                    <h1>GABINI HEADSET STORE</h1>

                    <div class="cta-hero-section">
                        <p class="subtitle-1">Welcome to Gabini quality, at our most welcoming price.</p>
                        <button class="btn-cta">
                            <p class="button-1">SEE MORE DETAILS</p>
                            <img src="../assets/icons/arrowRight.png" alt="A right-oriented arrow">
                        </button>
                    </div>

                    <div class="align-horizontal" style="gap: 3rem;">
                        <div class="rating">
                            <div class="align-horizontal" style="gap: 0.75rem;">
                                <p class="subtitle-3">4.8</p>
                                <img src="../assets/icons/star.png" alt="A star icon" id="star">
                            </div>
                            <p class="body-3">2,290 ratings</p>
                        </div>

                        <div class="align-vertical">
                            <p class="subtitle-2">10K+</p>
                            <p class="caption">Bought in past month</p>
                        </div>
                    </div>
                </div>

                <div class="right-container">
                    <div class="card-hero-section">
                        <img src="../assets/images/headsetHero.png"
                            alt="A card with a beautiful headset and some information about it. It says: 2 years of warranty and 78 hours of battery.">

                        <div class="bubble-info" id="battery">
                            <img src="../assets/icons/battery.png" alt="A battery that lasts 78 hours!">
                            <section class="battery-info">
                                <p>Battery</p>
                                <h2>78 hours</h2>
                            </section>
                        </div>

                        <div class="bubble-info" id="warranty">
                            <img src="../assets/icons/medal.png" alt="2 years of warranty!">
                            <section class="warranty-info">
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

.subtitle-1 {
    color: var(--Base-100, #1F2026);
    font-family: Inter;
    font-size: 2.25rem;
    font-style: normal;
    font-weight: 600;
    line-height: 2.75rem;
    letter-spacing: -0.09rem;
    width: 29.0625rem;
}

.subtitle-2 {
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

.subtitle-3 {
    color: var(--Black-black-500, #000);
    font-family: Inter;
    font-size: 1.5rem;
    font-style: normal;
    font-weight: 600;
    line-height: 1.875rem;
    letter-spacing: -0.03rem;
    margin: 0;
}

.body-3 {
    color: var(--Black-black-200, #8A8A8A);
    font-family: Inter;
    font-size: 1rem;
    font-style: normal;
    font-weight: 400;
    line-height: 1.5rem;
    letter-spacing: -0.01rem;
}

.bubble-info {
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
.hero-section {
    width: 100vw;
    height: 51.4375rem;
    flex-shrink: 0;
}

.cta-hero-section {
    border-left: 1px solid #BFC0C2;
    width: fit-content;
    padding: 25px;
}

.btn-cta {
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

.button-1 {
    font-family: Inter;
    font-size: 0.875rem;
    font-style: normal;
    font-weight: 600;
    line-height: 1.5rem;
    letter-spacing: -0.00875rem;
    text-transform: uppercase;
}

.btn-cta:hover {
    border: 1.5px solid #000;
}

.navbar-mockada {
    width: 100vw;
    height: 5.9375rem;
    flex-shrink: 0;
    background-color: black;
}

.align-horizontal {
    display: flex;
    flex-direction: row;
    width: fit-content;
}

.align-vertical {
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

.left-container {
    width: 34rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 700px;
}

.card-hero-section {
    position: relative;
    width: 33.3125rem;
    height: 36.1875rem;
    flex-shrink: 0;
    border-radius: 1.875rem;
}

.hero-section-container {
    display: flex;
    justify-content: center;
    padding: 60px;
}

.bubble-info {
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

.battery-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 0.25rem;
}

.warranty-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 0.25rem;
}
</style>