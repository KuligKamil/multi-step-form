<script setup lang="ts">
</script>
<template>
  <div class="h-screen flex flex-col justify-center grow items-center mx-auto bg-lime-50">
    <h1 class="text-gray-900 text-3xl font-black">Join our Community of Developers</h1>
    <p class="text-center text-gray-900 text-lg font-normal mt-4 mb-8">To join our community and participate in
      frontend challenges.<br />Please fill out the following form.</p>
    <div>
      <FormStep>
        <div class="grid grid-cols-2 gap-1">
          <div class="flex flex-col">
            <label for="name" class="label">Full Name</label>
            <input type="text" name="name" id="name" class="input" placeholder="Rocky Balboa" required />
            <label for="email" class="label">Phone Number</label>
            <input type="email" name="email" id="email" class="input" required />

          </div>
          <div class="flex flex-col">
            <label for="email" class="label">Email Address </label>
            <input type="email" name="email" id="email" class="input" required />
            <label for="email" class="label">Portfolio/GitHub Link</label>
            <input type="text" name="link" id="link" class="input" required />

          </div>
        </div>

      </FormStep>

      <span class="line"></span>
    </div>
  </div>
</template>
<style lang="postcss" scoped>
.label {
  @apply text-gray-900 text-sm font-medium mb-2 mt-4
}

.input {
  @apply w-64 h-10 rounded-lg border border-gray-300
}
</style>
