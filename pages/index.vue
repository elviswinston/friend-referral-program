<template>
  <div>
    <app-header />
    <app-banner-slider />
    <section class="bg-neutral-200">
      <div
        class="max-w-6xl m-auto flex flex-col justify-center items-center py-12 mb-12"
      >
        <AdvocaterIcon />
        <h1 class="mt-8 text-4xl font-bold">Giới thiệu bạn bè</h1>
        <p class="mt-4 text-center text-xl font-semibold max-w-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt.
        </p>
        <div class="mt-12">
          <p class="font-semibold text-base text-center mb-4">
            Giới thiệu bạn bè qua
          </p>
          <div class="flex justify-center items-center gap-x-6">
            <app-button
              icon="hifpt"
              text="Hi FPT"
              bg-color="bg-secondary-500"
            />
            <app-button
              icon="fptplay"
              text="FPT Play"
              bg-color="bg-green-500"
            />
          </div>
        </div>
      </div>
      <div class="grid place-items-center">
        <div class="">
          <img
            src="/iphone-left.png"
            alt="IPhone Left"
            class="relative float-left"
          />
          <img
            src="/iphone-middle.png"
            alt="IPhone Middle"
            class="relative float-left iphone-middle"
          />
          <img
            src="/iphone-right.png"
            alt="IPhone Right"
            class="relative float-left"
          />
        </div>
      </div>
    </section>
    <section class="bg-white py-16">
      <app-video />
    </section>
    <app-footer />
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
import AppBannerSlider from '@/components/AppBannerSlider.vue'
import AdvocaterIcon from '@/assets/icons/advocater.svg?inline'
import AppButton from '~/components/AppButton.vue'
import AppFooter from '~/components/AppFooter.vue'
import AppVideo from '~/components/AppVideo.vue'

export default {
  name: 'IndexPage',
  components: {
    AppHeader,
    AppBannerSlider,
    AdvocaterIcon,
    AppButton,
    AppFooter,
    AppVideo,
  },
}
</script>

<style lang="scss" scoped>
.iphone-middle {
  margin: -3.5rem -10rem 0 -10rem;
  z-index: 2;
}
</style>
