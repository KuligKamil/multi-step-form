<script setup lang="ts">

</script>

<template>
  <div>
    <div class="flex justify-center items-center my-6">
      <div class="step active">1</div>
      <div class="line"></div>
      <div class="step">2</div>
      <div class="line"></div>
      <div class="step">3</div>
      <div class="line"></div>
      <div class="step">4</div>
    </div>
  </div>
</template>
<style lang="postcss" scoped>
.step {
  @apply w-8 h-8 rounded-full bg-gray-200 mx-4 flex justify-center items-center
}

.line {
  @apply w-24 h-1.5 bg-gray-200 rounded-3xl
}

.active {
  @apply bg-red-400 text-white
}
</style>