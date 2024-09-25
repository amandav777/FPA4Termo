<template>
    <div class="testimonial-section">
        <h2 class="testimonial"> TESTIMONIALS</h2>
        <p class="voices">Voices of Satisfaction: Discover What Our Clients Have to Say</p>
    </div>
        <div class="row">
            <div class="col">
                <div class="star">
                    <img src="../assets/icons/star.png" alt="">
                </div>
                <p>
                I absolutely love this coffee maker! I use it every morning. Cold coffee is my favorite and this little machine makes great cold coffee. It is strong and tasty. I regular coffee cup or a larger stainless steel cup will work.
                </p>
                <div class="testimonials">
                    <img src="../assets/images/foto2.png">
                </div>
                <div class="name">Marlina Jole</div>
                <div class="name2">CEO, Coffin</div>
            </div>
        </div>
        <div class="col">
                <div class="star">
                    <img src="../assets/icons/star.png" alt="">
                </div>
                <p>
                I love the slim design of this Keurig. It works well except for the cold coffee. It states it does both hot and cold but I haven't found that to be accurate. The hot is perfect but it doesn't produce the cold coffee.
                </p>
                <div class="testimonials">
                    <img src="../assets/images/foto1.png">
                </div>
                <div class="name">Jhonatan Albert</div>
                <div class="name2">CEO, Samsung</div>
            </div>
            <div class="col">
                <div class="star">
                    <img src="../assets/icons/star.png" alt="">
                </div>
                <p>
                Nothing wrong with the maker but seller had it "On sale"truns out their supposed sale price was actually what the product actually sells for normally. It's retail price is 119.99. And is currently on sale for 64.99
                </p>
                <div class="testimonials">
                    <img src="../assets/images/foto3.png">
                </div>
                <div class="name">Stevano Albert</div>
                <div class="name2">CEO, Mayura</div>
            </div>

        <div class="arrow-navigation">
        <button @click="prevSlide">&#8592;</button>
        <button @click="nextSlide">&#8594;</button>
        </div>
        

</template>

<script>

export default {
  methods: {
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.testimonials.length;
    },
    prevSlide() {
      this.currentSlide = (this.currentSlide - 1 + this.testimonials.length) % this.testimonials.length;
    },
  },
};


</script>

<style>

.testimonial{
    color: #000;
    text-align: center;
    /* subtitle 1 */
    font-family: Inter;
    font-size: 36px;
    font-style: normal;
    font-weight: 600;
    line-height: 44px; /* 122.222% */
    letter-spacing: -1.44px;
        
}

.voices{
    color: var(--Base-60, #767A85);
    text-align: center;
    /* Body 2 */
    font-family: Inter;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 28px; /* 155.556% */
    letter-spacing: -0.18px;
}

.star{
    text-align: center;
}

.testimonials{
    text-align: center !important;
    position: relative;
    width: 50px;
    height: 50px;
    background-color: var(--neutral-10);
    border-radius: 50px;
    overflow: hidden;
    border: 2px ;

}

</style>