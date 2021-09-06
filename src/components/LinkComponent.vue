<template>
  <a
    class="px-3 py-1 text-xs text-center text-blue-500 transition-all duration-500 transform border shadow-md  rounded-xl hover:scale-105 hover:shadow-lg bg-gradient-to-t from-gray-100 to-white hover:text-blue-700"
    @mouseenter="hover = true"
    @mouseleave="hover = false"
    :href="href"
    target="blanck"
  >
    <slot></slot>
  </a>
</template>

<script>
export default {
  data() {
    return {
      hover: false,
    };
  },
  props: {
    href: String,
  },
};
</script>