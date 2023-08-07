<script setup lang="ts">
const props = defineProps<{
  name: string
  type: string
  placeholder: string
  labelText: string
  modelValue: string
}>()

const emit = defineEmits<{
  (event: 'update:modelValue', value: string): void
}>()
</script>

<template>
  <div class="flex flex-col">
    <label :for="name" class="label font-poppins font-medium">{{ labelText }}</label>
    <input
      :id="name" :value="modelValue" :type="type"
      :name="name" :placeholder="placeholder" required class="w-64 h-10 rounded-lg border border-gray-300 p-3 pb-2.5 outline-none focus-visible:border-red-400"
      @input="emit('update:modelValue', ($event.target as HTMLInputElement).value)"
    >
  </div>
</template>

<style lang="postcss" scoped>
.label {
  @apply text-gray-900 text-sm mb-2 mt-4
}
</style>
