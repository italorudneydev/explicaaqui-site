<template>
  <v-app-bar flat>
    <div class="divPrincipal d-flex">
      <div class="me-auto">
        <v-img 
          :width="200"
          :height="38"
          src="/src/assets/Logo-padrão.png"
        ></v-img>
      </div>
      <div class="spacingText">
        <v-btn variant="text">BENEFÍCIOS</v-btn>
        <v-btn variant="text">COMO FUNCIONA</v-btn>
        <v-btn variant="text">PLANOS</v-btn>
        <v-btn variant="text">FAQ</v-btn>
        <v-btn variant="outlined" rounded="xl">Cadastre-se agora</v-btn>
      </div>
    </div>
  </v-app-bar>
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

<style>

.divPrincipal {
  margin-top: 2%;
  margin-left: 15%;
  margin-right: 15%;
}

.spacingText {
  margin-right: -30%;
}

.spacingImg {
  margin-right: 400px;
}

</style>
