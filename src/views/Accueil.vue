<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle"></parallax>
    <div class="main main-raised">
      <div class="section">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto text-center">
              <h1 class="title">Uni'Son</h1>
              <h3 class="subtitle">by Pulsation UTT</h3>
              <h5 class="description">
                résumé unison.
                <img
                  src="@/assets/img/affiche/affiche2019.png"
                  alt="affiche2019"
                  style="padding-bottom: 15px"
                >
              </h5>
              <br>
              <md-button
                href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
                class="md-success md-lg"
                target="_blank"
              >
                <i class="fas fa-play"></i> Voir le teaser
              </md-button>
            </div>
          </div>
          <div class="team-player text-center">
            <md-card class="md-card-plain">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="info">
                  <div class="icon icon-info">
                    <md-icon>map</md-icon>
                  </div>
                </div>

                <h2 class="title text-center">Où c'est ?</h2>
                <div class="md-layout-item md-size-100 mx-auto">
                  <h5
                    class="description"
                  >Pour la première fois, Uni'Son aura lieu à la Chapelle Argence !</h5>
                  <img :src="mapView" v-img alt="Maps" class="img-raised">
                </div>
                <br>
                <h4 class="card-title">
                  <a
                    href="https://www.google.com/maps/place/Chapelle+Argence/@48.2877116,4.0723357,13.75z/data=!4m12!1m6!3m5!1s0x47ee9858d95ac6c3:0xbde05fa9da5fb65a!2sChapelle+Argence!8m2!3d48.2998506!4d4.0724576!3m4!1s0x47ee9858d95ac6c3:0xbde05fa9da5fb65a!8m2!3d48.2998506!4d4.0724576"
                  >20 bis Boulevard Gambetta, 10000 Troyes</a>
                </h4>
              </div>
            </md-card>
          </div>
        </div>
      </div>

      <div class="section text-center">
        <div class="container">
          <h2 class="title">Consommables</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="imgBieres[0].biere"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      >
                    </div>
                    <h4 class="card-title">Binouze
                      <br>
                      <small class="card-description text-muted">connais pas</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">input text.</p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="imgBieres[1].biere"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      >
                    </div>
                    <h4 class="card-title">Binouze
                      <br>
                      <small class="card-description text-muted">bière locale du canada</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">2.50</p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="imgBieres[2].biere"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      >
                    </div>
                    <h4 class="card-title">Et encore de la binouze
                      <br>
                      <small class="card-description text-muted">pas vraiment de la bière</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">7 €</p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="imgBieres[3].biere"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      >
                    </div>
                    <h4 class="card-title">Mdr ce sont des legos
                      <br>
                      <small class="card-description text-muted">rafraichissante</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">19 €</p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Photos des éditions précédentes</h2>
          <div class="team">
            <div class="md-layout-item md-size-66 mx-auto md-small-size-100">
              <md-card>
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
                    <img v-img:group :src="carousel1" alt="carousel1">
                  </slide>
                  <slide>
                    <img v-img:group :src="carousel2" alt="carousel2">
                  </slide>
                  <slide>
                    <img v-img:group :src="carousel3" alt="carousel3">
                  </slide>
                </carousel>
              </md-card>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Remerciements</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[4].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">Argentique UTT
                      <br>
                      <small class="card-description text-muted">Parce qu'ils font de jolies photos</small>
                    </h4>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[5].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">Media UTT
                      <br>
                      <small
                        class="card-description text-muted"
                      >Dommage qu'ils n'aient pas de talents...</small>
                    </h4>
                  </md-card>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Partenaires</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[0].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">BDE UTT
                      <br>
                      <small class="card-description text-muted">Parce qu'ils nous aiment bien</small>
                    </h4>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[1].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">Carrefour
                      <br>
                      <small
                        class="card-description text-muted"
                      >C'est toujours bien d'avoir de la bouffe</small>
                    </h4>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[2].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">Crous Reims
                      <br>
                      <small
                        class="card-description text-muted"
                      >C'est toujours sympa les subventions</small>
                    </h4>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img :src="partenaires[3].logo" alt="Thumbnail Image" class="img-fluid">
                    </div>
                    <h4 class="card-title">Maison du Boulanger
                      <br>
                      <small class="card-description text-muted">Centre Culturel</small>
                    </h4>
                  </md-card>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- 
        <div class="section text-center">
        <div class="container">
          <h2 class="title">Consommables</h2>

          <div class="team">
            <div class="md-layout mx-auto">
              <div class="md-layout-item md-medium-size-33 md-small-size-75">
                <item
                  :img="imgBieres[0].biere"
                  title="Binouze"
                  subtitle="connais pas"
                  description="input text."
                  isRaised="true"
                ></item>
                <item
                  :img="imgBieres[1].biere"
                  title="Binouze"
                  subtitle="bière locale du canada"
                  description="2.50"
                  isRaised="true"
                ></item>
                <item
                  :img="imgBieres[2].biere"
                  title="Et encore de la binouze"
                  subtitle="pas vraiment de la bière"
                  description="7 €"
                  isRaised="true"
                ></item>
                <item
                  :img="imgBieres[3].biere"
                  title="Mdr ce sont des legos"
                  subtitle="raffraichissante"
                  description="19 €"
                  isRaised="true"
                ></item>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Photos des éditions précédentes</h2>
          <div class="team">
            <div class="md-layout-item md-size-66 mx-auto md-small-size-100">
              <md-card>
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
                    <img v-img:group :src="carousel1" alt="carousel1">
                  </slide>
                  <slide>
                    <img v-img:group :src="carousel2" alt="carousel2">
                  </slide>
                  <slide>
                    <img v-img:group :src="carousel3" alt="carousel3">
                  </slide>
                </carousel>
              </md-card>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Remerciements</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <item
                  :img="partenaires[4].logo"
                  title="Argentique UTT"
                  subtitle="Parce qu'ils font de jolies photos"
                ></item>
                <item
                  :img="partenaires[5].logo"
                  title="Media UTT"
                  subtitle="Dommage qu'ils n'aient pas de talents..."
                ></item>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Partenaires</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <item
                  :img="partenaires[0].logo"
                  title="BDE UTT"
                  subtitle="Parce qu'ils nous aiment bien"
                ></item>
                <item
                  :img="partenaires[1].logo"
                  title="Carrefour"
                  subtitle="C'est toujours bien d'avoir de la bouffe"
                ></item>
                <item
                  :img="partenaires[2].logo"
                  title="Crous Reims"
                  subtitle="C'est toujours sympa les subventions"
                ></item>
                <item
                  :img="partenaires[3].logo"
                  title="Maison du Boulanger"
                  subtitle="Centre Culturel"
                ></item>
              </div>
            </div>
          </div>
        </div>
      </div>-->
    </div>
  </div>
