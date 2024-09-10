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
        <button class="shop-now">Shop Now</button>
        <p class="details">Ends 18/08. Restrictions apply. See details</p>
      </div>
      <div class="promo-image">
        <img src="../assets/images/image__2__1-removebg-preview.png" alt="Headset" />
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
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    font-family: 'Roboto', sans-serif;
  }
  
  .promo-container {
    width: 1000px;
    height: 600px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 30px;
    border: 1px solid #000;
    color: #FFF;
    padding: 20px;
    position: relative;
    background: linear-gradient(124deg, #548CAD 11.53%, #97C4D8 57.38%);
                /* url('../assets/images/Logo_gabini_cinza.png');  */
    background-size: cover; 
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
    font-size: 3em;
    margin: 50px;
    font-weight: 700;
  }
  
  .promo-text p {
    font-size: 1.5em;
    margin: 50px;
    font-weight: 400;
  }
  
  .timer {
    font-size: 3em;
    margin: 20px 50px;
    font-weight: 700;
    display: flex;
    gap: 5px;
  }
  
  .shop-now {
    background-color: #FFF;
    color: #548CAD;
    border: none;
    padding: 15px 30px;
    border-radius: 25px;
    font-size: 1.5em;
    cursor: pointer;
    margin: 2px 50px;
    font-weight: 700;
    transition: background-color 0.3s, color 0.3s;
  }
  
  .shop-now:hover {
    background-color: #548CAD;
    color: #FFF;
  }
  
  .details {
    font-size: 1em;
    margin: 2px 50px;
    color: #FFF;
  }
  
  .promo-image {
    flex-grow: 1;
    display: flex;
    justify-content: flex-end;
  }
  
  .promo-image img {
    max-width: 400px;
    max-height: 400px;
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
  

  