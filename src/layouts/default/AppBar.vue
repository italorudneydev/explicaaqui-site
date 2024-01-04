<template>
  <v-app-bar flat>
    <div class="divPrincipal d-flex">
      <div class="me-auto">
        <v-img 
          class="spacingImg"
          :width="200"
          :height="38"
          src="/src/assets/Logo-padrão.png"
        ></v-img>
      </div>
      <div>
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

    }
  }
}
</script>

<style>

.divPrincipal {
  margin-left: 15%;
  margin-right: 15%;
}

.spacingImg {
  margin-right: 400px;

}

</style>
