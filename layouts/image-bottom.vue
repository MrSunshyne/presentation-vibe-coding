<script setup lang="ts">
import { computed } from 'vue'
import CardLayers from '../components/CardLayers.vue'

const props = defineProps<{
  image?: string
  imageClass?: string
}>()

// Default image class for styling
const imgClass = computed(() => props.imageClass || 'object-cover w-full h-full')
</script>

<template>
  <div class="w-full h-full relative overflow-hidden">
    <!-- Background with patterns -->
    <div 
      class="absolute inset-0 bg-theme-blue z-0"
      style="view-transition-name: background-layer"
    >
      <!-- Geometric patterns overlay -->
      <div class="absolute inset-0 opacity-50 bg-repeat" style="background-image: repeating-linear-gradient(45deg, transparent, transparent 50px, rgba(255, 255, 255, 0.03) 50px, rgba(255, 255, 255, 0.03) 100px)"></div>
    </div>
    
    <!-- Main container with vertical layout -->
    <div class="absolute inset-0 flex flex-col z-1">
      <!-- Top section: Title/content (1/4 height) -->
      <div class="relative flex items-center justify-center px-16" style="height: 25%;">
        <div class="w-full max-w-1200px text-center layout-image-bottom text-white text-4xl font-bold">
          <slot />
        </div>
      </div>
      
      <!-- Bottom section: Large image (3/4 height with overflow allowed) -->
      <div class="relative flex items-start justify-center px-16 overflow-visible" style="height: 75%;">
        <div class="w-full max-w-1200px flex justify-center overflow-visible h-full">
          <div v-if="image" class="rounded-lg overflow-hidden shadow-2xl border-4 border-white h-full">
            <img :src="image" :class="imgClass" alt="Slide image" />
          </div>
          <div v-else class="text-white text-center opacity-50 mt-12">
            <p class="text-xl">No image specified</p>
            <p class="text-sm mt-2">Add <code class="bg-white/20 px-2 py-1 rounded">image: /path/to/image.png</code> to frontmatter</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

