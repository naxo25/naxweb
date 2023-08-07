<template>
  <section class="block relative z-1 bg-g2 pb-10">
    <!--<div class="container mx-auto">
      <div class="justify-center flex flex-wrap">
        <div class="w-full lg:w-12/12 px-4  -mt-24">
          <div class="flex flex-wrap">
            <div v-for='p in portafolio' class="w-full lg:w-4/12 px-4">
              <blockquote class='text-center flex flex-col mx-auto items-center mb-20'>
                <div class="relative flex flex-col min-w-0 break-words w-full mb-6  rounded-lg ease-linear transition-all duration-150">
                  <img class="shadow-lg imgPort align-middle border-none max-w-full mx-auto h-auto rounded-lg" :src="p.img">
                </div>

                <h5 class="text-xl font-semibold mb-1">{{  p.Titulo}}</h5>

                <div class="mt-2 text-gray-500 capitalize dark:text-gray-300">{{ p.cargo }}</div>

                <div class="flex mt-3 -mx-2 mb-2">
                  <a :href="a.link" target='_blank' v-for='a in p.links' class="mx-2 text-gray-600 dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300">
                    <img class='w-6 h-6 fill-current' :src="'/ico/' + a.ico + '.svg'">
                  </a>
                </div>

                <div class="flex gap-y-3 mt-3 -mx-2">
                  <a target='_blank' v-for='ico in p.icos' class="mx-2 text-gray-600 dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300" aria-label="Reddit">
                    <img class='w-5 h-5 fill-current' :src="'/ico/' + ico">
                  </a>
                </div>
              </blockquote>
            </div>
          </div>
        </div>
      </div>
    </div> -->

      <div id='portafolio' class="container mx-auto">
          <div class="grid grid-cols-1 gap-8 pt-8 xl:pt-16 md:grid-cols-2 xl:grid-cols-3">
              <div v-for='p in portafolio' class="flex flex-col items-center p-8 transition-colors duration-300 transform cursor-pointer group hover:bg-white rounded-xl">
                  <img class="w-32 h-32 rounded-full ring- ring-gray-300" :src="p.img" alt="">

                  <h1 class="mt-4 text-2xl font-semibold text-gray-700 capitalize dark:text-white">{{ p.Titulo }}</h1>

                  <div class="mt-2 text-gray-500 capitalize dark:text-gray-300">{{ p.cargo }}</div>

                  <div class="flex mt-3 -mx-2 mb-2">
                      <a :href="a.link" target='_blank' v-for='a in p.links' class="mx-2 text-gray-600 dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300">
                        <img class='w-6 h-6 fill-current' :src="'/ico/' + a.ico + '.svg'">
                      </a>
                  </div>

                  <div class="flex gap-y-3 mt-3 -mx-2">
                      <a target='_blank' v-for='ico in p.icos' class="mx-2 text-gray-600 dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300" aria-label="Reddit">
                        <img class='w-5 h-5 fill-current' :src="'/ico/' + ico">
                      </a>
                  </div>
              </div>
          </div>

        <a target="blank" href="https://github.com/naxo25">
          <button class="bg-black mx-auto mt-20 rounded text-sm sm:text-base flex items-center gap-x-3 justify-center text-white hover:bg-black/80 duration-300 transition-colors border border-transparent px-8 py-2.5"><svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-github" width="24" height="24" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
             <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
             <path d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5"></path>
           </svg>
           <span>Ver mi Github</span>
         </button>
       </a>
      </div>
  </section>
</template>

<script setup>
  import { portafolio } from '@/boot/list.js'
</script>