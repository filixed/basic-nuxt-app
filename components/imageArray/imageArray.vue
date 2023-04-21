<template>
    <div class="miniGallery">
        <SmallGallery v-for="(item, index) in items" :key="index" :image="item"></SmallGallery>
    </div>
  </template>
  
  <script>
import SmallGallery from '../gallery/smallGallery.vue' 

export default {
    name: 'ImageArray',
    components: {
        SmallGallery,
    },
    props: {
      items: {
        type: Array,
        required: true,
      },
    },
  };

  </script>
  
  <style scoped>  
  .miniGallery {
      display: flex;
      margin: auto;
      max-width: 100%;
      min-width: 100%;
      max-height: 25%;
      min-height: 25%;
  }
  </style>