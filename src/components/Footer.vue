<template>
  <footer>
    <v-card class="footer">
      <div class="divPrincipal">
        <v-row class="firstLine">
            <v-img
            class="spacingImg"
            :width="166"
            :height="32"
            src="/src/assets/logo.png"
            ></v-img>
            <v-btn class="spacingBtn" variant="text">CADASTRE-SE AGORA</v-btn>
        </v-row>
        <v-divider></v-divider>

        <div class="secondLine d-flex">
          <div class="me-auto">
            <v-btn variant="plain" size="x-large" class="mx-n12" src="/"><v-icon>mdi-instagram</v-icon></v-btn>
            <v-btn variant="plain" size="x-large" src="/"><v-icon>mdi-facebook</v-icon></v-btn>
            <v-btn variant="plain" class="imgTwitter" src="/">
              <v-img
                class=""
                :width="200"
                :height="25"
                src="/src/assets/twitter-x.png"
              ></v-img>
            </v-btn>
          </div>
          <div>
            <v-row>
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
            </v-row>
          </div>
        </div>
      </div>
    </v-card>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
footer {
  background-color: #34495e;
  color: #fff;
  padding: 10px;
  text-align: center;
}
.footer {
  background-color: #4E42FF0D;
  height: 200px;
}
.divPrincipal {
  margin-left: 20%;
  margin-right: 20%;
  margin-bottom: 2%;
}
.firstLine {
  margin-top: 20px;
  margin-bottom: 10px;
}
.spacingBtn {
  font-weight: 600;
}

.secondLine {
  margin-top: 25px;
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
.spacingImg {
  margin-left: -30%;
}

@media (max-width: 600px) {
  .menu-btn {
      margin-right: 1vw; /* ou ajuste conforme necessário para telas menores */
  }
}

@media (max-width: 1800px) {
  .spacingImg {
    margin-left: -10%;
  }
}

</style>
