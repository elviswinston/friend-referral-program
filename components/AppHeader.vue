<template>
  <div class="relative bg-neutral-800 h-fit">
    <div class="flex items-center h-20 w-8/12 mx-auto gap-x-12">
      <div class="flex justify-between items-center gap-x-12">
        <img src="/logo_fpt.png" alt="Logo FPT" class="cursor-pointer" />
        <img
          src="/logo_advocater_sell.png"
          alt="Logo Advocater Sell"
          class="cursor-pointer"
        />
      </div>
      <div class="flex justify-between items-center flex-1">
        <div v-for="menu in menus" :key="menu.name">
          <a
            :href="menu.url"
            class="text-sm font-small text-neutral-500 font-medium hover:text-white"
            >{{ menu.name }}</a
          >
        </div>
      </div>
      <div class="flex justify-between items-center gap-x-12">
        <SearchIcon class="cursor-pointer" />
        <ProfileCircle class="cursor-pointer" />
      </div>
    </div>
  </div>
</template>

<script>
import SearchIcon from '@/assets/icons/search.svg?inline'
import ProfileCircle from '@/assets/icons/profile-circle.svg?inline'

export default {
  components: {
    SearchIcon,
    ProfileCircle,
  },
  data() {
    return {
      menus: [
        {
          name: 'Trang chủ',
          url: '/',
        },
        {
          name: 'Giới thiệu bạn bè',
          url: '/',
        },
        {
          name: 'Khuyến mãi',
          url: '/',
        },
        {
          name: 'Tin tức',
          url: '/',
        },
        {
          name: 'FAQs',
          url: '/',
        },
        {
          name: 'Tích điểm',
          url: '/',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
