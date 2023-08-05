<script setup lang="ts">
const name = ref('')
const form = ref({
  name: '',
  email: '',
  phone: '',
  link: ''
})
</script>
<template>
  <div class="h-screen flex flex-col justify-center grow items-center mx-auto" style="background-color: #F3F3E3">
    <h1 class="text-gray-900 text-3xl font-black font-merry">Join our Community of
      Developers</h1>
    <p class="text-center text-gray-900 text-lg font-normal mt-4 mb-8">To join our community and
      participate in
      frontend challenges.<br />Please fill out the following form.</p>
    <pre>{{ name }}</pre>
    <pre>{{ form }}</pre>
    <div>
      <FormStep title="Personal Information"
        description=" Please provide your personal details so we can get to know you better.">
        <template #content>
          <BaseInput v-model="form.name" name="name" type="text" placeholder="Rocky Balboa" label-text="Full Name" />
          <BaseInput v-model="form.email" name="email" type="emial" placeholder="name@email.com"
            label-text="Email Address" />
          <BaseInput v-model="form.phone" name="phone" type="tel" placeholder="+91 1234567890"
            label-text="Phone Number" />
          <BaseInput v-model="form.link" name="link" type="url" placeholder="github.com/KuligKamil"
            label-text="Portfolio/GitHub Link" />
        </template>
        <template #buttons>
          <button
            class="w-30 h-10 px-6 py-2.5 bg-red-400 rounded-lg text-center text-white text-sm font-medium font-poppins-500">
            Next step
          </button>
        </template>
      </FormStep>
    </div>
  </div>
</template>
<style lang="postcss" scoped>
.font-merry {
  font-family: 'Merriweather', serif;
}

.label {
  @apply text-gray-900 text-sm font-medium mb-2 mt-4
}

.input {
  @apply w-64 h-10 rounded-lg border border-gray-300 p-3 pb-2.5;
}
</style>