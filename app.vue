<script setup lang="ts">
const form = ref({
  name: '',
  email: '',
  phone: '',
  portfolioLink: '',
})
</script>

<template>
  <div class="sm:h-screen flex flex-col justify-center items-center" style="background-color: #F3F3E3">
    <h1 class="text-gray-900 sm:text-3xl font-black font-merry">
      Join our Community of
      Developers
    </h1>
    <p class="text-center text-gray-900 sm:text-lg font-normal mt-4 mb-8">
      To join our community and
      participate in
      frontend challenges.<br>Please fill out the following form.
    </p>
    <!-- <pre>{{ form }}</pre> -->
    <div>
      <FormStep
        title="Personal Information"
        description=" Please provide your personal details so we can get to know you better."
      >
        <template #content>
          <BaseInput v-model="form.name" name="name" type="text" placeholder="Rocky Balboa" label-text="Full Name" />
          <BaseInput
            v-model="form.email" name="email" type="email" placeholder="name@email.com"
            label-text="Email Address"
          />
          <BaseInput
            v-model="form.phone" name="phone" type="tel" placeholder="+91 1234567890"
            label-text="Phone Number"
          />
          <BaseInput
            v-model="form.portfolioLink" name="text" type="url" placeholder="github.com/KuligKamil"
            label-text="Portfolio/GitHub Link"
          />
        </template>
        <template #buttons>
          <div class="w-full flex flex-row-reverse">
            <button
              class="px-6 py-2.5 bg-red-400 rounded-lg text-center text-white text-sm font-poppins font-medium"
            >
              Next step
            </button>
          </div>
        </template>
      </FormStep>
    </div>
  </div>
</template>

<style lang="postcss" scoped>
.font-merry {
  font-family: 'Merriweather', serif;
}
</style>
