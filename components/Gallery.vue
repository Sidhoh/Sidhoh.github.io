<template>
  <div>
    <h1 class="home">Gallery</h1>
    <div class="images" v-viewer="{button: false, navbar: false, title: false, toolbar: false, tooltip: false, movable: false, zoomable: false, rotatable: false, scalable: false, transition: false, fullscreen: false, keyboard: true}">
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
        "https://github.com/Sidhoh/Gallery/blob/main/9.gif?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/10.jpg?raw=true",
        "https://github.com/Sidhoh/Gallery/blob/main/11.png?raw=true",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/11.jpeg",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/12.jpeg",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/13.jpeg",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/14.jpeg",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/15.jpg",
        "https://raw.githubusercontent.com/Sidhoh/Gallery/main/16.jpg"
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
