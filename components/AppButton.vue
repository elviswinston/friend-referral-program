<template>
  <button
    class="flex justify-evenly items-center w-fit text-white rounded-full"
    :class="[bgColor, width, textSize, padding]"
  >
    <component :is="getIcon()"></component>
    <p>{{ text }}</p>
    <component :is="getRightArrow()" v-show="hasRightArrow"></component>
  </button>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: '',
    },
    text: {
      type: String,
      default: '',
    },
    bgColor: {
      type: String,
      default: '',
    },
    hasRightArrow: {
      type: Boolean,
      default: false,
    },
    width: {
      type: String,
      default: 'w-40',
    },
    textSize: {
      type: String,
      default: 'text-base',
    },
    padding: {
      type: String,
      default: 'p-4',
    },
  },
  methods: {
    getIcon() {
      if (this.icon) return require(`@/assets/icons/${this.icon}.svg?inline`)
    },
    getRightArrow() {
      return require('@/assets/icons/chevron-right.svg?inline')
    },
  },
}
</script>

<style lang="scss" scoped></style>
