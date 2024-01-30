<template>
  <v-main overflow-y:auto>
    <v-navigation-drawer class="w-100" temporary location="right" hide-overlay @resize="checkWindowSize" v-model="drawer"> <!--dentro do menu-->
      <v-list class="d-flex mx-auto"> <!--menu pequeno-->
        <v-img
          src="/src/assets/Logo-icone.png"
          :height="60"
          class="d-flex dimensionImage"
          @click="smallScrollMenu('home')"
        ></v-img>

        <v-spacer></v-spacer>

        <v-btn
          variant="plain"
          class="mt-3"
          @click.stop="drawer = !drawer"
        >
        <v-icon size="30">mdi-window-close</v-icon>
        </v-btn>
      </v-list>

      <v-divider class="mb-2"></v-divider>

      <v-list
        v-for="(section, index) in sections"
        :key="index"
      >
        <v-list-item
          variant="plain"
          @click="smallScroll(section.id)"
          class="pb-8 pt-10 mt-n4 ml-6 mr-6"
        >{{ section.title }} 
        </v-list-item>
        <v-divider class="mx-6 mb-4 mt-0 mb-n2" :thickness="2"></v-divider>
      </v-list>

      <div class="d-flex flex-column mt-6 align-center">
        <v-text-field
          class="emailInputNavigation"
          density="compact"
          variant="outlined"
          rounded="xl"
          placeholder="Insira seu e-mail"
        >
        </v-text-field>
        <v-btn 
          rounded="xl" 
          class="btnRegisterNavigation"
        ><b>CADASTRE-SE AGORA</b>
        </v-btn>
      </div>
    </v-navigation-drawer>

    <v-app-bar :elevation="0.5">
      <div class="me-auto d-none d-md-flex">
        <v-img 
          :width="200"
          :height="38"
          src="/src/assets/Logo-padrao.png"
          @click="scroll('home')"
          class="distanceLeft"
        ></v-img>
      </div>
      <div class="d-none d-md-flex distanceRight"> 
        <v-btn variant="plain" color="#000000" @click="scroll('beneficios')">BENEFÍCIOS</v-btn>
        <v-btn variant="plain" color="#000000" @click="scroll('comoFunciona')">COMO FUNCIONA</v-btn>
        <v-btn variant="plain" color="#000000" @click="scroll('planos')">PLANOS</v-btn>
        <v-btn variant="plain" color="#000000" @click="scroll('faq')">FAQ</v-btn>
        <v-btn variant="outlined" rounded="xl">Cadastre-se agora</v-btn>
      </div>
      <div class="d-sm-flex mx-auto d-md-none"> 
        <v-img 
          :width="100"
          :height="38"
          src="/src/assets/Logo-icone.png"
          @click="scroll('home')"
        ></v-img> 
      </div>
      <v-spacer class="d-sm-flex d-md-none"></v-spacer>
      <v-btn variant="outlined" rounded="xl" class="d-sm-flex d-md-none">Cadastre-se agora</v-btn>
      <v-btn variant="plain" class="iconMenu d-sm-flex d-md-none" @click.stop="drawer = !drawer">
        <v-icon size="30">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <LandingPage/>
  </v-main>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      sections: [
        { id: 'beneficios', title: 'BENEFÍCIOS' },
        { id: 'comoFunciona' ,title: 'COMO FUNCIONA' },
        { id: 'planos', title: 'PLANOS' },
        { id: 'faq', title: 'FAQ' },
      ],
    };
  },
  methods: {
    // Checa tamanho da tela para fechar o navigation automamticamente se acima de 959px
    checkWindowSize() {
      if (window.innerWidth > 959) {
        this.drawer = false;
      }
    }, 
    // Rolagem rápida
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
    },
    // Navigation menor fecha ao clicar
    smallScroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
      this.drawer = false;
    }, 
    // Navigation menor fecha ao clicar (imagem)
    smallScrollMenu(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
      this.drawer = false;
    },
    // Fechar navigation
    closeMenu() {
      this.drawer = false;
    },
  },
  watch: {
    // Adiciona ou remove a classe 'drawer-open' no elemento body quando o drawer é aberto ou fechado
    drawer(value) {
      document.documentElement.style.overflowY = value ? 'hidden' : 'auto';
    },
  },
  mounted() {
    window.addEventListener('resize', this.checkWindowSize);
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.checkWindowSize);
  }
};

</script>

<style>

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

@media screen and (min-width: 960px) and (max-width: 1279px) {
  .distanceLeft {
    margin-left: 20% !important;
  }
  .distanceRight {
    margin-right: 2% !important;
  }
}

  
.dimensionImage {
  cursor: pointer;
  margin-right: 50%;
  margin-left: 10px;
}

.emailInputNavigation {
  width: 343px !important;
  height: 40px;
  margin-top: 20px;
  margin-bottom: 15px;
}

.btnRegisterNavigation {
  background-color: #161B33 !important;
  color: #FFFFFF;
  width: 343px !important;
  height: 40px !important;
}

.iconMenu {
  margin-right: 10px;
  margin-top: 2px;
}

.align-center {
  align-items: center;
}

.distanceLeft {
  margin-left: 50%;
}

.distanceRight {
  margin-right: 5%;
}

</style>