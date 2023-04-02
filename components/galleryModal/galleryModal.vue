<template>
    <div v-if="show" class="modal-overlay">
        <div class="modal-container">
            <div class="modal-header">
                <button class="modal-close" @click="closeModal">X</button>
            </div>
            <div class="modal-body">
                    <div class="box">
                        <img :src="image" class="img" />
                    </div>
                    <div>
                        <ImageArray></ImageArray>
                    </div>
            </div>
        </div>
    </div>
</template>
  
<script>
import {ImageArray} from '../imageArray/imageArray.vue'
import { images } from '../models/galleryImage.js'
export default {
    name: "GalleryModal",
    components: {
        ImageArray
    },
    props: {
        title: {
            type: String,
            default: "Modal Title"
        },
        show: {
            type: Boolean,
            default: false
        },
        image: {
            type: String,
            default: () => ''
        }
    },
    methods: {
        closeModal() {
            this.$emit("close");
        },
    },
    data(){
        return{
            localData: images
        }
    },
};
</script>
  
<style scoped>
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 999;
    display: flex;
    justify-content: center;
    align-items: center;
}

.modal-container {
    background-color: #fff;
    max-width: 600px;
    width: 100%;
    max-height: 100vh;
    overflow-y: auto;
    border-radius: 4px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

.modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    border-bottom: 1px solid #ccc;
}

.modal-header h2 {
    margin: 0;
}

.modal-close {
    background-color: transparent;
    border: none;
    cursor: pointer;
    font-size: 2rem;
    font-weight: bold;
}

.modal-body {
    padding: 1rem;
}

.modal-overlay>*:not(.modal-container) {
    filter: blur(3px);
    pointer-events: none;
}

.img {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.box {
    display: flex;
    margin: auto;
    max-width: 90%;
    min-width: 90%;
    max-height: 90%;
    min-height: 90%;
}
</style>

