<template>
  <div>
    <navHeader></navHeader>
    <Nuxt />
    <GalleryModal :show="modal.show">
        <img :src="modal.content">
    </GalleryModal>
  </div>
</template>

<script>
import GalleryModal from '~/components/galleryModal/galleryModal.vue';

export default {
    data() {
        return {
            modal: {
                show: false,
                content: null,
            },
        };
    },
    created() {
        this.$nuxt.$on("runModal", ($event) => this.setModal($event));
        this.$nuxt.$on("closeModal", ($event) => this.setModal($event));
    },
    methods: {
        setModal(e) {
            this.modal.content = e.content;
            this.modal.show = e.state;
        },
    },
    components: { GalleryModal }
};
</script>
