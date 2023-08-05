<script setup lang="ts">
const props = defineProps<{
  name: string,
  type: string,
  placeholder: string,
  labelText: string,
  modelValue: string,
}>();

const emit = defineEmits<{
  (event: 'update:modelValue', value: string): void
}>()
</script>
<template>
  <div class="flex flex-col">
    <label :for="name" class="label font-poppins-500">{{ labelText }}</label>
    <input :value="modelValue" @input="emit('update:modelValue', ($event.target as HTMLInputElement).value)" :type="type"
      :name="name" :id="name" :placeholder="placeholder" required
      class="w-64 h-10 rounded-lg border border-gray-300 p-3 pb-2.5 active:border-red-400 outline-none focus:border-red-400 focus-visible:border-red-400" />
  </div>
</template>
<style lang="postcss" scoped>
.label {
  @apply text-gray-900 text-sm mb-2 mt-4
}

.input {
  @apply w-64 h-10 rounded-lg border border-gray-300 p-3 pb-2.5;
}
</style>
