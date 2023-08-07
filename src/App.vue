<template>
  <Header />
  <Main />
  <desc1 />
  <Portafolio />
  <Footer />
</template>

<script setup>
  import Header from '@/components/header.vue'
  import Main from '@/components/main.vue'
  import desc1 from '@/components/desc1.vue'
  import Portafolio from '@/components/portafolio.vue'
  import Footer from '@/components/footer.vue'

  setInterval(() => {
    window.screen.width < 1040
      ? location.assign('https://nacholabraweb.000webhostapp.com/index2.html')
      : ''
  }, 2000)

  // const top = ref('margin-top:' + (screen.height/2))
</script>

<style>
  @media (max-width: 1024px) {
    video {
      width: 80%
    }
  }
  body, header, .bg-img {
    background-color: rgb(249, 250, 251);
  }
  .bg-g2 {
    background-color: rgba(241,245,249);
  }
  html {
    scroll-behavior: smooth;
  }
  ::-webkit-scrollbar {
    display: none;
  }
  .imgPort {
    width: 384px;
    height: 288px;
    background-color: rgba(241,245,249);
  }
</style>