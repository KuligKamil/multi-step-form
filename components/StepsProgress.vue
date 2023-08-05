<script setup lang="ts">

</script>

<template>
  <div>
    <div class="flex justify-center items-center my-8">
      <div class="step active ml-0">1</div>
      <div class="line"></div>
      <div class="step">2</div>
      <div class="line"></div>
      <div class="step">3</div>
      <div class="line"></div>
      <div class="step mr-0">4</div>
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