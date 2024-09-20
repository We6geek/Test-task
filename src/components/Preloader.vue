<template>
    <div class="preloader">
      <div class="loader">
        <div class="light-ring"></div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Preloader'
  };
  </script>
  
  <style scoped>
  .preloader {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-image: url('../assets/images/bg_hero.png');
    background-size: cover;
    background-position-x: center;
    background-position-y: center;
  }
  
  .loader {
    position: relative;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border: 10px solid transparent;
    border-top: 10px solid rgb(250, 0, 255);
    border-right: 10px solid rgba(72, 112, 255, 1);
    border-bottom: 10px solid rgb(144, 0, 255);
    border-left: 10px solid rgba(0, 204, 255, 1);
    animation: gradient-spin 1.5s ease-in-out infinite;
  }
  
  .light-ring {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100px;
    height: 100px;
    margin-top: -50px;
    margin-left: -50px;
    border-radius: 50%;
    background: linear-gradient(69deg, rgba(250, 0, 255, 1) 0%, rgba(72, 112, 255, 1) 100%);
    box-shadow: 0 0 15px rgba(250, 0, 255, 0.6),
                0 0 25px rgba(72, 112, 255, 0.5),
                0 0 35px rgba(144, 0, 255, 0.5),
                0 0 50px rgba(0, 204, 255, 0.4);
    animation: flashing 2s linear infinite;
    opacity: 0.8;
  }
  
  @keyframes gradient-spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  
  @keyframes flashing {
    0%, 100% {
      opacity: 0.8;
    }
    50% {
      opacity: 1;
    }
  }
  </style>
  