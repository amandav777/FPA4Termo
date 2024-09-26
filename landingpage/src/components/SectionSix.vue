<template>
    <div class="testimonial-section">
        <h2>TESTIMONIALS</h2>
        <p>Voices of Satisfaction: Discover What Our Clients Have to Say</p>

        <div class="testimonial-container">
            <div class="testimonial-card" v-for="(testimonial, index) in testimonial" :key="index">
                <div class="stars">
                    <img src="../assets/icons/star.png" alt="">
                </div>
                <p>{{ testimonial.text }}</p>
                <div class="autor"></div>
            </div>
        </div>

    </div>
</template>

<script>
</script>

<style>

.testimonial-section{
    font-family: Inter;
    font-size: 36px;
    font-style: normal;
    font-weight: 600;
    line-height: 44px; /* 122.222% */
    letter-spacing: -1.44px;
    
}

</style>