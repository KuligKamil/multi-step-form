<script setup lang="ts">
defineProps<{
  title: string
  description: string
}>()
</script>

<template>
  <div class="bg-white sm:w-[640px] rounded-2xl p-4 sm:py-8 sm:px-[1.875rem] flex flex-col" style="box-shadow: 10px 10px 0px 0px #F4EDD6">
    <StepsProgress :number-of-steps="4" :active-number="1" />
    <div class="max-sm:hidden flex flex-col items-center">
      <div class="divider" />
    </div>
    <div>
      <div class="mb-5">
        <h2 class="text-gray-900 text-2xl font-medium mb-2 font-poppins font-medium">
          {{ title }}
        </h2>
        <p class="text-gray-500 text-sm font-normal">
          {{ description }}
        </p>
      </div>
      <form class="sm:flex flex-wrap justify-between" submit.prevent="onSubmit">
        <slot name="content" />
        <div class="divider mt-8" />
        <slot name="buttons" />
      </form>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.divider {
  @apply mb-8 w-full h-0 border-[0.5px] border-gray-200 border-solid
}
</style>
