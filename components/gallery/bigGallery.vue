<template>
    <div class="box">
        <img :src="image" class="img" @click="localShowModal = true" />
        <GalleryModal :image='image' :show='localShowModal' @close="localShowModal = false">

        </GalleryModal>
    </div>
</template>

<script>
import GalleryModal from '../galleryModal/galleryModal.vue'
export default {
    name: 'BigGallery',
    components: {
        GalleryModal
    },
    props: {
        image: {
            typeof: String,
            default: () => ''
        },
        showModal: {
            typeof: Boolean,
            default: false
        }
    },
    data() {
        return {
            localShowModal: this.showModal,
        };
    },
    methods: {
        openModal() {
            this.localShowModal = true;
        }
    },
    watch: {
        showModal(newValue) {
            this.localShowModal = newValue;
        },
    },
}
</script>

<style scoped>
.img {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.box {
    display: flex;
    margin: auto;
    max-width: 60%;
    min-width: 60%;
    max-height: 60%;
    min-height: 60%;
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