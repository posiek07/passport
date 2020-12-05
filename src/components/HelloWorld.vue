<template>
  <div class="d-flex justify-content-center">
    <div class="justify-content-center">
      <div class="p-3 d-flex buttons-container justify-content-center">
        <div class="d-flex justify-content-end w-100 w-md-50">
          <button class="btn btn-primary round mr-2">
            <strong>Get the app</strong>
          </button>
          <button class="btn grey">
            <strong>Log In</strong>
          </button>
        </div>
      </div>
      <div class="image-container d-flex justify-content-center">
        <div class="w-100 w-md-50">
          <div class="m-4">
            <div class="d-block text-left">
              <div class=" d-flex  align-items-center mb-3">
                <h2 class="m-0">username</h2>
                <button class="btn btn-outline-primary ml-4 pl-2 pr-2 follow">
                  <strong>FOLLOW</strong>
                </button>
              </div>
              <p class="mb-0">
                <strong>Firstname Lastname</strong> Lorem ipsum dolor sit amet,
                consectetur.
              </p>
              <a href="www.instagram.com" alt="Instagram">www.instagram.com</a>
            </div>
            <div
              class="d-flex flex-row mt-3 w-100 w-md-50 justify-content-between"
            >
              <p class=""><strong>870</strong> posts</p>
              <p class="ml-4"><strong>495</strong> followers</p>
              <p class="ml-3"><strong>112</strong> posts</p>
            </div>
          </div>
          <div>
            <img
              class="image m-2"
              v-for="(image, i) in images"
              :src="image"
              :key="i"
              @click="index = i"
            />
          </div>
        </div>
      </div>
    </div>
    <vue-gallery-slideshow
      :images="images"
      :index="index"
      @close="index = null"
    ></vue-gallery-slideshow>
  </div>
</template>

<script>
import VueGallerySlideshow from "vue-gallery-slideshow";

export default {
  name: "HelloWorld",

  components: {
    VueGallerySlideshow,
  },
  data: () => {
    return {
      index: null,
    };
  },
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.image-container {
  background-color: rgb(243, 243, 243);
}
.buttons-container {
  background-color: rgb(255, 255, 255);
}
.image {
  width: 150px;
  height: 150px;
  background-size: cover;
  cursor: pointer;
  margin: 1em;
  border-radius: 3px;
  object-fit: cover;
}
.follow {
  height: 100%;
  padding: 3px;
}
.round {
  border-radius: 20px;
  padding: 0px 20px 0px 20px;
}
.grey {
  color: gray;
}
@media (min-width: 768px) {
  .w-md-50 {
    width: 50% !important;
  }
  .image {
    width: 210px;
    height: 210px;
  }
}
</style>
