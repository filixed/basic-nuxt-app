<template>
    <div>
        <Header></Header>
        <h1>About Us</h1>
        <h2>web</h2>
        <button @click="showInfo">Click me</button>
    </div>

</template>

<script>
import Header from '../components/nav/Header.vue'
export default {
  name: 'AboutUs',
  components: {Header},
  methods: {
    showInfo: () => {
        console.log('hello')
        alert('hellow')
    }
  }
}
</script>

<style scoped></style>