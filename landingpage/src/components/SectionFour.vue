<template>
    <div class="promo-container">
      <div class="promo-content">
        <div class="promo-text">
          <h1>Save 20% or more on Headset</h1>
          <p>Enjoy for a limited time</p>
        </div>
        <div class="timer">
          <span id="hours" class="number-slide">12</span>:
          <span id="minutes" class="number-slide">25</span>:
          <span id="seconds" class="number-slide">45</span>
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
  function startCountdown() {
    let hours = 12;
    let minutes = 25;
    let seconds = 45;
  
    function updateTimer() {
      let prevSeconds = seconds;
      let prevMinutes = minutes;
      let prevHours = hours;
  
      seconds--;
      if (seconds < 0) {
        seconds = 59;
        minutes--;
        if (minutes < 0) {
          minutes = 59;
          hours--;
          if (hours < 0) {
            hours = 0;
            minutes = 0;
            seconds = 0;
            clearInterval(timer);
          }
        }
      }
  
      if (prevSeconds !== seconds) {
        slideNumber('seconds', seconds);
      }
  
      if (prevMinutes !== minutes) {
        slideNumber('minutes', minutes);
      }
  
      if (prevHours !== hours) {
        slideNumber('hours', hours);
      }
    }
  
    function slideNumber(id, value) {
      const element = document.getElementById(id);
      element.classList.remove('slide');
      void element.offsetWidth; 
      element.classList.add('slide');
      element.textContent = value.toString().padStart(2, '0');
    }
  
    const timer = setInterval(updateTimer, 1000);
  }
  
  window.onload = startCountdown;
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
    width: 1400px;
height: 645px;
flex-shrink: 0;
    display: flex;
    justify-content: center;
    padding: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 30px;
    border: 1px solid #000;
    color: #FFF;
    padding: 20px;
    position: relative;
    background: linear-gradient(124deg, #548CAD 11.53%, #97C4D8 57.38%), 
                url('../assets/images/Texture.png');
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
    color: var(--White-white-50, #FFF);
font-family: Inter;
font-size: 80px;
font-style: normal;
font-weight: 600;
line-height: 80px; 
letter-spacing: -3.2px;
margin-top: 53px;
padding: 0;
margin-left: 101px;
  }
  
  .promo-text p {
    font-size: 1.5em;
    margin-left: 101px;
    font-weight: 400;
    font-family: Inter;
  }
  
  .timer {
    font-size: 3em;
    margin-left: 101px;
    font-size: 127.257px;
    display: flex;
    gap: 5px;
    font-family: Inter;
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
    border-radius: 30px; /* Faz o botão ser oval */
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    margin: 2px 50px;
    transition: background-color 0.3s, color 0.3s;
    text-transform: uppercase;
    position: relative;
    overflow: hidden;
    font-family: 'Inter', sans-serif;
    margin-left: 101px;
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

  
  .shop-now:hover {
    background-color: #548CAD;
    color: #FFF;
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

  

  .number-slide {
    display: inline-block;
    position: relative;
    overflow: hidden;
  }
  
  .slide {
    animation: slide-up 0.5s ease-in-out forwards;
  }
  
  @keyframes slide-up {
    0% {
      transform: translateY(100%);
    }
    100% {
      transform: translateY(0);
    }
  }
  
  </style>
  

  