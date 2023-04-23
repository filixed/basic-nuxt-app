<template>
  <div>
    <h1>nasa</h1>
    <div class="box">
      <input v-model="searchData" placeholder="..." />
      <button @click="findData()">Search</button>
    </div>
    <div class="box">
      <template v-for="(value) in nasaCollection" >
        <template v-for="(itemLinks, index) in value.links" >
          <BigGallery v-if="index == 0" :image="itemLinks.href" :data-index="index"> </BigGallery>
        </template>
      </template>
      >
      <!-- <img class="imgstyle" :src="value.links[0].href" v-for="(value, index) in nasaCollection" :key="index" /> -->
    </div>
  </div>
</template>

<script>
import BigGallery from "~/components/gallery/bigGallery.vue";
import axios from "axios";

export default {
  name: "index",
  components: { BigGallery },
  created() {
    this.fetchData("sun");
  },
  data() {
    return {
      nasaCollection: [],
      searchData: "",
    };
  },
  methods: {
    findData() {
      this.fetchData(this.searchData);
      this.searchData = "";
    },
    async fetchData(searchValue) {
      await axios
        .get("https://images-api.nasa.gov/search?q=" + searchValue)
        .then((res) => {
          console.log(res.data.collection.items);
          console.log(this.searchData);
          this.nasaCollection = res.data.collection.items;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style scoped>
.box {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
