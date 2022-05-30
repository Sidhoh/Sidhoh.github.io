<template>
  <div>
    <h1 class="home">Gallery</h1>
    <div class="images" v-viewer>
      <img
        v-for="src in images"
        :key="src"
        :src="src"
        width="250px"
        class="photos"
      />
    </div>
  </div>
</template>

<script>
import "viewerjs/dist/viewer.css";
import VueViewer from "v-viewer";
import Vue from "vue";
Vue.use(VueViewer);

export default {
  data() {
    return {
      images: [
        "https://github.com/Sidhoh/Gallery/blob/main/1.jpeg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/2.jpeg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/3.jpeg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/4.jpeg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/6.jpeg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/8.JPG?raw=true",
      ],
    };
  },
  methods: {
    show() {
      this.$viewerApi({
        images: this.images,
      });
    },
  },
};
</script>

<style></style>
