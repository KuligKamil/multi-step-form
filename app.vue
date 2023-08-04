<script setup lang="ts">
</script>
<template>
  <div class="h-screen flex flex-col justify-center grow items-center mx-auto" style="background-color: #F3F3E3">
    <h1 class="text-gray-900 text-3xl font-black">Join our Community of Developers</h1>
    <p class="text-center text-gray-900 text-lg font-normal mt-4 mb-8">To join our community and participate in
      frontend challenges.<br />Please fill out the following form.</p>
    <div>
      <FormStep>
        <PersonalInformation name="name" type="text" placeholder="Rocky Balboa" label-text="Full Name" />
        <PersonalInformation name="email" type="emial" placeholder="name@email.com" label-text="Email Address" />
        <PersonalInformation name="phone" type="tel" placeholder="+91 1234567890" label-text="Phone Number" />
        <PersonalInformation name="link" type="url" placeholder="github.com/KuligKamil"
          label-text="Portfolio/GitHub Link" />
      </FormStep>
    </div>
  </div>
</template>
<style lang="postcss" scoped>
.label {
  @apply text-gray-900 text-sm font-medium mb-2 mt-4
}

.input {
  @apply w-64 h-10 rounded-lg border border-gray-300 p-3 pb-2.5;
}
</style>