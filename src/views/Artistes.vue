<template xmlns:img="">
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <br />
    <br />
    <div class="main main-raised">
      <div class="section profile-content text-center">
        <div class="container">
          <h2 class="title">Tête d'affiche</h2>
          <div class="md-layout">
            <div
              class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center"
            >
              <artiste
                nom="Yves Romao"
                titre="Auteur - Compositeur - Interprète"
                :img="photoRomao"
                isVisible="true"
                :photos="photosRomao[0].image"
                fb="https://www.facebook.com/romaoyves/"
                insta="https://www.instagram.com/yvesromao/"
                yt="https://www.youtube.com/user/yvesromao"
                description="
              Chanson Pop Musique
              "
              />
            </div>
          </div>
          <div class="section text-center">
            <div class="container">
              <h2 class="title">Artistes Pulsation</h2>
              <div class="team">
                <div class="md-layout" style="padding-bottom: 20px">
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-100 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[0].image"
                      title="Big Band UTT"
                      subtitle="Meilleur Big Band de l'UTT"
                      description="input text."
                    />
                  </div>
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-100 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[1].image"
                      title="GSN"
                      subtitle="style musical"
                      description="input text."
                    />
                  </div>
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-100 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[2].image"
                      title="Prol'UTT"
                      subtitle="style musical"
                      description="input text."
                    />
                  </div>
                </div>
                <div class="md-layout">
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-100 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[4].image"
                      title="Red Machines"
                      subtitle="Groupe"
                      description="input text."
                    />
                  </div>
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-100 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[3].image"
                      title="Les Zicos"
                      subtitle="style musical"
                      description="input text."
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="section text-center">
            <div class="container">
              <h2 class="title">Artistes Extérieurs</h2>
              <div class="team">
                <div class="md-layout" style="padding-bottom: 20px">
                  <div
                    class="md-layout-item md-medium-size-33 md-xsmall-size-100 md-small-size-50 mx-auto text-center"
                  >
                    <item
                      v-img
                      :img="photosUnison[5].image"
                      title="Still in Beta"
                      subtitle="UTBM"
                      description="Hey ! Nous c'est Still in Beta, un groupe de l'UTBM monté il y a peu et spécialement pour l'occasion ! Notre délire ? Du bon vieux Rock avec une pointe de Punk de temps à autres, mais on joue aussi un peu de Pop 😀 N'hésite pas à venir nous écouter, on fait un peu peur, mais on mord pas, promis ! 😉"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Artiste from "@/views/Artiste.vue";
import Item from "@/components/Item.vue";
export default {
  data() {
    return {
      photoRomao: require("@/assets/img/faces/romao-profil.jpg"),
      photosRomao: [
        { image: require("@/assets/img/faces/romao.jpg") },
        { image: require("@/assets/img/faces/romao.jpg") }
      ],
      photosUnison: [
        { image: require("@/assets/img/faces/big-band.jpg") },
        { image: require("@/assets/img/2018/uni_son-12.jpg") },
        { image: require("@/assets/img/faces/prol-utt.jpg") },
        { image: require("@/assets/img/2018/uni_son-14.jpg") },
        { image: require("@/assets/img/faces/redmachines.png") },
        { image: require("@/assets/img/faces/redmachines.png") }
      ]
    };
  },
  components: {
    Artiste,
    Item
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/affiche/couverture2019.jpg")
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

<style lang="scss" scoped></style>
