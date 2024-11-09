<template>
    <div class="animated-gradient" :style="gradientStyle">
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AnimatedGradient',
    props: {
      height: {
        type: String,
        default: '300px'
      },
      width: {
        type: String,
        default: '100%'
      }
    },
    data() {
      return {
        angle: 0,
        intervalId: null
      }
    },
    computed: {
      gradientStyle() {
        return {
          background: `linear-gradient(${this.angle}deg, 
            #32a852,
            #41c967,
            #32a852,
            #288543,
            #32a852
          )`,
          backgroundSize: '400% 400%',
          animation: 'gradient 15s ease infinite',
          height: this.height,
          width: this.width
        }
      }
    },
    mounted() {
      this.intervalId = setInterval(() => {
        this.angle = (this.angle + 1) % 360
      }, 50)
    },
    beforeDestroy() {
      if (this.intervalId) {
        clearInterval(this.intervalId)
      }
    }
  }
  </script>
  
  <style scoped>
  .animated-gradient {
    border-radius: 15px;
  }
  
  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
  </style>