<template>
  <div class="hero is-white" v-if="showAll">
    <div class="hero-body">
      <div class="container">
        <h1 class="title is-1 is-size-2-touch is-700">talleres en simultaneo</h1>
        <br />
        <br />
        <div class="columns is-centered" v-if="showPrimerBloque">
          <div class="column is-5">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${primerBloque[0].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{primerBloque[0].title}}</p>
          </div>
          <div class="column is-5 is-offset-2">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${primerBloque[1].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{primerBloque[1].title}}</p>
          </div>
        </div>
        <div class="columns is-centered" v-if="showSegundoBloque">
          <div class="column is-5">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${segundoBloque[0].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{segundoBloque[0].title}}</p>
          </div>
          <div class="column is-5 is-offset-2">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${segundoBloque[1].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{segundoBloque[1].title}}</p>
          </div>
        </div>
        <div class="columns is-centered" v-if="showTercerBloque">
          <div class="column is-5">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${tercerBloque[0].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{tercerBloque[0].title}}</p>
          </div>
          <div class="column is-5 is-offset-2">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${tercerBloque[1].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{tercerBloque[1].title}}</p>
          </div>
        </div>
        <div class="columns is-centered" v-if="showCuartoBloque">
          <div class="column is-5">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${cuartoBloque[0].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{cuartoBloque[0].title}}</p>
          </div>
          <div class="column is-5 is-offset-2">
            <div class="videoWrapper">
              <iframe
                width="560"
                height="315"
                :src="`https://www.youtube.com/embed/${cuartoBloque[1].videoId}`"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
            <br />
            <hr class="custom-hr" />
            <p class="title is-4 has-text-black">{{cuartoBloque[1].title}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      now: new Date(),
      fridayStarts: new Date(Date.UTC(2020,3,24,3,0,0)),
      fridayEnds: new Date(Date.UTC(2020,3,25,2,59,59)),
      saturdayStarts: new Date(Date.UTC(2020,3,25,3,0,0)),
      saturdayEnds: new Date(Date.UTC(2020,3,26,2,59,59)),
      intervalId: null,
      primerBloque: [
        {
          title: "Exploraciones para escenarios posdomésticos",
          videoId: "HCtGbrao2Ak"
        },
        {
          title: "El lugar como sistema vivo",
          videoId: "386N_R6Em8E"
        }
      ],
      segundoBloque: [
        {
          title: "Herramientas digitales para gobierno abierto",
          videoId: "lWIAppvv4YQ"
        },
        {
          title:
            "Fairbnb.coop: Cómo activar la economía circular en tiempos de corona virus",
          videoId: "dPZf5Cco8eA"
        }
      ],
      tercerBloque: [
        {
          title:
            "Empoderamiento comunitario como herramienta para el cambio en barrios populares",
          videoId: "uT26GAqTw0E"
        },
        {
          title: "Red(d)Red(s)",
          videoId: "ohcplHCXW40"
        }
      ],
      cuartoBloque: [
        {
          title:
            "CO.VIDA: Metodologías Digitales para la Cocreación de nuestra vida social urbana",
          videoId: "dHy17jvnAIk"
        },
        {
          title: "Rebeldía Urbana",
          videoId: "lPty-K35FOk"
        }
      ]
    };
  },
  components: {},
  mounted: function() {
    this.intervalId = setInterval(this.updateTime, 30000);
  },
  beforeDestroy() {
    if (this.intervalId) clearInterval(this.intervalId);
  },
  methods: {
    updateTime: function() {
      this.now = new Date();
    }
  },
  computed: {
    isFriday: function() {
      if (this.fridayStarts < this.now && this.now < this.fridayEnds)
        return true;
      return false;
    },
    isSaturday: function() {
      if (this.saturdayStarts < this.now && this.now < this.saturdayEnds)
        return true;
      return false;
    },
    showAll: function() {
      return (
        this.showPrimerBloque ||
        this.showSegundoBloque ||
        this.showTercerBloque ||
        this.showCuartoBloque
      );
    },
    showPrimerBloque: function() {
      let start = new Date(Date.UTC(2020,3,24,17,45,0))
      let end = new Date(Date.UTC(2020,3,24,19,45,0))
      if (start <= this.now && this.now < end) return true;
      return false;
    },
    showSegundoBloque: function() {
      let start = new Date(Date.UTC(2020,3,24,19,15,0))
      let end = new Date(Date.UTC(2020,3,24,21,15,0))
      if (start <= this.now && this.now < end) return true;
      return false;
    },
    showTercerBloque: function() {
      let start = new Date(Date.UTC(2020,3,25,17,45,0))
      let end = new Date(Date.UTC(2020,3,25,19,45,0))
      if (start <= this.now && this.now < end) return true;
      return false;
    },
    showCuartoBloque: function() {
      let start = new Date(Date.UTC(2020,3,25,19,15,0))
      let end = new Date(Date.UTC(2020,3,25,21,15,0))
      if (start <= this.now && this.now < end) return true;
      return false;
    }
  }
};
</script>

<style lang="scss" scoped>
.hero.is-custom {
  background-color: #6e559e;
}
.custom-hr {
  width: 200px;
  background-color: #000;
  height: 1px;
}
.videoWrapper {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 */
  height: 0;
}
.videoWrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>