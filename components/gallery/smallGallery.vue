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
    height: 100%;
}

.minibox {
    display: flex;
    margin: auto;
    max-width: 25%;
    min-width: 25%;
    max-height: 25%;
    min-height: 25%;
}
</style>