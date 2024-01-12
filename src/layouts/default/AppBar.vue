<template>
  <v-main>
    <v-card clas="header">
      <div class="justify-center d-flex">
        <div class="me-auto d-none d-md-flex d-lg-flex d-xl-flex">
          <v-img 
            :width="200"
            :height="38"
            src="/src/assets/Logo-padrão.png"
          ></v-img>
        </div>
        <div class="d-sm-flex d-md-none">
          <v-img 
            :width="200"
            :height="38"
            src="/src/assets/Logo-icone.png"
          ></v-img>
        </div>
        <div class="spacingText d-none d-md-flex d-lg-flex d-xl-flex">
          <v-btn variant="text">BENEFÍCIOS</v-btn>
          <v-btn variant="text">COMO FUNCIONA</v-btn>
          <v-btn variant="text">PLANOS</v-btn>
          <v-btn variant="text">FAQ</v-btn>
          <v-btn variant="outlined" rounded="xl">Cadastre-se agora</v-btn>
        </div>
      </div>
    </v-card>
  </v-main>
</template>

<style>

.header {
  background-color: #4E42FF0D;
  height: 200px;
}

.spacingText {
  margin-right: 0%;
}

</style>
