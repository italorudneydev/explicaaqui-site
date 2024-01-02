<template>
  <v-app>
    <v-card variant="flat" class="principalCard">
      <div class="principalDiv d-flex justify-center align-center h-100"> <!-- Utilize "h-100" para ocupar 100% da altura -->
        <div class="spacing"> <!-- div 1 -->
          <p class="titlename"><v-icon>mdi-flash</v-icon>PLATAFORMA EXCLUSIVA</p>
          <h1 class="mt-4 mb-5">Conecte-se com outros servidores públicos e amplie seu conhecimento</h1>
          <p class="mr-3">
            Com o Explica Aqui, você tira suas dúvidas, aprende com os melhores especialistas e constrói uma rede de contatos para se manter atualizado e avançar na carreira.
          </p>
          <div class="d-flex mt-4 justify-center">
            <v-text-field
              class="insertButton"
              bg-color="#FFFFFF"
              variant="flat"
              density="compact"
              rounded="xl"
              placeholder="Insira seu e-mail"
            >
            </v-text-field> 
            <v-btn 
              rounded="xl" 
              class="registerButton"
            >CADASTRE-SE AGORA</v-btn>
          </div>
        </div>
        <div class="imagemPrincipal"> <!-- div 2 -->
          <v-card variant="flat" rounded="xl">
            <v-img
              :width="504"
              :height="381"
              aspect-ratio="16/9"
              cover
              src="/src/assets/tablet-digital-pode-resolver-o-problema 1.png"
            ></v-img>
          </v-card>
          <v-img
          src="/src/assets/image-PhotoRoom.png-PhotoRoom.png"
          class="spacingImage1"
          :width="183"
          >
          </v-img>
          <v-img
          src="/src/assets/tiresuaduvida.png"
          class="spacingImage2"
          :width="253"
          >
          </v-img>
        </div>
      </div>
    </v-card>
    <div class="principalDiv d-flex justify-center align-center">
      <div>
        <img 
        src="/src/assets/image-removebg.png"
        :width="472"
        :height="600">
      </div>
      <div class="mt-15">
        <h1 class="mb-8 ml-14">Aprenda, colabore com colegas e se desenvolva profissionalmente</h1>
          <v-row align="center" justify="center">
            <v-col v-for="(variant, i) in variants" :key="i" cols="auto">
              <v-card class="mx-auto ml-5" max-width="280" variant="flat">
                <v-card-item>
                  <div>
                    <v-sheet variant="tonal" :color="colors[i]" :height="40" :width="40" rounded="lg" ><v-icon :color="colorIcon[i]" size="17" class="colorIcon" >{{ variant.icon }}</v-icon></v-sheet>
                    <h6 class="classTitle">{{ variant.title }}</h6>
                    <div>{{ variant.description }}</div>
                  </div>
                </v-card-item>
              </v-card>
            </v-col>
          </v-row>
          
      </div>
     

    </div>

  </v-app>
</template>


<script>
import { VApp } from 'vuetify/lib/components/index.mjs';

export default {
  data() {
    return {
      colors: ['#F6F5FF','#FFF6FA','#FEF9D5CC', '#F3F3F5'],
      colorIcon: ['#4E42FF','#FF57A7','#FFDE13', '#1C1B1F'],
      variants: [
        { icon: 'mdi-message-text-outline', title: 'Respostas com quem entende', description: 'Obtenha respostas precisas e atualizadas de profissionais qualificados da área.' },
        { icon: 'mdi-chart-box-plus-outline', title: 'Aprimore suas habilidades', description: 'Transforme cada interação em uma oportunidade única de desenvolvimento profissional' },
        { icon: 'mdi-web', title: 'Cresça em comunidade', description: 'Compartilhe experiências, insights e desenvolva relacionamentos profissionais.' },
        { icon: 'mdi-gesture-tap-hold', title: 'Conhecimento na palma da mão', description: 'Garanta uma experiência de aprendizado contínuo onde quer que você esteja.' }
      ],
    };
  }
};

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Sora&display=swap');

* {
font-family: 'Sora', sans-serif;
}

.titlename {
  font-weight: 600;
  font-size: 14px;
}

.principalCard {
  background-color: #edecff;
  height: 552px;
}

.principalDiv {
  margin-left: 20%;
  margin-right: 20%;
}

.spacing {
  margin-right: 15%;
  
}

.insertButton {
  width: 219px !important;
  height: 40px;
  margin-right: 12px;
  margin-top: 15px;
  margin-bottom: 40px;
  font-weight: 600 !important;
}

.imagemPrincipal {
  margin-top: 35px;
  margin-left: 20px;
  margin-right: 20px;
}

.registerButton {
  background-color: #161B33 !important;
  color: white !important;
  width: 199px;
  height: 40px;
  margin-top: 15px;
  margin-bottom: 40px;
  font-weight: 600 !important;
  font-size: 13px;
}

.spacingImage1 {
  margin-top: -350px;
  margin-left: -40px;
}

.spacingImage2 {
  margin-top: 205px;
  margin-left: 240px;
}

.colorIcon {
  padding-left: 20px;
  padding-top: 14px;
  height: 17px;
  width: 17px !important;
}

.btnIcon {
  width: 6px !important;
}

.classTitle {
  margin-top: 12px;
  margin-bottom: 12px;
  font-size: 24px;
  font-weight: 600;
}

</style>