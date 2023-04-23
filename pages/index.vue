<template>
  <div>
    <BigGallery
      image="https://dynamic-media-cdn.tripadvisor.com/media/photo-o/0f/ba/29/5c/img-worlds-of-adventure.jpg?w=1200&h=-1&s=1">
    </BigGallery>
  </div>
</template>

<script>
import Header from '../components/nav/Header.vue'
import BigGallery from '../components/gallery/bigGallery.vue'

export default {
  name: 'IndexPage',
  components: { Header, BigGallery },
  props: {
    show: {
      type: Boolean,
      default: false
    },
  }
}
</script>

