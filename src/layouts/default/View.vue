<template>
    <router-view />
    <v-card class="footer">
      <div class="divPrincipal">
        <div class="d-flex flex-row firstLine">
          <v-img
          clas="me-auto"
            :width="166"
            :height="32"
            src="/src/assets/logo.png"
          ></v-img>
          <v-btn class="spacingBtn" variant="text">CADASTRE-SE AGORA</v-btn>
        </div>
        <v-divider></v-divider>
        <div class="d-flex flex-row secondLine">
          <div class="me-auto d-flex">
            <v-btn variant="text" size="x-large" src="/" icon="mdi-instagram"></v-btn>
            <v-btn variant="text" size="x-large" src="/" icon="mdi-facebook"></v-btn>
            <v-btn icon size="x-large" variant="text">
              <v-avatar>
                <v-img
                  class="twtter"
                  src="/src/assets/twitter-x.png"
                ></v-img>
              </v-avatar>
            </v-btn>
          </div>
          <div class="d-flex flex-row">
            <v-sheet v-for="(itemDownload, index) in itemsDownload" :key="index" :height="40" color="#FFFFFF" class="mt-4 mr-4" :width="114" rounded>
              <div class="d-flex">
                <v-img
                  class="ml-n9 mt-2"
                  :width="200"
                  :height="25"
                  :src="itemDownload.iconSrc"
                ></v-img>
                <div>
                  <p class="description1">{{ itemDownload.description1 }}</p>
                  <p class="description2">{{ itemDownload.description2 }}</p>
                </div>
              </div>
            </v-sheet>
          </div>
        </div>
      </div>
    </v-card>
</template>

<script>
export default {
  data() {
    return {
      itemsDownload: [
        { iconSrc: "/src/assets/icons8-mac-os-60.png", description1: "Grátis na", description2: "App store" },
        { iconSrc: "/src/assets/icons8-google-play-60.png", description1: "Grátis na", description2: "Play store" },
      ]
    }
  }
}
</script>


<style scoped>
.footer {
  background-color: #4E42FF0D;
  height: 200px;
}
.divPrincipal {
  margin-left: 20%;
  margin-right: 20%;
}
.firstLine {
  margin-top: 25px;
  margin-bottom: 25px;
}
.spacingBtn {
  font-weight: 600;
}

.secondLine {
  margin-top: 15px;
  margin-left: 12px;
}
.imgTwitter {
  padding-top: 2px;
  margin-left: -105px;
}
.description1 {
  font-size: 8px;
  margin-left: -35px;
  margin-top: 6px;
}
.description2 {
  font-size: 12px;
  font-weight: 600;
  margin-left: -35px;
}

.twtter {
  width: 10px;
}

</style>

