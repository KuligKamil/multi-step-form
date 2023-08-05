<script setup lang="ts">
defineProps<{
  title: string,
  description: string,
}>();

</script>

<template>
  <div class="bg-white w-[640px] h-[525px] rounded-2xl flex flex-col" style="box-shadow: 10px 10px 0px 0px #F4EDD6">
    <StepsProgress />
    <BaseLine />
    <div>
      <div class="flex flex-col ml-8 mb-5">
        <h2 class="text-gray-900 text-2xl font-medium mb-2 font-poppins-500">
          {{ title }}
        </h2>
        <p class="text-gray-500 text-sm font-normal">
          {{ description }}
        </p>
      </div>
      <form class="flex flex-wrap justify-between mx-8" submit.prevent="onSubmit">

        <div class="flex flex-wrap justify-between">
          <slot name="content"></slot>
        </div>

        <BaseLine class="mt-8" />
        <div class="w-full flex flex-row-reverse">
          <slot name="buttons"></slot>
        </div>
      </form>
    </div>
  </div>
</template>
<style lang="postcss" scoped></style>