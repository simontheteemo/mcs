<!-- src/views/HomeView.vue -->
<script setup lang="ts">
import { ref } from 'vue'
import GithubIcon from '../components/icons/IconGithub.vue'
import ProjectCard from '../components/ProjectCard.vue'

const projects = ref([
  {
    title: 'Movie2U',
    description:
      'A serverless application that enhances video accessibility by providing comprehensive visual and audio descriptions, specifically designed to help blind or visually impaired users understand video content',
    technologies: ['AWS', 'AI', 'serverless', 'Demo'],
    link: 'https://simontheteemo.github.io/Movie2U/',
  },
  {
    title: 'Plant Tracker',
    description: 'React Native App to help plant lovers to mangage their plants in real time.',
    technologies: ['ios', 'react-native', 'Beta'],
    link: 'https://github.com/simontheteemo/PlantTracker',
  },
])
</script>

<template>
  <main class="max-w-4xl mx-auto px-4 py-8">
    <!-- Hero Section -->
    <section class="text-center mb-16">
      <div class="w-32 h-32 rounded-full mx-auto mb-4 object-cover" />
      <h1 class="text-4xl font-bold mb-4">Miller Consulting Specialist</h1>
      <p class="text-xl text-gray-600 mb-6">IT Solutioning & Consulting</p>
      <div class="flex justify-center gap-4">
        <a
          href="https://github.com/simontheteemo"
          target="_blank"
          class="text-gray-700 hover:text-black"
        >
          <GithubIcon class="w-6 h-6" />
        </a>
        <a
          href="https://linkedin.com/in/yourusername"
          target="_blank"
          class="text-gray-700 hover:text-blue-600"
        >
          <LinkedInIcon class="w-6 h-6" />
        </a>
      </div>
    </section>

    <!-- About Section -->
    <section class="mb-16">
      <h2 class="text-2xl font-bold mb-4">About Us</h2>
      <p class="text-gray-700 leading-relaxed">
        We bring innovative software solutions from concept to reality. Our team specializes in
        crafting custom software products that solve real business challenges. With deep expertise
        in product development and engineering, we partner with businesses to build scalable,
        market-ready applications that drive growth. From MVP development to enterprise solutions,
        we combine technical excellence with product strategy to deliver software that makes an
        impact.
      </p>
    </section>

    <!-- Projects Section -->
    <section class="mb-16">
      <h2 class="text-2xl font-bold mb-6">Featured Projects</h2>
      <div class="grid md:grid-cols-2 gap-6">
        <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
      </div>
    </section>

    <!-- Contact Section -->
    <section>
      <h2 class="text-2xl font-bold mb-4">Get in Touch</h2>
      <p class="text-gray-700 mb-4">I'm always open to new opportunities and collaborations.</p>
      <a
        href="mailto:info.millercc@gmail.com"
        class="inline-block bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-colors"
      >
        Contact Me
      </a>
    </section>
  </main>
</template>

<style scoped>
/* Add any custom styles here */
</style>
