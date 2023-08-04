<script setup lang="ts">

</script>

<template>
  <div class="bg-white rounded-2xl flex flex-col"
    style="width: 640px; height: 525px; box-shadow: 10px 10px 0px 0px #F4EDD6">
    <Steps></Steps>
    <!-- <span class="line" style=""></span> -->
    <div class="flex flex-col items-center">
      <div class="mb-8" style="width: 580px; height: 0px; border: 0.50px #E5E7EB solid"></div>
    </div>
    <div>
      <div class="flex flex-col ml-8 mb-5">
        <h2 class=" text-gray-900 text-2xl font-medium mb-2">
          Personal Information
        </h2>
        <p class="text-gray-500 text-sm font-normal">
          Please provide your personal details so we can get to know you better.
        </p>
      </div>
      <form class="flex flex-wrap gap-2 justify-between mx-8">
        <slot></slot>
        <div class="mt-8" style="width: 580px; height: 0px; border: 0.50px #E5E7EB solid"></div>
        <div class="w-full flex flex-row-reverse">
          <button class="w-28 h-10 px-6 py-2.5 bg-red-400 rounded-lg text-center text-white text-sm font-medium mt-4">
            Next step
          </button>
        </div>
      </form>
    </div>
  </div>
</template>
<style lang="postcss" scoped></style>