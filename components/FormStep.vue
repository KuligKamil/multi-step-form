<script setup lang="ts">

</script>

<template>
  <div class="bg-white rounded-2xl shadow flex flex-col item-center" style="width: 640px; height: 525px">
    <Steps></Steps>
    <!-- <span class="line" style=""></span> -->
    <div class="flex flex-col items-center">
      <div class="mb-8" style="width: 580px; height: 0px; border: 0.50px #E5E7EB solid"></div>
    </div>
    <div class="flex flex-col items-center">
      <h2 class="text-gray-900 text-2xl font-medium mb-2">
        Personal Information
      </h2>
      <p class="text-gray-500 text-sm font-normal">
        Please provide your personal details so we can get to know you better.
      </p>
    </div>
    <form class="flex flex-col items-center">
      <slot></slot>
      <div class="mt-10" style="width: 580px; height: 0px; border: 0.50px #E5E7EB solid"></div>
    </form>
  </div>
</template>
<style lang="postcss" scoped></style>