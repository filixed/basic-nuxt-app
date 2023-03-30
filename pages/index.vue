<template>
  <div>
  <Header></Header>
  <BigGallery image="https://dynamic-media-cdn.tripadvisor.com/media/photo-o/0f/ba/29/5c/img-worlds-of-adventure.jpg?w=1200&h=-1&s=1"></BigGallery>
    <BigGallery image="https://media.architecturaldigest.com/photos/57c7003fdc03716f7c8289dd/master/pass/IMG%20Worlds%20of%20Adventure%20-%201.jpg"></BigGallery>
  </div>
</template>

<script>
import Header from '../components/nav/Header.vue'
import BigGallery from '../components/gallery/BigGallery.vue'
export default {
  name: 'IndexPage',
  components: {Header, BigGallery}
}
</script>

