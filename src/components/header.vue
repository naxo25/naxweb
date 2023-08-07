<template>
  <header class="fixed w-full z-30 md:bg-opacity-90 transition duration-300 ease-in-out">
    <nav x-data="{ isOpen: false }" style='max-width: 1280px; margin: auto;' class="relative dark:bg-gray-800">
      <div class="container px-6 py-4 md:flex md:justify-between md:items-center">
        <div class="flex items-center justify-between">
          <div class='flex items-center justify-center'>
            <img class="w-auto h-9" src="https://nacholabraweb.000webhostapp.com/ico.png" alt="">
            <h2 class="px-2 text-xl font-bold text-gray-800 dark:text-white"><span class='text-blue-600'>N</span>axWeb</h2>
          </div>

          <!-- Mobile menu button -->
          <div class="flex md:hidden">
            <button x-cloak @click="isOpen = !isOpen" type="button" class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400" aria-label="toggle menu">
              <svg v-if="!isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
              </svg>

              <svg v-if="isOpen" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>


        <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
        <div x-cloak :class="[isOpen ? 'translate-x-0 opacity-100 ' : 'opacity-0 -translate-x-full']" class="absolute inset-x-0 z-20 w-full px-6 py-4 transition-all duration-300 ease-in-out dark:bg-gray-800 md:mt-0 md:p-0 md:top-0 md:relative md:bg-transparent md:w-auto md:opacity-100 md:translate-x-0 md:flex md:items-center">
          <div class="flex flex-col md:flex-row md:mx-6">
            <div v-for='m in header'>
              <a class="font-medium text-gray-600 hover:text-gray-900 px-5 py-3 flex items-center transition duration-150 ease-in-out" :href="m.to" target='_blank'>{{ m.name }}</a>
            </div>
              <button class="bg-black rounded text-sm sm:text-base flex items-center gap-x-3 justify-center text-white hover:bg-black/80 duration-300 transition-colors border border-transparent px-8 py-2 ml-4">
                <svg class="w-3 h-3 fill-current text-gray-400" viewBox="0 0 12 12" xmlns="http://www.w3.org/2000/svg"><path d="M11.707 5.293L7 .586 5.586 2l3 3H0v2h8.586l-3 3L7 11.414l4.707-4.707a1 1 0 000-1.414z" fill-rule="nonzero"></path></svg>

                <span>Sign in</span>
              </button>
            </div>
            <!-- <a href='https://cafecito.app/naxweb' rel='noopener' target='_blank'><img srcset='https://cdn.cafecito.app/imgs/buttons/button_5.png 1x, https://cdn.cafecito.app/imgs/buttons/button_5_2x.png 2x, https://cdn.cafecito.app/imgs/buttons/button_5_3.75x.png 3.75x' src='https://cdn.cafecito.app/imgs/buttons/button_5.png' alt='Invitame un café en cafecito.app' /></a> -->
          </div>
        </div>
      </nav>
    </header>
  </template>

  <script setup>
    import { ref } from 'vue'
    const isOpen = ref(false)

    const header = [
      // { to: '#Portafolio', name: 'Portafolio' },
      { to: 'https://nacholabraweb.000webhostapp.com/naxtasksApp', name: 'NaxtasksApp' },
      // { to: 'https://nacholabraweb.000webhostapp.com/Tutoriales/dist', name: 'Tutoriales' },
      { to: 'https://asdf-3e590.web.app', name: 'Contactame en NaxChatApp' },
      { to: 'https://www.linkedin.com/jobs/search/?keywords=Frontend%20Developer', name: '¿Buscas trabajo?' },
    ]
  </script>