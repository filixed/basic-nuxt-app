<template>
    <div class="minibox">
        <img :src="image" class="img"/>
    </div>
</template>

<script>
export default {
    name: 'SmallGallery',
    props: {
        image: {
            typeof: String,
            default: () => ''
        }
    }
}
</script>

<style scoped>
.img {
    display: flex;
    flex-direction: column;
    width: 100%;
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