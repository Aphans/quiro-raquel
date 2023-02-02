<template>
    <img src="https://escuelaelitesalud.es/wp-content/uploads/2018/04/quiromasaje.jpg" alt="imagen de fondo" class="bg-gray-900 text-white bg-cover bg-center">
  <nav class="fixed w-full z-10 top-0 flex items-center justify-between p-6 bg-transparent text-color">
    <div class="flex items-center">
      <img src="../assets/images/logo.png" alt="Logo" class="h-30 w-40">
      <h1 class="hidden sm:block ml-4 text-2xl font-medium">Quiro Raquel</h1>
    </div>
    <div class="hidden sm:flex items-center">
      <router-link to="/" class="px-4 py-2 text-lg font-medium hover:text-gray-300">Inicio</router-link>
      <router-link to="/about" class="px-4 py-2 ml-8 text-lg font-medium hover:text-gray-300">Sobre nosotros</router-link>
      <router-link to="/therapeutic" class="px-4 py-2 ml-8 text-lg font-medium hover:text-gray-300">Terápeutico</router-link>
      <router-link to="/sport" class="px-4 py-2 ml-8 text-lg font-medium hover:text-gray-300">Deportivo</router-link>
      <router-link to="/contact" class="px-4 py-2 ml-8 text-lg font-medium hover:text-gray-300">Contacto</router-link>
    </div>
    <div class="block sm:hidden">
      <button class="flex items-center px-3 py-2 text-gray-500 hover:text-white" @click="show = !show">
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menú</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/>
        </svg>
      </button>
    </div>
  </nav>
  <div class="sm:hidden p-6 bg-transparent text-black" v-show="show">
    <router-link to="/" class="block px-4 py-2 text-lg font-medium hover:text-gray-300">Inicio</router-link>
    <router-link to="/about" class="block px-4 py-2 text-lg font-medium hover:text-gray-300">Sobre nosotros</router-link>
    <router-link to="/therapeutic" class="block px-4 py-2 text-lg font-medium hover:text-gray-300">Terápeutico</router-link>
    <router-link to="/sport" class="block px-4 py-2 text-lg font-medium hover:text-gray-300">Deportivo</router-link>
    <router-link to="/contact" class="block px-4 py-2 text-lg font-medium hover:text-gray-300">Contacto</router-link>
    </div>
  </template>

<script setup>
import {ref} from 'vue';
  const show = ref(true);
</script>
<style scoped>
  .absolute {
    position: absolute;
    top: -6px; /* ajusta el margen negativo al alto de tu nav */
    left: 0;
    right: 0;
    z-index: -1;
  }
</style>