<script setup lang="ts">
import { provide, ref, reactive } from 'vue';
import { RouterView } from 'vue-router';

// Configuración de idiomas
const languages = reactive({
  es: {
    title: 'Shinbukan Sogo Budo',
    nav: ['Inicio', 'Sobre nosotros', 'Clases', 'Contacto'],
  },
  en: {
    title: 'Shinbukan Sogo Budo',
    nav: ['Home', 'About us', 'Classes', 'Contact'],
  },
});

// Estado del idioma actual
const currentLanguage = ref<'es' | 'en'>('es');

// Función para alternar idiomas
const toggleLanguage = () => {
  currentLanguage.value = currentLanguage.value === 'es' ? 'en' : 'es';
};

// Proveemos el idioma y las configuraciones globalmente para que puedan ser accesibles desde cualquier parte
provide('languages', languages);
provide('currentLanguage', currentLanguage);
</script>

<template>
  <header class="bg-gray-800 text-white py-4 px-6">
    <div class="max-w-7xl mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold">{{ languages[currentLanguage].title }}</h1>
      <nav class="flex items-center space-x-4">
        <RouterLink
          v-for="(item, index) in languages[currentLanguage].nav"
          :key="index"
          :to="['/', '/about', '/classes', '/contact'][index]"
          class="hover:underline text-gray-300"
        >
          {{ item }}
        </RouterLink>
        <button
          @click="toggleLanguage"
          class="bg-gray-600 px-3 py-1 rounded text-sm hover:bg-gray-700"
        >
          {{ currentLanguage === 'es' ? 'EN' : 'ES' }}
        </button>
      </nav>
    </div>
  </header>

  <main class="min-h-screen bg-gray-100">
    <RouterView :key="currentLanguage" />
  </main>
</template>

<style scoped>
header {
  background-color: #1f2937;
  color: white;
}

nav a:hover {
  color: #ffffff;
}

main {
  padding: 2rem 1rem;
}
</style>
