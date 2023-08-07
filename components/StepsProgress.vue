<script setup lang="ts">
defineProps<{
  numberOfSteps: number
  activeNumber: number
}>()
</script>

<template>
  <div class="max-sm:hidden relative overflow-auto">
    <div class="overflow-x-scroll flex justify-center items-center mb-8">
      <template v-for="step in numberOfSteps" :key="step">
        <!-- ml-0 mr-0 -->
        <div class="step" :class="{ active: step <= activeNumber }">
          {{ step }}
        </div>
        <div v-if="step !== numberOfSteps" class="line" :class="{ active: step < activeNumber }" />
      </template>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.step {
  @apply w-8 h-8 flex justify-center items-center rounded-full bg-gray-200 mx-5
}

.line {
  @apply w-24 h-1.5 bg-gray-200 rounded-3xl
}

.active {
  @apply bg-red-400 text-white
}
</style>
