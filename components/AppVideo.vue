<template>
  <div
    class="max-w-7xl max-h-168 w-7xl h-168 bg-neutral-500 mx-auto rounded-3xl grid place-items-center custom bg-center bg-cover"
  >
    <div class="flex flex-col justify-center items-center">
      <app-button
        icon="fptplay"
        text="Video Clip"
        bg-color="bg-green-400"
        padding="p-2"
        text-size="text-sm"
        width="w-32"
      />
      <h1 class="font-bold text-4xl my-6 text-white">Giới thiệu FPT Telecom</h1>
      <p class="mt-4 text-center text-xl text-white max-w-xl mb-6">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt.
      </p>
      <app-button
        text="Giới thiệu ngay"
        bg-color="bg-secondary-500"
        :has-right-arrow="true"
        width="w-52"
      />
    </div>
  </div>
</template>

<script>
import AppButton from './AppButton.vue'
export default {
  components: {
    AppButton,
  },
}
</script>

<style lang="scss" scoped>
.custom {
  background-image: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),
    url('/cloud.jpg');
}
</style>
