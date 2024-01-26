<template>
    <router-view />
    <v-card class="footer">
      <div class="justify-center spacingPrincipalNavigation">
        <div class="d-flex align-center flex-row secondLine">
          <div class="me-auto d-flex">
            <v-img 
              :width="150"
              :height="32"
              src="/src/assets/Logo-padrao.png"
              class="mb-6 mt-3"
            ></v-img>
          </div>
          <div class="d-flex flex-row mt-n3">
            <v-btn class="spacingBtn" to="/" variant="text">CADASTRE-SE AGORA</v-btn>
          </div>
        </div>

        <v-divider class="mx-3"></v-divider>

        <div class="d-flex align-center flex-row secondLine">
          <div class="me-auto d-flex">
            <v-btn class="spacingIconsSmallGrid" variant="text" size="x-large" src="/" icon="mdi-instagram"></v-btn>
            <v-btn class="spacingIconsSmallGrid" variant="text" size="x-large" src="/" icon="mdi-facebook"></v-btn>
            <v-btn icon size="x-large" class="spacingIconsSmallGrid" variant="text">
              <v-avatar>
                <v-img 
                  class="twitter"
                  src="/src/assets/twitter-x.png"
                ></v-img>
              </v-avatar>
            </v-btn>
          </div>
          <div class="d-flex flex-row mt-n3">
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

@media screen and (max-width: 959px) {
  .spacingPrincipalNavigation {
    margin-top: 15px;
  }
}
  
@media screen and (min-width: 960px) {
  .spacingPrincipalNavigation {
    margin-left: 150px;
    margin-right: 10%;
    margin-top: 18px;
  }
}

@media screen and (max-width: 600px) {
  .spacingIconsSmallGrid {
    margin-right: -10px !important;
    margin-left: -20px;
  }
}
.footer {
  background-color: #4E42FF0D;
  height: 200px;
}
.align-center {
  align-items: center;
}
.secondLine {
  margin-top: 15px;
  margin-left: 12px;
}
.twitter {
  width: 10px;
}
.spacingBtn {
  font-weight: 600;
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

</style>