</template>

<script>
import Item from "@/components/Item.vue";
export default {
  bodyClass: "landing-page",
  components: { Item },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/affiche/couverture2019.jpg")
    }
  },
  data() {
    return {
      carousel1: require("@/assets/img/2018/uni_son-5.jpg"),
      carousel2: require("@/assets/img/2018/uni_son-12.jpg"),
      carousel3: require("@/assets/img/2018/uni_son-35.jpg"),
      imgBieres: [
        { biere: require("@/assets/img/consommable/biere-1.jpg") },
        { biere: require("@/assets/img/consommable/biere-2.jpg") },
        { biere: require("@/assets/img/consommable/biere-3.jpg") },
        { biere: require("@/assets/img/consommable/biere-4.jpg") }
      ],
      background: require("@/assets/img/affiche/fond-bannière.png"),
      mapView: require("@/assets/img/map.png"),
      partenaires: [
        { logo: require("@/assets/img/partenaires/bdeutt.jpg") },
        { logo: require("@/assets/img/partenaires/carrefour.png") },
        { logo: require("@/assets/img/partenaires/crous.png") },
        { logo: require("@/assets/img/partenaires/maison-boulanger.jpg") },
        { logo: require("@/assets/img/partenaires/argentique.jpg") },
        { logo: require("@/assets/img/partenaires/media.jpg") }
      ]
    };
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
.md-card-actions.text-center {
  display: flex;
  justify-content: center !important;
}
.contact-form {
  margin-top: 30px;
}

.md-has-textarea + .md-layout {
  margin-top: 15px;
}
.body {
  background-image: url(../assets/img/affiche/fond-bannière.png);
  margin: 50;
}
</style>
