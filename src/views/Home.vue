<template>
  <div class="wrapper">
    <div class="section page-header header-filter" :style="headerStyle">
      <div class="container">
        <div class="md-layout">
          <div class="md-layout-item text-center mx-auto">
            <h4 slot="title" class="card-title">
              <img :src="couverture" alt="Rounded Image" class="img-raised rounded img-fluid">
            </h4>

            <div class="md-layout-item md-size-50 mx-auto">
              <router-link to="/accueil">
                <md-button class="md-default md-info md-lg mx-auto">
                  <img :src="backgroundImage"> Welcome
                </md-button>
              </router-link>
              <div class="md-layout-item md-size-50 mx-auto">
                <md-button slot="buttons" class="md-just-icon md-simple md-white">
                  <i class="fab fa-facebook-square"></i>
                </md-button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { LoginCard } from "@/components";

export default {
  components: {
    LoginCard
  },
  bodyClass: "login-page",
  data() {
    return {
      affiche: require("@/assets/img/affiche/affiche2019.png"),
      couverture: require("@/assets/img/affiche/couverture2019.jpg")
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/affiche/fond-bannière.png")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="css"></style>
