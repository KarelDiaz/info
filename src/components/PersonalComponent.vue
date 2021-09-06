<template>
  <div class="relative">
    <!-- Background -->
    <div
      class="relative flex shadow-xl bg-gradient-to-t from-white to-gray-300 h-36 opacity-95"
    ></div>
    <!-- Name and phone number -->
    <div
      class="absolute top-0 left-0 flex flex-col w-full h-full p-3 text-transparent font-extralight bg-clip-text bg-gradient-to-b from-blue-500 to-blue-800 filter drop-shadow-md"
    >
      <span
        class="text-3xl font-bold transition-all duration-500 sm:text-6xl pr-28"
      >
        {{ info.name }}
      </span>
    </div>
    <!-- Image -->
    <img
      class="absolute top-0 right-0 z-10 h-36 filter drop-shadow-md"
      src="../assets/photo-small.png"
    />
    <!-- Social medias -->
    <social-media
      class="absolute left-0 z-50 -bottom-6"
      :socialMedias="info.socialMedias"
    />
  </div>
</template>

<script>
import SocialMedia from "./SocialMedia.vue";
export default {
  components: { SocialMedia },
  props: {
    info: Object,
  },
};
</script>