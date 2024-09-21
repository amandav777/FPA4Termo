<template>
  <div class="promo-container">
    <div class="promo-content">
      <div class="promo-text">
        <h1>Save 20% or more on Headset</h1>
        <p>Enjoy for a limited time</p>
      </div>
      <div class="timer">
        <div class="time-section">
          <span id="hours">12</span>
          <p>HOURS</p>
        </div>
        <div class="time-section">
          <span id="minutes">25</span>
          <p>MINUTES</p>
        </div>
        <div class="time-section">
          <span id="seconds">45</span>
          <p>SECONDS</p>
        </div>
      </div>
      <button class="shop-now">
        SHOP NOW
        <div class="button_icon">
          <img src="../assets/icons/seta.png" alt="Seta" />
        </div>
      </button>
      <p class="details">Ends 18/08. Restrictions apply. See details</p>
    </div>
    <div class="promo-image">
      <svg class="background-svg" xmlns="http://www.w3.org/2000/svg" width="701" height="309" viewBox="0 0 701 309" fill="none">
        <g style="mix-blend-mode:multiply" filter="url(#filter0_f_1249_751)">
          <path d="M646.905 100L100 125.524L128.064 280L753 239.852L646.905 100Z" fill="#709CB2" fill-opacity="0.66"/>
        </g>
        <defs>
          <filter id="filter0_f_1249_751" x="0" y="0" width="853" height="380" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix"/>
            <feBlend mode="normal" in="SourceGraphic" in2="BackgroundImageFix" result="shape"/>
            <feGaussianBlur stdDeviation="50" result="effect1_foregroundBlur_1249_751"/>
          </filter>
        </defs>
      </svg>
      <img src="../assets/images/blueHeadset.png" alt="Headset" />
    </div>
  </div>
</template> 

<script>
function startCountdown(duration) {
  let remainingTime = duration; 

  function updateTimer() {
    const hoursElem = document.getElementById('hours');
    const minutesElem = document.getElementById('minutes');
    const secondsElem = document.getElementById('seconds');

    const hours = Math.floor(remainingTime / 3600);
    const minutes = Math.floor((remainingTime % 3600) / 60);
    const seconds = Math.floor(remainingTime % 60);

    hoursElem.textContent = String(hours).padStart(2, '0');
    minutesElem.textContent = String(minutes).padStart(2, '0');
    secondsElem.textContent = String(seconds).padStart(2, '0');

    remainingTime--;

    if (remainingTime < 0) {
      clearInterval(timer);
      hoursElem.textContent = '00';
      minutesElem.textContent = '00';
      secondsElem.textContent = '00';
    }
  }

  const timer = setInterval(updateTimer, 1000);
}

window.onload = function() {
  const durationInSeconds = 12 * 3600 + 25 * 60 + 45;
  startCountdown(durationInSeconds);
};


</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

body {
  margin: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
  font-family: Inter;
}

.promo-container {
  position: relative;
  width: 1400px;
  height: 645px;
  margin: 0 auto;
  flex-shrink: 0;
  display: flex;
  justify-content: center;
  padding: 60px;
  align-items: center;
  border-radius: 30px;
  border: 1px solid #000;
  color: #FFF;
  position: relative;
  background-image: url('../assets/images/background.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;  
}

.promo-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  max-width: 50%;
  gap: 20px;
}

.promo-text h1 {
  color: #FFF;
  font-family: Inter;
  font-size: 80px;
  font-weight: 600;
  line-height: 80px;
  letter-spacing: -3.2px;
  margin-top: 53px;
  margin-left: 101px;
}

.promo-text p {
  font-size: 1.5em;
  margin-left: 101px;
  font-weight: 400;
  font-family: Inter;
}

.timer {
  display: flex;
  gap: 68.51px;
  font-family: Inter;
  align-items: center;
  margin-left: 101px;
}

.time-section {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.time-section span {
  font-size: 127.257px;
}

.time-section p {
  font-size: 24px;
  font-family: Inter;
  color: #FFF;
  margin-top: -15px;
  text-transform: uppercase;
  letter-spacing: 2px;
}

.shop-now {
  width: 179px;
  height: 56px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #FFF;
  color: #000;
  border: 2px solid #E2E2E2;
  padding: 8px;
  padding-left: 22px;
  border-radius: 30px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  margin-left: 101px;
  transition: background-color 0.3s, color 0.3s;
  text-transform: uppercase;
  position: relative;
  overflow: hidden;
  font-family: 'Inter', sans-serif;
}

.shop-now:hover {
  background-color: #548CAD;
  color: #000000;
}

.button_icon {
  background-color: #000;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 35px;
  height: 35px;
  margin-left: 10px;
  transition: background-color 0.3s;
}

.button_icon img {
  width: 15px;
  height: 15px;
}

.shop-now:hover .button_icon {
  background-color: #FFF;
}

.details {
  font-size: 1em;
  margin-left: 101px;
  color: #FFF;
  font-family: Inter;
  margin-bottom: 61px;
}

.promo-image {
  flex-grow: 1;
  display: flex;
  justify-content: flex-end;
  margin-right: 65px;
  position: relative;
}

.promo-image img {
  width: 490px;
  height: 509px;
  flex-shrink: 0;
  position: relative;
  z-index: 2;
}

.background-svg {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-42.5%, -10%);
  z-index: 1;
  width: 701px;
  height: 309px;
  pointer-events: none;
}

.numbers {
  position: absolute;
  animation: scroll 1s infinite linear;
}

@keyframes scroll {
  0% { transform: translateY(0); }
  100% { transform: translateY(-160px); }
}

.numbers div {
  height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media screen and (max-width: 1024px) {
  .promo-container {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .promo-content {
    max-width: 90%;
    margin-bottom: 20px;
  }

  .promo-image {
    justify-content: center;
  }

  .promo-image img {
    width: 250px;
  }

  .background-svg {
    width: 350px; 
    height: auto;
  }

  .shop-now {
    width: 120px;
    height: 42px;
    font-size: 10px;
  }

  .details {
    font-size: 0.8em;
  }
}

@media screen and (max-width: 768px) {
  .promo-container {
    width: 100%;
    padding: 20px;
  }

  .promo-content {
    max-width: 100%;
  }

  .promo-text h1 {
    font-size: 36px;
    line-height: 40px;
  }

  .timer {
    gap: 20px;
  }

  .time-section span {
    font-size: 60px;
  }

  .promo-image img {
    width: 200px;
  }

  .background-svg {
    width: 300px; 
  }

  .shop-now {
    width: 110px;
    height: 40px;
    font-size: 10px;
  }

  .details {
    font-size: 0.75em;
  }
}

@media screen and (max-width: 375px) {
  .promo-container {
    padding: 20px;
    height: auto;
  }

  .promo-text h1 {
    font-size: 32px;
  }

  .promo-text p {
    font-size: 1em;
  }

  .time-section span {
    font-size: 50px;
  }

  .promo-image img {
    width: 200px;
  }

  .background-svg {
    width: 300px; 
  }

  .shop-now {
    width: 100px;
  }

  .details {
    font-size: 0.75em;
  }
}
</style>