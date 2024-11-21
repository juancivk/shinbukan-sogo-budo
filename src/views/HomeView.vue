<script setup lang="ts">
import { inject } from 'vue';

// Obtenemos el idioma actual y la configuración de idiomas
const currentLanguage = inject('currentLanguage');
const languages = inject('languages');
</script>

<template>
  <section class="bg-gray-100 py-10 px-6">
    <!-- Hero Section -->
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-5xl font-bold mb-6">
        {{ currentLanguage === 'es'
          ? 'Bienvenidos a Shinbukan Sogo Budo'
          : 'Welcome to Shinbukan Sogo Budo' }}
      </h2>
      <p class="text-lg text-gray-700 mb-6">
        {{ currentLanguage === 'es'
          ? 'Explora nuestro arte marcial en español. Aprende sobre nuestra filosofía, clases y horarios.'
          : 'Explore our martial art in English. Learn about our philosophy, classes, and schedule.' }}
      </p>
      <div>
        <img
          src="https://via.placeholder.com/1200x600"
          alt="Aikido Practice"
          class="w-full h-auto rounded-lg shadow-lg"
        />
      </div>
    </div>

    <!-- Sección Filosofía -->
    <div class="py-20 bg-white">
      <div class="max-w-7xl mx-auto text-center">
        <h3 class="text-4xl font-bold mb-6">
          {{ currentLanguage === 'es' ? 'Nuestra Filosofía' : 'Our Philosophy' }}
        </h3>
        <p class="text-lg text-gray-700">
          {{ currentLanguage === 'es'
            ? 'En Shinbukan Sogo Budo, practicamos Aikido no solo como un arte marcial, sino como una forma de vida. Nuestro enfoque está en la armonía y el respeto, buscando el equilibrio tanto físico como mental.'
            : 'At Shinbukan Sogo Budo, we practice Aikido not only as a martial art but as a way of life. Our focus is on harmony and respect, seeking balance both physically and mentally.' }}
        </p>
      </div>
    </div>

    <!-- Sección de Clases -->
    <div class="py-20 bg-gray-100">
      <div class="max-w-7xl mx-auto text-center">
        <h3 class="text-4xl font-bold mb-6">
          {{ currentLanguage === 'es' ? 'Nuestras Clases' : 'Our Classes' }}
        </h3>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <!-- Card 1 -->
          <div class="bg-white rounded-lg shadow-md overflow-hidden">
            <img
              src="https://via.placeholder.com/400x300"
              alt="Clase de Aikido"
              class="w-full h-48 object-cover"
            />
            <div class="p-4">
              <h4 class="text-xl font-semibold mb-2">
                {{ currentLanguage === 'es' ? 'Aikido Básico' : 'Basic Aikido' }}
              </h4>
              <p class="text-gray-600">
                {{ currentLanguage === 'es'
                  ? 'Clases para principiantes donde aprenderás los fundamentos del Aikido.'
                  : 'Classes for beginners where you will learn the fundamentals of Aikido.' }}
              </p>
            </div>
          </div>
          <!-- Card 2 -->
          <div class="bg-white rounded-lg shadow-md overflow-hidden">
            <img
              src="https://via.placeholder.com/400x300"
              alt="Clase avanzada de Aikido"
              class="w-full h-48 object-cover"
            />
            <div class="p-4">
              <h4 class="text-xl font-semibold mb-2">
                {{ currentLanguage === 'es' ? 'Aikido Avanzado' : 'Advanced Aikido' }}
              </h4>
              <p class="text-gray-600">
                {{ currentLanguage === 'es'
                  ? 'Para aquellos que ya dominan lo básico y desean profundizar en la técnica.'
                  : 'For those who have mastered the basics and wish to deepen their technique.' }}
              </p>
            </div>
          </div>
          <!-- Card 3 -->
          <div class="bg-white rounded-lg shadow-md overflow-hidden">
            <img
              src="https://via.placeholder.com/400x300"
              alt="Clase Infantil de Aikido"
              class="w-full h-48 object-cover"
            />
            <div class="p-4">
              <h4 class="text-xl font-semibold mb-2">
                {{ currentLanguage === 'es' ? 'Aikido Infantil' : 'Children’s Aikido' }}
              </h4>
              <p class="text-gray-600">
                {{ currentLanguage === 'es'
                  ? 'Clases adaptadas para niños, enseñando disciplina y concentración.'
                  : 'Classes tailored for children, teaching discipline and concentration.' }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Sección de Instructores -->
    <div class="py-20 bg-white">
      <div class="max-w-7xl mx-auto text-center">
        <h3 class="text-4xl font-bold mb-6">
          {{ currentLanguage === 'es' ? 'Nuestros Instructores' : 'Our Instructors' }}
        </h3>
        <div class="flex justify-center space-x-8">
          <!-- Instructor 1 -->
          <div class="text-center">
            <img
              src="https://via.placeholder.com/150"
              alt="Instructor"
              class="w-32 h-32 rounded-full mb-4"
            />
            <h4 class="font-semibold text-xl mb-2">Sensei Juan Pérez</h4>
            <p class="text-gray-600">{{ currentLanguage === 'es' ? 'Instructor principal de Aikido' : 'Chief Aikido Instructor' }}</p>
          </div>
          <!-- Instructor 2 -->
          <div class="text-center">
            <img
              src="https://via.placeholder.com/150"
              alt="Instructor"
              class="w-32 h-32 rounded-full mb-4"
            />
            <h4 class="font-semibold text-xl mb-2">Sensei María López</h4>
            <p class="text-gray-600">{{ currentLanguage === 'es' ? 'Instructor de Aikido avanzado' : 'Advanced Aikido Instructor' }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Testimonios -->
    <div class="py-20 bg-gray-100">
      <div class="max-w-7xl mx-auto text-center">
        <h3 class="text-4xl font-bold mb-6">
          {{ currentLanguage === 'es' ? 'Testimonios' : 'Testimonials' }}
        </h3>
        <div class="flex flex-col md:flex-row justify-center space-y-6 md:space-y-0 md:space-x-6">
          <!-- Testimonio 1 -->
          <div class="bg-white p-6 rounded-lg shadow-md w-full md:w-1/3">
            <p class="text-lg italic text-gray-600">
              "{{ currentLanguage === 'es' ? 'El Aikido cambió mi vida, me ha enseñado a mantener la calma en situaciones difíciles.' : 'Aikido changed my life, it taught me to remain calm in tough situations.' }}"
            </p>
            <p class="font-semibold mt-4">Juan Gómez</p>
            <p class="text-gray-500">Estudiante de Aikido</p>
          </div>
          <!-- Testimonio 2 -->
          <div class="bg-white p-6 rounded-lg shadow-md w-full md:w-1/3">
            <p class="text-lg italic text-gray-600">
              "{{ currentLanguage === 'es' ? 'La disciplina y la filosofía del Aikido han sido clave para mi crecimiento personal.' : 'The discipline and philosophy of Aikido have been key to my personal growth.' }}"
            </p>
            <p class="font-semibold mt-4">Ana Martínez</p>
            <p class="text-gray-500">Estudiante avanzada</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Contacto -->
    <div class="py-20 bg-white">
      <div class="max-w-7xl mx-auto text-center">
        <h3 class="text-4xl font-bold mb-6">
          {{ currentLanguage === 'es' ? 'Contacto' : 'Contact' }}
        </h3>
        <p class="text-lg text-gray-700 mb-6">
          {{ currentLanguage === 'es'
            ? 'Si tienes preguntas o deseas más información sobre nuestras clases, no dudes en contactarnos.'
            : 'If you have questions or need more information about our classes, feel free to contact us.' }}
        </p>
        <a
          href="mailto:info@shinbukan.com"
          class="inline-block bg-blue-600 text-white px-6 py-3 rounded-full text-lg"
        >
          {{ currentLanguage === 'es' ? 'Escríbenos' : 'Write to us' }}
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
h2, h3 {
  color: #1f2937;
}

p {
  color: #4b5563;
}
</style>
