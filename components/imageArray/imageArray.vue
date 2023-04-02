<template>
    <div>
        <SmallGallery v-for="(item, index) in items" :key="index" :item="item"></SmallGallery>
    </div>
  </template>
  
  <script>
import {SmallGallery} from '../gallery/smallGallery.vue'
  
  export default {
    name: "ImageArray",
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
  