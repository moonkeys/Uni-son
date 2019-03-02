<template>
  <div class="section profile-content">
    <div class="container">
      <div class="md-layout">
        <div class="md-layout-item mx-auto">
          <div class="profile">
            <div class="avatar">
              <img :src="img" alt="Circle Image" class="img-raised rounded-circle img-fluid">
            </div>
            <div class="name">
              <h3 class="title">{{nom}}</h3>
              <h6>{{titre}}</h6>
              <div v-show="isVisible">
                <md-button :href="insta" class="md-just-icon md-simple md-instagram">
                  <i class="fab fa-instagram"></i>
                </md-button>
                <md-button :href="fb" class="md-just-icon md-simple md-facebook">
                  <i class="fab fa-facebook"></i>
                </md-button>
                <md-button :href="yt" class="md-just-icon md-simple md-youtube">
                  <i class="fab fa-youtube"></i>
                </md-button>
                <md-button :href="twitter" class="md-just-icon md-simple md-twitter">
                  <i class="fab fa-twitter"></i>
                </md-button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="description text-center">
        <p>{{description}}</p>
      </div>
      <div class="profile-tabs">
        <!-- here you can add your content for tab-content -->
        <template>
          <div class="md-layout" v-if="carousel">
            <carousel
              :per-page="1"
              loop
              :speed="700"
              autoplay
              :autoplay-timeout="5000"
              :mouse-drag="false"
              navigationEnabled
              navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
              navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
            >
              <slide>
                <img v-img:group :src="photos[0].image" alt="carousel1">
              </slide>
              <slide>
                <img v-img:group :src="photos[1].image" alt="carousel2">
              </slide>
              <slide>
                <img v-img:group :src="photos[2].image" alt="carousel3">
              </slide>
            </carousel>
          </div>
          <div align="center" v-else>
            <div class="md-layout-item md-medium-size-50 md-small-size-75">
              <div
                v-for="(src, index) in images"
                :key="index"
                class="pic"
                @click="() => showImg(index)"
              >
                <img :src="src">
              </div>
              <div class>
                <VueEasyLightbox
                  :visible="visible"
                  :imgs="images"
                  :index="index"
                  @hide="handleHide"
                ></VueEasyLightbox>
              </div>

              <img v-img:group-1 :src="photos[3].image" class="rounded">
              <p></p>
            </div>
            <div class="md-layout">
              <div class="md-layout-item md-size-50 ml-auto">
                <p></p>

                <img v-img:group-1 :src="photos[1].image" class="rounded">
                <p></p>
              </div>
              <div class="md-layout-item md-size-50 mr-auto">
                <img v-img:group-1 :src="photos[2].image" class="rounded">
                <p style="padding-bottom:25px;"></p>
                <p>
                  <img v-img:group-1 :src="photos[0].image" class="rounded">
                </p>
              </div>
            </div>
          </div>
        </template>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
import VueGallery from "vue-gallery";
import VueGallerySlideshow from "vue-gallery-slideshow";
import VueEasyLightbox from "vue-easy-lightbox";

export default {
  components: {
    Tabs,
    gallery: VueGallery,
    VueGallerySlideshow,
    VueEasyLightbox
  },
  bodyClass: "profile-page",
  data() {
    return {};
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/image-de-profil.jpg")
    },
    nom: String,
    titre: String,
    photos: Array,
    images: Array,
    description: String,
    carousel: false,
    isVisible: false,
    visible: false,
    index: 0,

    fb: {
      type: String,
      defaut: null
    },
    insta: {
      type: String,
      defaut: null
    },
    twitter: {
      type: String,
      defaut: null
    },
    yt: {
      type: String,
      defaut: null
    }
  },
  methods: {
    onClick(i) {
      this.index = i;
    },
    showImg(index) {
      this.index = index;
      this.visible = true;
    },
    showSingle() {
      this.imgs = "http://via.placeholder.com/350x150";
      this.show();
    },
    showMultiple() {
      this.imgs = [
        "http://via.placeholder.com/350x150",
        "http://via.placeholder.com/350x150"
      ];
      this.index = 1; // index of imgList
      this.show();
    },
    show() {
      this.visible = true;
    },
    handleHide() {
      this.visible = false;
    }
  }
};
</script>

<style lang="scss" scoped>
.section {
  padding: 0;
}

.profile-tabs /deep/ {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
.image {
  float: left;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  border: 1px solid #ebebeb;
  margin: 5px;
}
</style>
