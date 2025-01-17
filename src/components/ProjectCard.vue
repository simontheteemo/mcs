<!-- src/components/ProjectCard.vue -->
<script setup lang="ts">
interface Project {
  title: string
  description: string
  technologies: string[]
  link: string
}

defineProps<{
  project: Project
}>()
</script>

<template>
  <div class="border rounded-lg p-6 hover:shadow-lg transition-shadow">
    <h3 class="text-xl font-semibold mb-2">{{ project.title }}</h3>
    <p class="text-gray-600 mb-4">{{ project.description }}</p>
    <div class="flex flex-wrap gap-2 mb-4">
      <span 
        v-for="tech in project.technologies" 
        :key="tech"
        class="bg-gray-100 px-3 py-1 rounded-full text-sm text-gray-700"
      >
        {{ tech }}
      </span>
    </div>
    <a 
      :href="project.link"
      target="_blank"
      class="text-blue-600 hover:text-blue-800 font-medium"
    >
      View Project →
    </a>
  </div>
</template>