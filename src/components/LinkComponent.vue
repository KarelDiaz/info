<template>
  <a
    class="px-3 py-1 text-xs text-center text-blue-500 transition-all duration-500 transform shadow-lg rounded-xl hover:scale-105 hover:shadow-xl bg-gradient-to-b from-gray-100 to-white hover:text-blue-700"
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