<template>
<main class='pt-72'>
<h1 class="text-5xl text-center md:text-6xl font-extrabold leading-tighter tracking-tighter mb-10 aos-init aos-animate" data-aos="zoom-y-out">Ignacio Labra <span class="bg-clip-text text-transparent bg-gradient-to-r from-blue-500 to-teal-400">Website</span></h1>

<div class="max-w-3xl mx-auto">
<p class="mt-14 text-lg mb-14 text-center leading-relaxed text-gray-600">Conocerte a ti mismo es una cualidad necesaria para volverte mejor persona, para los demás, para contigo mismo y para el éxito. De que serviría ser el mejor si eres un asco con tu equipo, no aportas en nada y no enseñas nada a los demás, tú actitud es la que te abre más caminos que saber mil frameworks.</p>

<div class="max-w-xs gap-x-3 mx-auto sm:max-w-none sm:flex sm:justify-center aos-init aos-animate" data-aos="zoom-y-out" data-aos-delay="300">
<button @click='video=true' class="bg-blue-900 animate-pulse flex gap-x-3 text-sm sm:text-base items-center justify-center text-white rounded hover:bg-[#1877F2]/80 duration-300 transition-colors border border-transparent px-8 py-2.5">
<!-- <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-file-cv" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
<path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
<path d="M14 3v4a1 1 0 0 0 1 1h4"></path>
<path d="M17 21h-10a2 2 0 0 1 -2 -2v-14a2 2 0 0 1 2 -2h7l5 5v11a2 2 0 0 1 -2 2z"></path>
<path d="M11 12.5a1.5 1.5 0 0 0 -3 0v3a1.5 1.5 0 0 0 3 0"></path>
<path d="M13 11l1.5 6l1.5 -6"></path>
</svg> -->

<span>Ver videocv</span>
</button>
<a href="#portafolio" class="bg-black rounded text-sm sm:text-base flex items-center gap-x-3 justify-center text-white hover:bg-black/80 duration-300 transition-colors border border-transparent px-8 py-2.5">
<!-- <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-github" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
<path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
<path d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5"></path>
</svg> -->

<span>Ver experiencia</span>
</a>
</div>

<img @click='video=true' class='mt-32 cursor-pointer shadow-2xl rounded-xl' style='height: 432px;' :src='img'>

<p class='mt-10 text-center text-sm text-gray-600'>*Nota: En el video te muestro lo que me ayudo ir a la universidad hasta ahora.</p>
</div>

<div v-if='video' class='fixed top-0 left-0 right-0 bottom-0 z-30'>
<div class='absolute bg-black w-full h-screen opacity-70' @click="video=false"></div>
<div class="mt-28">
<video class='mx-auto relative rounded-lg shadow' :src='linkVideo' autoplay loop controls></video>
</div>
</div>
</main>
</template>

<script setup>
import { ref } from 'vue'

const img = '/images/image.jpg' // https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fempleocerca.com%2Fwp-content%2Fuploads%2F2021%2F08%2F2105-ECC-img-nota-6.png&f=1&nofb=1&ipt=353509e95f0013f8771969e0829e27ebdca3d46ed35aaa3a831df4c08e82953f&ipo=images
  // const msgMovil = ref(window.screen.width < 1040)
const linkVideo = 'https://tzjikybnymfhmvezapqo.supabase.co/storage/v1/object/public/public/1688466617248.mp4'
const video = ref(false)
</script>