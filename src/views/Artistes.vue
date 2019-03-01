<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle"></parallax>
    <br>
    <br>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout text-center" style="margin-left: 5px;margin-right: 5px;">
              <div style="margin-bottom: 20%;" align="center">
                <artiste
                  nom="MB14"
                  titre="Beatbox"
                  :img="photoMB14"
                  isVisible="true"
                  :photos="photosMB14"
                  :images="photosMB14"
                  fb="https://www.facebook.com/mb14beatbox/?hc_ref=ARS40_SRiI5yyp4Ta8jNafdeieJ_DQSQwmok6_pIpb5vuvKrF97N2dzfllxa9s1xQeE&__xts__[0]=68.ARCRw1IqYeIWe3gPR56JXouWJhhNz_7NqccGc1QOtBpV33ZpEL4_d9WXQxs9rYamd7y1nVh7KAzeQlShwLaW0ksUvAnuPlo1LVufZNn1_Uz4bDuHTETSaGpi8bZdoPXJdOPbvzxni4PXY1s9bBEZCBZeM2_Ht9iSaajzYxwFjWS9jVTRwd5e9IEWVP5Usl65PJkJF0mquAvC_4gYw_uQmsrPwWdwPmnmQ4YzV09Zpxnf-vjFBGSODWhNJz1MKBAve3BtBVOnJqOTMQ&__tn__=kC-R"
                  insta="https://www.instagram.com/mb14beatbox/?hl=fr"
                  yt="https://www.youtube.com/channel/UCloH7JPn0CtzIJnThe125_g"
                  twitter="https://twitter.com/mb14beatbox"
                  description="
              Gagnant The Voice saison 5.
              "
                />
              </div>
              <div style="margin-bottom: 20%;">
                <artiste
                  :photos="photosUnison"
                  :images="photosUnison"
                  :carousel="false"
                  nom="Petit Déjeuner"
                  titre="Meilleur groupe de l'UTT"
                  description="J'aime le petit déjeuner"
                />
              </div>
              <div style="margin-bottom: 20%;">
                <artiste
                        :photos="photosUnison"
                  :images="photosUnison"
                  :img="photoMoonkeys"
                  :carousel="false"
                  nom="Moonkeys"
                  titre="Meilleur groupe de l'UTT"
                  description="J'aime le petit déjeuner"
                />
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
export default {
  data() {
    return {
      photoMB14: require("@/assets/img/faces/mb14.jpg"),
      photosMB14: [
        require("@/assets/img/mb14/mb14-2.jpg"),
        require("@/assets/img/mb14/mb14-5.jpg"),
        require("@/assets/img/mb14/mb14-1.jpg"),
        require("@/assets/img/mb14/mb14-4.jpg")
      ],
      photoMoonkeys: require("@/assets/img/faces/moonkeys.jpg"),
      photosUnison: [
        require("@/assets/img/2018/uni_son-5.jpg"),
        require("@/assets/img/2018/uni_son-12.jpg"),
        require("@/assets/img/2018/uni_son-35.jpg"),
        require("@/assets/img/2018/uni_son-14.jpg"),
        require("@/assets/img/2018/uni_son-40.jpg")
      ]
    };
  },
  components: {
    Artiste
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/affiche/bannièrefbunison.png")
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

<style lang="scss" scoped>
</style>
