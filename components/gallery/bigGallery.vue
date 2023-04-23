<template>
  <div @click="setModal(localImage)">
    <img :src="image"  class="img" />
  </div>
</template>

<script>
import GalleryModal from "../galleryModal/galleryModal.vue";
export default {
  name: "BigGallery",
  components: {
    GalleryModal,
  },
  props: {
    image: {
      typeof: String,
      default: () => "",
    },
  },
  data() {
    return {
      localImage : this.image
    };
  },
  methods: {
    setModal(value) {
      const data = {
        state: true,
        content: value,
      };
      this.$nuxt.$emit("runModal", data);
    },
  },
};
</script>

<style scoped>
.img {
  width: 100px;
  height: 100px;
  object-fit: cover;
  padding: 5px;
}

.minibox {
  display: flex;
  margin: auto;
  max-width: 5%;
  min-width: 5%;
  max-height: 5%;
  min-height: 5%;
}
</style>
