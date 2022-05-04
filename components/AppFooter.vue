<template>
  <div class="bg-neutral-200">
    <div class="max-w-6xl m-auto flex flex-col justify-center items-center">
      <div
        class="flex justify-between items-center w-full py-5 border-b border-neutral-400"
      >
        <img src="/logo_fpt_color.png" alt="Logo FPT" />
        <div class="flex justify-between items-center gap-x-4">
          <div v-for="(item, index) in social" :key="index">
            <nuxt-link :to="item.url">
              <component
                :is="getIcon(item.icon)"
                class="cursor-pointer"
              ></component>
            </nuxt-link>
          </div>
        </div>
      </div>
      <div class="grid grid-cols-3 py-5 gap-x-12">
        <div>
          <p class="mb-5 text-sm">
            Giấy chứng nhận ĐKKD số 0101778163 do Sở Kế hoạch Đầu tư Thành phố
            Hà Nội cấp ngày 28/07/2005
          </p>
          <p class="mb-5 text-sm">
            Giấy phép cung cấp dịch vụ viễn thông số 469/GP-BTTTT do Bộ Thông
            tin và Truyền thông cấp ngày 14/10/2016
          </p>
          <p class="text-sm">
            Hotline: <span class="font-bold text-base">1900 6600</span>
          </p>
        </div>
        <div class="col-span-2">
          <div class="grid grid-cols-3">
            <div>
              <h3 class="text-base font-semibold mb-5">Về FPT Telecom</h3>
              <div class="flex flex-col gap-y-4">
                <nuxt-link
                  v-for="(item, index) in about"
                  :key="index"
                  :to="item.url"
                  class="text-sm"
                >
                  {{ item.name }}
                </nuxt-link>
              </div>
            </div>
            <div>
              <h3 class="text-base font-semibold mb-5">Quan hệ nhà đầu tư</h3>
              <div class="flex flex-col gap-y-4">
                <nuxt-link
                  v-for="(item, index) in coop"
                  :key="index"
                  :to="item.url"
                  class="text-sm"
                >
                  {{ item.name }}
                </nuxt-link>
              </div>
            </div>
            <div>
              <h3 class="text-base font-semibold mb-5">
                Dịch vụ của chúng tôi
              </h3>
              <div class="flex flex-col gap-y-4">
                <nuxt-link
                  v-for="(item, index) in services"
                  :key="index"
                  :to="item.url"
                  class="text-sm"
                >
                  {{ item.name }}
                </nuxt-link>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="flex justify-start items-center w-full mb-12">
        <template v-for="(item, index) in information">
          <nuxt-link :key="index" :to="item.url">
            <span :key="index" class="cursor-pointer text-sm">
              {{ item.name }}
            </span>
          </nuxt-link>
          <span
            :key="index"
            class="divider w-px h-4 bg-neutral-400 mx-4"
          ></span>
        </template>
      </div>
    </div>
    <div class="bg-neutral-800 py-1.5 text-center">
      <p class="text-sm text-white">© 2018 Bản quyền thuộc FPT Telecom</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      social: [
        {
          icon: 'hifpt-black',
          url: '/',
        },
        {
          icon: 'youtube-black',
          url: '/',
        },
        {
          icon: 'instagram-black',
          url: '/',
        },
        {
          icon: 'fb-black',
          url: '/',
        },
        {
          icon: 'zalo-black',
          url: '/',
        },
      ],
      information: [
        {
          name: 'Chính sách',
          url: '/',
        },
        {
          name: 'Điều khoản',
          url: '/',
        },
        {
          name: 'Bảo mật',
          url: '/',
        },
        {
          name: 'Liên hệ',
          url: '/',
        },
      ],
      about: [
        {
          name: 'Giới thiệu chung',
          url: '/',
        },
        {
          name: 'Chất lượng dịch vụ',
          url: '/',
        },
        {
          name: 'Công ty thành viên',
          url: '/',
        },
        {
          name: 'Giải thưởng',
          url: '/',
        },
        {
          name: 'Đối tác',
          url: '/',
        },
        {
          name: 'Về tập đoàn FPT',
          url: '/',
        },
        {
          name: 'Tuyển dụng',
          url: '/',
        },
      ],
      coop: [
        {
          name: 'Điều lệ công ty',
          url: '/',
        },
        {
          name: 'Quản trị công ty',
          url: '/',
        },
        {
          name: 'Đại hội đồng cổ đông',
          url: '/',
        },
        {
          name: 'Liên hệ cổ đông',
          url: '/',
        },
        {
          name: 'Thông báo chung',
          url: '/',
        },
      ],
      services: [
        {
          name: 'Internet FPT',
          url: '/',
        },
        {
          name: 'Truyền hình FPT',
          url: '/',
        },
        {
          name: 'Dịch vụ online',
          url: '/',
        },
        {
          name: 'Smart home',
          url: '/',
        },
      ],
    }
  },
  methods: {
    getIcon(icon) {
      if (icon) return require(`@/assets/icons/${icon}.svg?inline`)
    },
  },
}
</script>

<style lang="scss" scoped>
.divider:last-child {
  width: 0;
}
</style>
