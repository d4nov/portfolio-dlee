<template>
    <transition name="fade">
      <div v-if="show" class="welcome-background">
        <div class="welcome-text">
          <h1 >Hello!</h1>
        </div>
      </div>
    </transition>
  </template>
  
  <script>
  export default {
    name: 'WelcomeBackground',
    data() {
      return {
        show: true, // Hiển thị component
      };
    },
    mounted() {
      setTimeout(() => {
        this.show = false;
      }, 3500);
    },
  };
  </script>
  
  <style scoped>
  .welcome-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #b0fde0;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    z-index: 1000;
  }
  
  .welcome-text {
  text-align: center;
  color:  #333836 ; 
  z-index: 1;
  font: bold 2rem 'Roboto', sans-serif;
}
  
  .welcome-text h1 {
    font-size: 6rem;
    margin-bottom: 1rem;
    animation: fadeIn 2s ease-in-out;
  }
  
  .welcome-text p {
    font-size: 1.5rem;
    animation: fadeIn 3s ease-in-out;
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  .welcome-background::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 10%, transparent 10.01%);
    background-size: 20px 20px;
    animation: moveBackground 10s linear infinite;
  }
  
  @keyframes moveBackground {
    from {
      transform: translateY(0);
    }
    to {
      transform: translateY(-20px);
    }
  }
  

  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s ease;
  }
  
  .fade-enter-from, .fade-leave-to {
    opacity: 0;
  }
  </style>